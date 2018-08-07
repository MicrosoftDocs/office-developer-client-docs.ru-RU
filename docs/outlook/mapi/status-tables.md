---
title: Таблицы состояния
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: afbef333af46051284fa51d52c2e3f77607b0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812393"
---
# <a name="status-tables"></a>Таблицы состояния

  
  
**Относится к**: Outlook 
  
Состояние таблица содержит сведения, относящиеся к состоянию текущего сеанса. Существует одна таблица состояния для каждого сеанса MAPI, который содержит сведения, представленные с MAPI и поставщиками услуг. MAPI предоставляет данные для трех строк: строки подсистемы MAPI, строку для очереди MAPI и строку для встроенной адресной книги. Так как поставщиками транспорта необходимы для предоставления сведений о состоянии в таблице состояния, имеется одна строка для каждого поставщика транспорта активный. Поставщиков хранилища адресной книги и сообщения можно выбрать для поддержки в таблице состояния. 
  
Поскольку каждую строку обеспечивается на другой ресурс, наборы столбцов, может меняться в зависимости от строки к строке. Имеется набор столбцов, каждый объект состояние необходимость предоставить и набор столбцов, которые предоставляет MAPI. Поставщик службы можно добавить в эти наборы для предоставления поставщика свойства этого элемента управления. Например поставщиков хранилища сообщений добавить **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) для предоставления клиентам с идентификатором их хранилища сообщений. Клиенты должны иметь знания предварительное существование эти дополнительные данные, чтобы иметь возможность использовать его. 
  
В следующей таблице приведены свойства, которые должны быть в каждой строки в таблице состояния. Разработчик объект состояния предоставляет ряд свойств; другие пользователи вычисляются с MAPI.
  
|**Свойства, предоставленные объектом состояния**|**Свойства, предоставляемые MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Если объект состояния предоставляет удостоверение, его следует задать **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) и **PR_IDENTITY_SEARCH_KEY** ([ PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) и включить эти свойства в таблице. 
  
Четыре свойства вычисляются по MAPI для каждой строки в таблице состояния:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI назначает идентификатор записи в строке состояния, чтобы разрешить клиентам для открытия соответствующего объекта состояния. Для идентификации строки в таблице, — это ключ на экземпляр для определения данных в объекте состояния также назначается идентификатор строки. Свойство **PR_OBJECT_TYPE** имеет значение MAPI_STATUS. 
  
Для доступа к таблице состояния, клиенты вызовите метод [IMAPISession::GetStatusTable](imapisession-getstatustable.md) . Этот вызов, не следует делать сразу же после запуска. Это, поскольку **GetStatusTable** должен ожидать в очереди MAPI для инициализации поставщиками транспорта, операция откладывается до того времени, после его входа клиента. **GetStatusTable** является относительно быстрой звонок после завершения обработки запуска диспетчера очереди MAPI. 
  
Сведения о состоянии в таблице можно использовать различными способами, например, для доступа к объекту состояния, для определения выполнения клиента в подключенных и интерактивном режимах и отслеживать состояние поставщика. К примеру клиентов можно открыть объект состояние определенной службы поставщика, передав значение свойства **PR_ENTRYID** в метод [IMAPISession::OpenEntry](imapisession-openentry.md) . Объект состояния поддерживает интерфейс **IMAPIStatus** , интерфейс, который содержит методы, позволяющие изменить пароль поставщика службы, очистка очереди сообщений, откройте окно свойств конфигурации или подтверждение с поставщиком непосредственно. Также сведения о состоянии в таблице можно использовать для построения диалоговое окно для информирования клиентов о ходе выполнения длительной операции. 
  
Поставщики услуг, которые поддерживают в таблице состояния используйте метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) для создания и обновления их строки. При каждом изменении их строки все уведомить приемник объекты, зарегистрированные для получения уведомления о состоянии в таблице должны получать уведомления. Поставщиков услуг можно вызвать метод [IMAPISupport::Notify](imapisupport-notify.md) , если они являются с помощью служебной программы уведомлений MAPI или непосредственно вызовите метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) каждый приемник уведомлений. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

