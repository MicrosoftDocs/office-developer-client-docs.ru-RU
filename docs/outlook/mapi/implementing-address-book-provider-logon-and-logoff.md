---
title: Реализация входа и выхода для поставщика адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 1ffde0814fe5024a3f89a93462c48136712f1013
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809306"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Реализация входа и выхода для поставщика адресной книги

**Относится к**: Outlook 
  
Поставщиками адресных книг поддерживать сеанса входа в систему и выход из системы за счет реализации методов из [IABProvider: IUnknown](iabprovideriunknown.md) интерфейса. ** IABProvider ** интерфейс наследует непосредственно из **IUnknown** и добавляет только два других метода: **Вход в систему** и **Завершение работы**. 
  
## <a name="logoff"></a>Выход из системы

MAPI будет вызов метода [IABProvider::Logon](iabprovider-logon.md) ваш поставщик в начале каждого сеанса и каждый раз, когда у поставщика добавляется в текущий профиль клиента поддерживает динамической перенастройки. Когда MAPI вызывает метод **IABProvider::Logon** , адресной книге начинается его процесс входа. 
  
**Для реализации IABProvider::Log**
  
1. Инициализируйте все указатели параметра выходные данные, переданного по MAPI. 
    
2. Вызовите метод **IUnknown::AddRef** объекта поддержки увеличить счетчик ссылок на него. 
    
3. Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки откройте раздел профиль, который содержит сведения о конфигурации о ваш поставщик. Передайте значение NULL для параметра _lpUID_ и флаг MAPI_MODIFY, если требуется внести изменения. 
    
4. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) раздела профиля для извлечения свойств, поставщик должен для входа в систему, таких как имя таблицы данных, файл или базы данных. 
    
5. Убедитесь, что установлен свойства всех доступных и допустимый. Если необходимо, разрешенных отображения диалогового окна на запрос пользователю для исправлений или дополнении недопустимый или отсутствующий сведения и вызовите метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля, чтобы сохранить изменения. Ниже перечислены некоторые общие свойства, которые должны быть доступны: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Не устанавливайте **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) или **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)). Во время входа в систему эти свойства доступны только для чтения. 
  
6. При отсутствии одного или нескольких свойств конфигурации с ошибкой, а возвращаемое значение MAPI_E_UNCONFIGURED.
    
7. Вызов [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) для регистрации [MAPIUID](mapiuid.md). Ваш поставщик можно создать **MAPIUID** с: 
    
   - Вызов метода [IMAPISupport::NewUID](imapisupport-newuid.md) . 
    
   - Вызов UUIDGEN. Tool exe-ФАЙЛ, чтобы задать идентификатор GUID, который использует ваш поставщик, чтобы включить в один из файлов заголовка.
    
8. При желании сохранить только что созданный **MAPIUID** текущего профиля, вызвав раздела профиля ** IMAPIProp::SetProps ** метод. 
    
9. Освобождение раздела профиля путем вызова метода **функции IUnknown::Release** . 
    
10. Создайте экземпляр объекта входа в систему и установите содержимое параметра _lppABLogon_ адрес этого нового объекта. 
    
Поскольку существует возможность MAPI для вызова вашей ** входа ** метод несколько раз во время сеанса имеет смысл для поддержки этой возможности в реализации по возможность создать несколько объектов входа в систему и отслеживание каждого объекта, которая создается. Поддержка нескольких звонков **входа** позволяет пользователю из клиентского приложения, например войти в сеанс с разными удостоверениями и использования различных доставки назначений. 
  
**Завершение работы** вызывается при завершении сеанса. MAPI вызывает метод [IABProvider::Shutdown](iabprovider-shutdown.md) как один из последней задачи в завершение работы сеанса. MAPI выпущен все объекты ваш поставщик входа в систему и, если ваш поставщик получает этот вызов, его можно допустить, что это последний звонок, он будет получать. В реализации **IABProvider::Shutdown**Очистка, если вам не требуется. Например ваш поставщик может вызвать **MAPIDeinitIdle** , если называется **MAPIInitIdle** простоя модуль во время сеанса или метод **функции IUnknown::Release** любые объекты, которые еще не нужно освободить по. 
  
Если ваш поставщик не окончательную, его реализация может состоять из одной строки кода: 
  
```cpp
return S_OK;

```

