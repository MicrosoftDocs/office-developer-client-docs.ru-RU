---
title: Таблица состояния и объекты состояния
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
# <a name="status-table-and-status-objects"></a>Таблица состояния и объекты состояния

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
MAPI предоставляет таблицу с информацией о состоянии подсистемы MAPI, пула MAPI, адресной книги или определенного поставщика услуг. Вы можете получить доступ к этой таблице, вызывая [IMAPISession::GetStatusTable.](imapisession-getstatustable.md)
  
Каждая строка в таблице состояния представляет объект состояния, реализованный MAPI или поставщиком услуг. Объект состояния можно использовать для отображения таблицы свойств конфигурации поставщика, изменения пароля поставщика, отправки или загрузки сообщений, а также для связи с определенным поставщиком транспорта. 
  
Существует два способа доступа к объекту состояния:
  
- С помощью таблицы состояния
    
- С помощью метода **OpenStatusEntry** объекта для логотипа 
    
Так как объекты для входов недоступны клиентам, для доступа к объектам состояния необходимо использовать таблицу состояния. Подход к таблице состояния является косвенным и требует нескольких вызовов перед открытием объекта состояния и возвратом указателя на его реализацию **IMAPIStatus.** 
  
 **Использование таблицы состояния для открытия объекта состояния**
  
1. Вызовите **IMAPIStatus::GetStatusTable,** чтобы получить [указатель IMAPITable.](imapitableiunknown.md) 
    
2. Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) таблицы состояния, чтобы ограничить значение столбца **PR_ENTRYID** ([PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_RESOURCE_TYPE** ([PidTagResourceType)](pidtagresourcetype-canonical-property.md)и **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)
    
3. Ограничив представление таблицы определенным объектом состояния. Для реализации MAPI клиент может определить ограничение свойств с **помощью PR_RESOURCE_TYPE.** Для реализации поставщиков услуг клиент может ограничить PR_PROVIDER_DISPLAY **(** [PidTagProviderDisplay),](pidtagproviderdisplay-canonical-property.md)имя поставщика или **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName),](pidtagproviderdllname-canonical-property.md)имя DLL-файла поставщика.
    
4. Вызов [IMAPITable::Restrict,](imapitable-restrict.md) чтобы установить ограничение. 
    
5. Вызовите [HrQueryAllRows,](hrqueryallrows.md)передав структуру [SPropertyRestriction,](spropertyrestriction.md) чтобы получить строку, представляюную состояние поставщика. 
    
6. Вызовите [IMAPISession::OpenEntry,](imapisession-openentry.md)указав идентификатор записи из строки таблицы состояния, чтобы открыть объект состояния и получить **указатель IMAPIStatus.** 
    
Чтобы отобразить лист свойств, вызовите метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) объекта состояния для целевого поставщика. **SettingsDialog** отображает лист свойств для просмотра и, в некоторых случаях, изменение свойств конфигурации поставщика. 
  
Для связи с поставщиком транспорта вызовите метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) объекта состояния. **ValidateState** может перенастроить поставщика транспорта, запретить ему отображение пользовательского интерфейса и управлять сеансом, который включает загрузку сообщений с удаленного сервера в зависимости от флагов, которые вы передаете. Например, чтобы отменить загрузку удаленных headers, передайте флаг ABORT_XP_HEADER_OPERATION **validateState.** Чтобы подключиться к удаленному серверу или отключиться от него, FORCE_XP_CONNECT или FORCE_XP_DISCONNECT. Чтобы перенастроить поставщика, передав CONFIG_CHANGED. 
  
Клиенты, которые реализуют отправку или получение сообщений по требованию, звонят либо к поставщику транспорта, либо к методу [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) поставщика транспорта или пула MAPI. В метод можно передать три флага: FLUSH_UPLOAD, FLUSH_DOWNLOAD и FLUSH_FORCE. FLUSH_UPLOAD поставщика или пула MAPI отправлять все сообщения, ожидающих в очереди вывода, а FLUSH_DOWNLOAD предписывает поставщику или пуле MAPI получать любые входящие сообщения. FLUSH_FORCE можно установить с помощью любого из других флагов, чтобы объект состояния выполнял очистку независимо от времени. 
  
Не ожидайте вызова **SettingsDialog** или [ChangePassword](imapistatus-changepassword.md) ни в одной из подсистем MAPI, пула MAPI или объектов состояния адресной книги. Объекты состояния подсистемы и адресной книги поддерживают **только ValidateState;** Объект состояния пула MAPI поддерживает **FlushQueues** в дополнение к **ValidateState.**
  
## <a name="see-also"></a>См. также



[Таблицы состояния](status-tables.md)
  
[Объекты состояния MAPI](mapi-status-objects.md)

