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
ms.openlocfilehash: d612738ef8bf0e6925d89a5be7cb423695672d28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422364"
---
# <a name="status-tables"></a>Таблицы состояния

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица состояния содержит сведения о состоянии текущего сеанса. Для каждого сеанса MAPI существует одна таблица состояния, включаемая сведения, предоставляемые MAPI и поставщиками услуг. MAPI предоставляет данные для трех строк: строки для подсистемы MAPI, строки для пула MAPI и строки для интегрированной адресной книги. Так как поставщики транспорта должны предоставить сведения о состоянии в таблицу состояния, для каждого активного поставщика транспорта существует одна строка. Поставщики адресной книги и магазина сообщений могут выбрать, следует ли поддерживать таблицу состояния. 
  
Так как каждая строка предоставляется разными ресурсами, набор столбцов может отличаться в зависимости от строки. Существует набор столбцов, которые должен предоставить каждый объект состояния, и набор столбцов, поставляемого MAPI. Поставщик службы может добавить в эти наборы, чтобы получить доступ к свойствам конкретного поставщика. Например, поставщики хранилищ сообщений могут добавить PR_STORE_RECORD_KEY **(** [PidTagStoreRecordKey),](pidtagstorerecordkey-canonical-property.md)чтобы предоставить клиентам идентификатор их хранилищ сообщений. Клиенты должны иметь расширенные знания о наличии этих дополнительных сведений, чтобы иметь возможность использовать их. 
  
В следующей таблице перечислены свойства, которые должны быть указаны в каждой строке таблицы состояния. Реализутель объекта состояния предоставляет некоторые свойства; другие вычисляются с помощью MAPI.
  
|**Свойства, предоставляемые объектом состояния**|**Свойства, предоставляемые MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode)](pidtagstatuscode-canonical-property.md)  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType)](pidtagresourcetype-canonical-property.md)  <br/> |
   
Если объект состояния предоставляет удостоверение, он должен установить **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay),](pidtagidentitydisplay-canonical-property.md) **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId)](pidtagidentityentryid-canonical-property.md)и **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey),](pidtagidentitysearchkey-canonical-property.md)а также включить эти свойства в таблицу. 
  
MAPI вычисляет четыре свойства для каждой строки таблицы состояния:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |**PR_ROWID** ([PidTagRowid)](pidtagrowid-canonical-property.md)  <br/> |
   
MAPI назначает идентификатор записи строке состояния, чтобы позволить клиентам открывать соответствующий объект состояния. Идентификатор строки также назначен для идентификации строки в таблице в качестве ключа экземпляра для идентификации данных в объекте состояния. Свойству **PR_OBJECT_TYPE** установлено MAPI_STATUS. 
  
Чтобы получить доступ к таблице состояния, клиенты вызвать метод [IMAPISession::GetStatusTable.](imapisession-getstatustable.md) Этот вызов не следует делать сразу после запуска. Это необходимо, так как **GetStatusTable** должен дождаться инициализации поставщиков транспорта пулом MAPI— операции, отложенной до завершения клиентского имени. **GetStatusTable** — относительно быстрый вызов после завершения обработки запуска пулом MAPI. 
  
Сведения о таблице состояния можно использовать различными способами, например для доступа к объекту состояния, для определения того, работает ли клиент в подключенном или автономном режиме, а также для отслеживания состояния поставщика. Например, клиенты могут открыть объект состояния определенного поставщика услуг, **передав** значение свойства PR_ENTRYID [методу IMAPISession::OpenEntry.](imapisession-openentry.md) Объект состояния поддерживает интерфейс **IMAPIStatus,** интерфейс, содержащий методы для изменения пароля поставщика службы, очистки очереди сообщений, отображения таблицы свойств конфигурации или подтверждения состояния непосредственно у поставщика. Сведения о таблице состояния также можно использовать для создания диалоговых окно для информирования клиентов о ходе выполнения длительной операции. 
  
Поставщики услуг, которые поддерживают таблицу состояния, используют метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) для создания и обновления строки. При изменении строки все объекты приемника, зарегистрированные для получения уведомлений таблицы состояния, должны быть уведомлены. Поставщики услуг могут вызывать метод [IMAPISupport::Notify,](imapisupport-notify.md) если они используют службную службу уведомлений MAPI, или вызывать метод [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) каждого приемника рекомендации напрямую. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

