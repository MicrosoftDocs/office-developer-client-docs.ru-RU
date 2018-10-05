---
title: Реализация входа для поставщика службы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401645"
---
# <a name="implementing-service-provider-logon"></a>Реализация входа для поставщика службы

**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI вызывает метод в объект поставщика для начала процесса входа в систему с помощью указателя, который возвращает из вашей функции точки входа. Метод следующим образом может отличаться в зависимости от типа поставщика услуг:
  
- [IABProvider::Logon](iabprovider-logon.md) для поставщиками адресных книг 
    
- [IMSProvider::Logon](imsprovider-logon.md) для поставщиков хранилища сообщений 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) для поставщиками транспорта 
    
Выполните следующие задачи в любой реализации метода входа в систему.
  
1. Увеличивает счетчик ссылок на объекте поддержки, который передается в качестве входного параметра путем вызова метода [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) . 
    
2. Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки для доступа к вашей раздела профиля. 
    
3. Вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля для настройки следующих свойств: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Не следует задать свойства **PR_RESOURCE_FLAGS** или **PR_PROVIDER_DLL_NAME** раздела профиля. Во время входа в систему эти свойства доступны только для чтения. 
  
4. Проверьте, что свойства, которые необходимы для настройки хранятся в профиле или от пользователя. Дополнительные сведения о проверке конфигурации можно [Проверка конфигурации поставщика службы](verifying-service-provider-configuration.md).
    
5. Вызов метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) объекта поддержки для регистрации уникального идентификатора или [MAPIUID](mapiuid.md), если ваш поставщик является поставщик адресной книги или сообщения хранилища. Поставщики транспорта зарегистрировать структур **MAPIUID** при MAPI вызывает метод их [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . Дополнительные сведения о регистрации **MAPIUID**можно [Регистрации уникальных идентификаторов поставщика службы](registering-service-provider-unique-identifiers.md).
    
6. Создайте экземпляр объекта входа в систему и возврата с одним из следующих значений:
    
  - Значение S_OK для указания успешного входа в систему.
    
  - MAPI_E_UNCONFIGURED, чтобы указать, что один или несколько свойств конфигурации будет недоступен.
    
  - MAPI_E_USER_CANCEL, чтобы указать, что пользователь отменил окно настройки вызывает ошибку свойства конфигурации, которые будут недоступны.
    
  - MAPI_E_FAILONEPROVIDER, чтобы указать, что ваш поставщик может не настроен, но, что MAPI, должна поддерживать его для использования в любом случае. Методы входа в систему должна вернуть это значение, чтобы сообщить о Исправимая ошибка, например, когда поставщика требуется пароль и не могут запрашивать у пользователя его так, как отключить пользовательский интерфейс. 
    
Предыдущая список задач описываются минимальные реализации метода входа в систему поставщика службы. При необходимости можно включить дополнительные функции. Например некоторые поставщики вызов [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) для обновления таблицы состояния в их способ входа в систему. 
  
> [!NOTE]
> Для достижения наилучшей производительности во время входа в систему, избегайте вызова [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) или [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Перед эти вызовы можно выполнить и вернуть управление в метод входа в систему, необходимо запустить диспетчер очереди MAPI. 
  
## <a name="see-also"></a>См. также

- [Запуск поставщика службы](starting-a-service-provider.md)

