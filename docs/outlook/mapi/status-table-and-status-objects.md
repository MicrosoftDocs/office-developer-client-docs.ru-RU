---
title: Объекты таблицы состояния и состояния
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425178"
---
# <a name="status-table-and-status-objects"></a>Объекты таблицы состояния и состояния

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
MAPI предоставляет таблицу с сведениями о состоянии подсистемы MAPI, пулера MAPI, адресной книги или конкретного поставщика услуг. Вы можете получить доступ к этой таблице, позвонив [в IMAPISession::GetStatusTable](imapisession-getstatustable.md).
  
Каждая строка в таблице состояния представляет объект состояния, реализованный MAPI или поставщиком услуг. Вы можете использовать объект состояния для отображения листа свойств конфигурации поставщика, изменения пароля поставщика, загрузки или загрузки сообщений, а также для связи с определенным поставщиком транспорта. 
  
Существует два способа доступа к объекту состояния:
  
- Через таблицу состояния
    
- Метод **OpenStatusEntry** объекта logon 
    
Так как объекты с логотипом недоступны для клиентов, для доступа к объектам состояния необходимо использовать таблицу состояния. Подход таблицы состояния является косвенным, требующий нескольких вызовов до открытия объекта состояния и возврата указателя на реализацию **IMAPIStatus.** 
  
 **Использование таблицы состояния для открытия объекта состояния**
  
1. Вызов **IMAPIStatus::GetStatusTable,** чтобы получить [указатель IMAPITable.](imapitableiunknown.md) 
    
2. Позвоните в [IMAPITable таблицы состояния::SetColumns,](imapitable-setcolumns.md) чтобы ограничить значение столбца **PR_ENTRYID** [(PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_RESOURCE_TYPE** [(PidTagResourceType)](pidtagresourcetype-canonical-property.md)и **PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)
    
3. Ограничить представление таблицы определенным объектом состояния. Для реализации MAPI клиент может определить ограничение свойств с помощью **PR_RESOURCE_TYPE.** Для реализации поставщика услуг клиент  может ограничить PR_PROVIDER_DISPLAY [(PidTagProviderDisplay),](pidtagproviderdisplay-canonical-property.md)имя поставщика или **PR_PROVIDER_DLL_NAME** [(PidTagProviderDllName),](pidtagproviderdllname-canonical-property.md)имя файла DLL поставщика.
    
4. Вызов [IMAPITable:::Restrict,](imapitable-restrict.md) чтобы установить ограничение. 
    
5. [Вызывай hrQueryAllRows,](hrqueryallrows.md)передав структуру [SPropertyRestriction,](spropertyrestriction.md) чтобы получить строку, представляюную состояние поставщика. 
    
6. Вызов [IMAPISession::OpenEntry,](imapisession-openentry.md)указав идентификатор входа из строки таблицы состояния, чтобы открыть объект состояния и получить **указатель IMAPIStatus.** 
    
Чтобы отобразить лист свойств, вызываем метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) для целевого поставщика. **SettingsDialog** отображает лист свойств для просмотра, а в некоторых случаях изменяет свойства конфигурации поставщика. 
  
Чтобы связаться с поставщиком транспорта, позвоните по методу [IMAPIStatus::ValidateState](imapistatus-validatestate.md) объекта его состояния. **ValidateState** может перенастроить поставщика транспорта, запретить поставщику отображать пользовательский интерфейс и управлять сеансом, который включает загрузку заглавных сообщений с удаленного сервера в зависимости от флагов, которые вы передаете. Например, чтобы отменить загрузку удаленных загодеров, передайте флаг ABORT_XP_HEADER_OPERATION **в ValidateState.** Чтобы подключиться или отключиться от удаленного сервера, FORCE_XP_CONNECT или FORCE_XP_DISCONNECT. Чтобы перенастроить поставщика, передай CONFIG_CHANGED. 
  
Клиенты, реализуют отправку или получение сообщений по запросу, звонят поставщику транспорта или методу [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) mapI. В метод можно передать три флага: FLUSH_UPLOAD, FLUSH_DOWNLOAD и FLUSH_FORCE. FLUSH_UPLOAD поставщику или шпалеру MAPI отправлять любые сообщения, ожидающих в очереди вывода, а FLUSH_DOWNLOAD и поставщику или шпалеру MAPI для получения любых входящих сообщений. FLUSH_FORCE можно установить с одним из других флагов, чтобы вызвать объект состояния для выполнения флеша независимо от времени. 
  
Не ожидайте вызова **SettingsDialog** или [ChangePassword](imapistatus-changepassword.md) ни в одной из подсистем MAPI, spooler MAPI или объектов состояния адресной книги. Объекты состояния подсистемы и адресной книги поддерживают **только ValidateState;** объект состояния пульпера MAPI поддерживает **FlushQueues** в дополнение к **ValidateState.**
  
## <a name="see-also"></a>См. также



[Таблицы состояния](status-tables.md)
  
[Объекты состояния MAPI](mapi-status-objects.md)

