---
title: Реализация logon поставщика услуг
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
# <a name="implementing-service-provider-logon"></a>Реализация logon поставщика услуг

**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI вызывает метод в объекте поставщика для начала процесса логона с помощью указателя, возвращаемого с функции точки входа. Метод изменяется следующим образом, в зависимости от типа поставщика услуг:
  
- [IABProvider::Logon](iabprovider-logon.md) для поставщиков адресных книг 
    
- [IMSProvider::Logon](imsprovider-logon.md) для поставщиков магазинов сообщений 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) для поставщиков транспорта 
    
Выполните следующие задачи в любом методе logon, который вы реализуете:
  
1. Прибавка отсчета ссылок на объект поддержки, передаваемого в качестве параметра ввода, вызывает его [метод IUnknown::AddRef.](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) 
    
2. Чтобы получить доступ к разделу профилей, позвоните в [метод IMAPISupport::OpenProfileSection.](imapisupport-openprofilesection.md) 
    
3. Чтобы установить следующие свойства, позвоните по методу [IMAPIProp::SetProps в разделе IMAPIProp.](imapiprop-setprops.md) 
    
  - **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
  - **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)
    
  - **PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)
    
  - **PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Не пытайтесь установить свойства PR_RESOURCE_FLAGS  **или PR_PROVIDER_DLL_NAME** профиля. Во время логоса эти свойства являются только для чтения. 
  
4. Убедитесь, что свойства, необходимые для настройки, хранятся в профиле или доступны пользователю. Дополнительные сведения о проверке конфигурации см. в дополнительных сведениях [о проверке конфигурации поставщика услуг.](verifying-service-provider-configuration.md)
    
5. Вызов метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации уникального идентификатора или [MAPIUID,](mapiuid.md)если поставщик является поставщиком адресной книги или магазина сообщений. Поставщики транспорта регистрируют **структуры MAPIUID,** когда MAPI вызывает их [метод IXPLogon::AddressTypes.](ixplogon-addresstypes.md) Дополнительные сведения о регистрации **MAPIUID** см. в документе [Registering Service Provider Unique Identifiers.](registering-service-provider-unique-identifiers.md)
    
6. Мгновенно укачив объект logon и вернись с одним из следующих значений:
    
  - S_OK указать успешный логотип.
    
  - MAPI_E_UNCONFIGURED указывает, что одно или несколько свойств конфигурации недоступны.
    
  - MAPI_E_USER_CANCEL, что пользователь отменил диалоговое окно конфигурации, из-за чего свойства конфигурации были недоступны.
    
  - MAPI_E_FAILONEPROVIDER, чтобы указать, что поставщик не может быть настроен, но что MAPI следует разрешить его использовать независимо. Методы Logon должны вернуть это значение, чтобы сообщить о нефатальной ошибке, например, когда поставщику требуется пароль и он не может подсказать пользователю его, так как пользовательский интерфейс отключен. 
    
В предыдущем списке задач описывается минимальная реализация метода логотипа поставщика услуг. При необходимости можно включить дополнительные функции. Например, некоторые поставщики называют [IMAPISupport::ModifyStatusRow,](imapisupport-modifystatusrow.md) чтобы обновить таблицу состояния в методе logon. 
  
> [!NOTE]
> Чтобы достичь максимальной производительности во время логотипа, не вызывайтесь в [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) или [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Прежде чем эти вызовы смогут завершить и вернуть управление методу logon, необходимо начать использовать пуллер MAPI. 
  
## <a name="see-also"></a>См. также

- [Запуск поставщика услуг](starting-a-service-provider.md)

