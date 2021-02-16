---
title: Реализация входа и входа поставщика адресной книги
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
# <a name="implementing-address-book-provider-logon-and-logoff"></a>Реализация входа и входа поставщика адресной книги

**Относится к**: Outlook 2013 | Outlook 2016 
  
Поставщики адресных книг поддерживают вход и вход в сеанс, реализуя методы интерфейса [IABProvider : IUnknown.](iabprovideriunknown.md) Интерфейс ** IABProvider ** наследуется непосредственно от **IUnknown** и добавляет только два других метода: **Logon** и **Shutdown**. 
  
## <a name="logoff"></a>Logoff

MAPI будет вызывать метод [IABProvider::Logon](iabprovider-logon.md) поставщика в начале каждого сеанса и каждый раз, когда поставщик добавляется в текущий профиль и клиент поддерживает динамическую перенастройку. Когда MAPI вызывает метод **IABProvider::Logon,** поставщик адресной книги начинает процесс его работы. 
  
**Реализация IABProvider::Log**
  
1. Инициализировать все указатели выходных параметров, переданные MAPI. 
    
2. Вызовите метод **IUnknown::AddRef** объекта поддержки, чтобы добавить его количество ссылок. 
    
3. Вызовите метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) объекта поддержки, чтобы открыть раздел профиля, содержащий сведения о конфигурации поставщика. Передав NULL для  _параметра lpUID_ и MAPI_MODIFY флага, если вы собираетесь внести изменения. 
    
4. Вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) раздела профиля, чтобы получить свойства, необходимые поставщику для работы с данными, например имя файла данных или таблицы базы данных. 
    
5. Убедитесь, что все свойства доступны и действительны. Если необходимо и разрешено, вы можете отобразить диалоговое окно с запросом на внесение исправлений или дополнений в недопустимые или отсутствующие сведения, а также вызвать метод [IMAPIProp::SetProps](imapiprop-setprops.md) раздела профиля, чтобы сохранить изменения. Некоторые из общих свойств, которые должны быть доступны: 
    
   **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)
    
   **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)
    
   **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay)](pidtagproviderdisplay-canonical-property.md)
    
   **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)
    
   > [!NOTE]
   > Не **задав PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md) **или PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName).](pidtagproviderdllname-canonical-property.md) Во время logon эти свойства являются только для чтения. 
  
6. Если одно или несколько свойств конфигурации недоступны, сбой и возврат значения MAPI_E_UNCONFIGURED.
    
7. Вызов [IMAPISupport::SetProviderUID для](imapisupport-setprovideruid.md) регистрации [MAPIUID](mapiuid.md). Поставщик может создать **MAPIUID** с помощью: 
    
   - Вызов метода [IMAPISupport::NewUID.](imapisupport-newuid.md) 
    
   - Вызов средства UUIDGEN.EXE для определения GUID, который поставщик использует для включаемого в один из файлов его заголовок.
    
8. При желании сохраните только что созданный **MAPIUID** в текущем профиле, вызывая метод ** IMAPIProp::SetProps ** раздела профиля. 
    
9. Освободите раздел профиля, вызывая его метод **IUnknown::Release.** 
    
10. Создать новый объект для логотипа и установить для содержимого параметра  _lppABLogon_ адрес этого нового объекта. 
    
Так как MAPI может вызвать метод ** Logon ** несколько раз во время сеанса, целесообразно поддерживать эту возможность в реализации, создав несколько объектов для логотипа и отслеживая каждый созданный объект. Поддержка **нескольких вызовов** входа позволяет пользователю клиентского приложения, например, войти в сеанс с разными удостоверениями или использовать разные места доставки. 
  
**Завершение работы** происходит после завершения сеанса. MAPI вызывает метод [IABProvider::Shutdown](iabprovider-shutdown.md) как одну из последних задач, которые связаны с завершением сеанса. MAPI выпустила все объекты для работы с вашим поставщиком и, когда поставщик получает этот вызов, он может предположить, что это последний вызов, который он получит. В реализации **IABProvider::Shutdown** выполните окончательную очистку, которую вы считаете необходимой. Например, поставщик может вызвать **MAPIDeinitIdle,** если он вызвал **MAPIInitIdle,** чтобы использовать обработчик бездействия во время сеанса, или метод **IUnknown::Release** любых объектов, которые еще не были отпущены. 
  
Если у поставщика нет окончательной очистки, его реализация может быть состоит из одной строки кода: 
  
```cpp
return S_OK;

```


