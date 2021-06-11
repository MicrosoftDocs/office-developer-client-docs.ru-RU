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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице состояния содержатся сведения, касающиеся состояния текущего сеанса. Для каждого сеанса MAPI существует одна таблица состояния, включаемая сведения, предоставляемые MAPI и поставщиками услуг. MAPI предоставляет данные для трех строк: строка для подсистемы MAPI, строка для пулера MAPI и строка для интегрированной адресной книги. Поскольку поставщики транспорта обязаны поставлять сведения о состоянии в таблицу состояния, для каждого активного поставщика транспорта имеется одна строка. Поставщики адресной книги и магазина сообщений могут выбрать, следует ли поддерживать таблицу состояния. 
  
Поскольку каждая строка предоставляется другим ресурсом, набор столбцов может отличаться от строки к строке. Существует набор столбцов, которые необходимо предоставить каждому объекту состояния, и набор столбцов, которые поставляет MAPI. Поставщик услуг может добавить в эти наборы, чтобы раскрыть свойства, определенные для конкретного поставщика. Например, поставщики магазинов **сообщений** могут добавить PR_STORE_RECORD_KEY [(PidTagStoreRecordKey),](pidtagstorerecordkey-canonical-property.md)чтобы предоставить клиентам идентификатор магазина сообщений. Клиенты должны заранее знать о существовании этой дополнительной информации, чтобы иметь возможность ее использовать. 
  
В следующей таблице перечислены свойства, которые должны быть в каждой строке таблицы состояния. Реализутель объекта состояния предоставляет некоторые свойства; другие вычисляются MAPI.
  
|**Свойства, предоставляемые объектом состояния**|**Свойства, предоставляемые MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName)](pidtagproviderdllname-canonical-property.md)  <br/> |
|**PR_STATUS_CODE** [(PidTagStatusCode)](pidtagstatuscode-canonical-property.md)  <br/> |**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |
|**PR_RESOURCE_METHODS** [(PidTagResourceMethods)](pidtagresourcemethods-canonical-property.md)  <br/> |**PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)  <br/> |
   
Если объект состояния предоставляет удостоверение, он должен задать **PR_IDENTITY_DISPLAY** [(PidTagIdentityDisplay),](pidtagidentitydisplay-canonical-property.md) **PR_IDENTITY_ENTRYID** [(PidTagIdentityEntryId)](pidtagidentityentryid-canonical-property.md)и **PR_IDENTITY_SEARCH_KEY** [(PidTagIdentitySearchKey)](pidtagidentitysearchkey-canonical-property.md)и включить эти свойства в таблицу. 
  
Четыре свойства вычисляются MAPI для каждой строки таблицы состояния:
  
|||
|:-----|:-----|
|**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)  <br/> |**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |
|**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |**PR_ROWID** [(PidTagRowid)](pidtagrowid-canonical-property.md)  <br/> |
   
MAPI назначает идентификатор входа в строку состояния, чтобы клиенты могли открыть соответствующий объект состояния. Идентификатор строки также назначен для определения строки в таблице, как ключ экземпляра для идентификации данных в объекте состояния. Свойство **PR_OBJECT_TYPE** установлено для MAPI_STATUS. 
  
Чтобы получить доступ к таблице состояния, клиенты звонят по [методу IMAPISession::GetStatusTable.](imapisession-getstatustable.md) Этот вызов не следует делать сразу после запуска. Это потому, что **GetStatusTable** должен ждать, пока пуллер MAPI инициализирует поставщиков транспорта, операция, которая отложена до завершения клиентом своего логотипа. **GetStatusTable** — это относительно быстрый вызов после завершения обработки запуска пулером MAPI. 
  
Сведения о таблице состояния можно использовать различными способами, например для доступа к объекту состояния, для определения того, работает ли клиент в подключенном или автономном режиме, а также для мониторинга состояния поставщика. Например, клиенты могут открыть объект состояния конкретного поставщика **услуг, передав** значение свойства [PR_ENTRYID методу IMAPISession::OpenEntry.](imapisession-openentry.md) Объект состояния поддерживает интерфейс **IMAPIStatus,** интерфейс, содержащий методы изменения пароля поставщика услуг, очистки очереди сообщений, отображения листа свойств конфигурации или подтверждения состояния непосредственно у поставщика. Сведения о состоянии таблицы также можно использовать для создания диалоговое окно для информирования клиентов о ходе длительной операции. 
  
Поставщики услуг, поддерживаювшие таблицу состояния, используют метод [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) для создания и обновления строки. Всякий раз, когда происходит изменение строки, все объекты раковины, зарегистрированные для получения уведомлений таблицы состояния, должны быть уведомлены. Поставщики услуг могут вызывать метод [IMAPISupport::Notify,](imapisupport-notify.md) если они используют утилиту уведомлений MAPI или звонят каждый из них по рекомендации метода [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) напрямую. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

