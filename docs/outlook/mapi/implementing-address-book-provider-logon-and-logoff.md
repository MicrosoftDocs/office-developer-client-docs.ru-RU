---
title: Реализация логона поставщика адресных книг и logoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c4a1fb5d-ae23-445b-a6f0-ef430b03fc9a
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8d33bccdd01075d692e5a887082ba51ee23bb083
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438738"
---
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Реализация логона поставщика адресных книг и logoff

**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщики адресных книг поддерживают логотип сеанса и вход, реализуя методы интерфейса [IABProvider: IUnknown.](iabprovideriunknown.md) Интерфейс ** IABProvider ** наследуется непосредственно от **IUnknown** и добавляет только два других метода: **Logon** и **Shutdown.** 
  
## <a name="logoff"></a>Logoff

MAPI будет вызывать метод [IABProvider::Logon](iabprovider-logon.md) поставщика в начале каждого сеанса и всякий раз, когда поставщик добавляется в текущий профиль и клиент поддерживает динамическую перенастройку. Когда MAPI вызывает **метод IABProvider::Logon,** поставщик адресных книг начинает процесс логона. 
  
**Реализация IABProvider::Log**
  
1. Инициализация всех указателей параметров вывода, переданных MAPI. 
    
2. Вызов метода **IUnknown::AddRef** объекта поддержки, чтобы прибавить количество ссылок. 
    
3. Вызов метода [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки, чтобы открыть раздел профиля, содержащий сведения о конфигурации поставщика. Передай NULL для  _параметра lpUID_ и флага MAPI_MODIFY, если вы собираетесь внести изменения. 
    
4. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) в разделе профилей, чтобы получить свойства, необходимые поставщику для логона, например имя файла данных или таблицы баз данных. 
    
5. Убедитесь, что все свойства доступны и действительны. Если это необходимо и разрешено, отобразите диалоговое окно, чтобы побудить пользователя внести исправления или дополнения в недействительные или отсутствующие сведения, и позвоните в метод IMAPIProp::SetProps для сохранения любых изменений в разделе [IMAPIProp::SetProps.](imapiprop-setprops.md) Некоторые из распространенных свойств, которые должны быть доступны, включают: 
    
   **PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
   **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)
    
   **PR_PROVIDER_DISPLAY** [(PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)
    
   **PR_RECORD_KEY** [(PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
   > [!NOTE]
   > Не **задай PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md) **или PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName).](pidtagproviderdllname-canonical-property.md) Во время логоса эти свойства являются только для чтения. 
  
6. Если одно или несколько свойств конфигурации недоступны, сбой и возвращение значения MAPI_E_UNCONFIGURED.
    
7. Вызов [IMAPISupport::SetProviderUID для](imapisupport-setprovideruid.md) регистрации [MAPIUID](mapiuid.md). Поставщик может создать **MAPIUID по:** 
    
   - Вызов [метода IMAPISupport::NewUID.](imapisupport-newuid.md) 
    
   - Вызов средства UUIDGEN.EXE, чтобы определить GUID, который поставщик использует, чтобы включить в один из его файлов заголовки.
    
8. При желании сохраните недавно созданный **MAPIUID** в текущем профиле, назвав метод IMAPIProp::SetProps ** раздела профилей. 
    
9. Освободите раздел профилей, назвав его **метод IUnknown::Release.** 
    
10. Мгновенно установите новый объект logon и установите содержимое параметра  _lppABLogon_ по адресу этого нового объекта. 
    
Поскольку mapI может несколько раз вызывать метод ** Logon ** во время сеанса, целесообразно поддерживать эту возможность в реализации, создав несколько объектов с логотипом и отслеживая каждый созданный объект. Поддержка нескольких **вызовов Logon** позволяет пользователю клиентского приложения, например, войти в сеанс с разными удостоверениями или использовать различные назначения доставки. 
  
**Отключение** вызвано после завершения сеанса. MAPI вызывает метод [IABProvider::Shutdown](iabprovider-shutdown.md) в качестве одной из последних задач, участвующих в закрытии сеанса. MAPI выпустила все объекты логона поставщика, и, когда поставщик получает этот вызов, можно предположить, что это последний вызов, который он получит. В реализации **IABProvider::Shutdown** выполните любую окончательную очистку, которую вы считаете необходимой. Например, поставщик может вызвать **MAPIDeinitIdle,** если он вызвал **MAPIInitIdle** для использования простоя двигателя во время сеанса или метода **IUnknown::Release** любых объектов, которые еще не выпущены. 
  
Если у поставщика нет окончательной очистки, его реализация может быть выполнена из одной строки кода: 
  
```cpp
return S_OK;

```


