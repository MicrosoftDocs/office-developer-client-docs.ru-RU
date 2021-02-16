---
title: Реализация службы для логоса
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310089"
---
# <a name="implementing-service-provider-logon"></a>Реализация службы для логоса

**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI вызывает метод в объекте поставщика, чтобы начать процесс входа с помощью указателя, возвращаемого функцией точки входа. Этот метод зависит от типа поставщика услуг:
  
- [IABProvider::Logon](iabprovider-logon.md) для поставщиков адресных книг 
    
- [IMSProvider::Logon](imsprovider-logon.md) for message store providers 
    
- [IXPProvider::TransportLogon для](ixpprovider-transportlogon.md) поставщиков транспорта 
    
Выполните следующие задачи в любом методе для логоса, который вы реализуете:
  
1. Приращение отсчета ссылки на объект поддержки, который передается в качестве входного параметра, путем вызова метода [IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) 
    
2. Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки, чтобы получить доступ к разделу профиля. 
    
3. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля, чтобы установить следующие свойства: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)
    
  - **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)
    
  > [!NOTE]
  > Не пытайтесь установить свойства PR_RESOURCE_FLAGS **или** **PR_PROVIDER_DLL_NAME** профиля. Во время logon эти свойства являются только для чтения. 
  
4. Убедитесь, что свойства, необходимые для настройки, хранятся в профиле или доступны пользователю. Дополнительные сведения о проверке конфигурации см. в под [вопросе "Проверка конфигурации поставщика услуг".](verifying-service-provider-configuration.md)
    
5. Вызовите метод [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) объекта поддержки, чтобы зарегистрировать уникальный идентификатор или [MAPIUID,](mapiuid.md)если ваш поставщик является адресной книгой или поставщиком store сообщений. Поставщики транспорта регистрируют структуры **MAPIUID,** когда MAPI вызывает метод [IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Дополнительные сведения о регистрации **MAPIUID** см. в документе [Registering Service Provider Unique Identifiers.](registering-service-provider-unique-identifiers.md)
    
6. С помощью одного из следующих значений обновите объект для логотипа и вернетесь:
    
  - S_OK, чтобы указать успешное в logon.
    
  - MAPI_E_UNCONFIGURED, что одно или несколько свойств конфигурации недоступны.
    
  - MAPI_E_USER_CANCEL, что пользователь отменил диалоговое окно конфигурации, из-за чего свойства конфигурации недоступны.
    
  - MAPI_E_FAILONEPROVIDER, что поставщик не может быть настроен, но mapI должен разрешить его использовать независимо от того. Методы для доступа к данным должны возвращать это значение, чтобы сообщить о некритальной ошибке, например о том, что поставщику требуется пароль и он не может завести его у пользователя, так как пользовательский интерфейс отключен. 
    
В предыдущем списке задач описана минимальная реализация метода для работы с поставщиком услуг. При необходимости можно включить дополнительные функции. Например, некоторые поставщики звонят по методу [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы обновить таблицу состояния. 
  
> [!NOTE]
> Чтобы добиться максимальной производительности при во время работы при logon, избегайте вызова [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) или [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) Прежде чем эти вызовы завершались и возвратит управление методу для логотипа, необходимо начать работу пула MAPI. 
  
## <a name="see-also"></a>См. также

- [Запуск поставщика услуг](starting-a-service-provider.md)

