---
title: Таблица и объекты состояний
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 774aaea0365066981b9d6426a2579160f6578844
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812385"
---
# <a name="status-table-and-status-objects"></a>Таблица и объекты состояний

  
  
**Относится к**: Outlook 
  
MAPI таблица со сведениями о состоянии в подсистеме MAPI, диспетчер очереди MAPI, адресной книги или поставщик конкретной службы. Можно получить доступ к этой таблице путем вызова [IMAPISession::GetStatusTable](imapisession-getstatustable.md).
  
Каждой строки в таблице состояния представляет собой объект состояния, реализован MAPI или поставщика услуг. Чтобы открыть окно свойств конфигурации поставщика, чтобы изменить пароль поставщика, для отправки или загрузки сообщений и способ связи с помощью поставщика транспорта определенного можно использовать объект состояния. 
  
Существует два способа для доступа к объекту состояние:
  
- В таблице состояния
    
- Через метод **OpenStatusEntry** объекта входа в систему 
    
Так как вход в систему объекты недоступны для клиентов, необходимо использовать в таблице состояния для доступа к объектам состояние. Подход в таблице состояния ДВССЫЛ, требуя несколько вызовов перед открыть объект состояния и возвращается указатель на его реализации **IMAPIStatus** . 
  
 **Использовать таблицу состояния для открытия объект состояния**
  
1. Вызов **IMAPIStatus::GetStatusTable** для извлечения указатель [IMAPITable](imapitableiunknown.md) . 
    
2. Вызовите метод [IMAPITable::SetColumns](imapitable-setcolumns.md) в таблице состояния для ограничения в столбце, задайте значение **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) и **PR_DISPLAY_NAME** ([ PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Ограничение в табличном представлении объект определенное состояние. Для реализации интерфейса MAPI клиента можно задать ограничение свойства, с помощью **PR_RESOURCE_TYPE**. Для реализации поставщика службы можно ограничить клиента на **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), имя поставщика, или на **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), имя DLL-Библиотеки поставщика файл.
    
4. Вызовите [IMAPITable::Restrict](imapitable-restrict.md) , чтобы задать ограничение. 
    
5. Вызовите [HrQueryAllRows](hrqueryallrows.md), передав в структуре [SPropertyRestriction](spropertyrestriction.md) , чтобы получить строку, представляющую состояние поставщика. 
    
6. Вызовите [IMAPISession::OpenEntry](imapisession-openentry.md), указания идентификатора запись из строки состояния таблицы, для открытия объекта состояния и получить указатель **IMAPIStatus** . 
    
Чтобы открыть окно свойств, вызов метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) состояние объекта для целевого поставщика. **SettingsDialog** отображает окно свойств для просмотра и в некоторых случаях изменение свойств конфигурации поставщика. 
  
Для взаимодействия с помощью поставщика транспорта, вызовите метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) его состояние объекта. **ValidateState** можно повторно настройте поставщика транспорта, запретить отображение пользовательского интерфейса поставщика и управление сеансом, включающей загрузку заголовков сообщений с удаленного сервера, в зависимости от флаги, переданных в. Например Отмена загрузки удаленного заголовки, передайте флаг ABORT_XP_HEADER_OPERATION **ValidateState**. Подключение или отключение от удаленного сервера, передайте FORCE_XP_CONNECT или FORCE_XP_DISCONNECT. Чтобы изменить поставщик, передайте CONFIG_CHANGED. 
  
Клиенты, которые реализуют отправку и получение сообщений по запросу вызов метода [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) поставщика транспорта или диспетчер очереди MAPI. Три флага можно передать в метод: FLUSH_UPLOAD, FLUSH_DOWNLOAD и FLUSH_FORCE. FLUSH_UPLOAD указывает, что поставщик или диспетчер очереди MAPI, чтобы отправить все сообщения, ожидающие в очереди вывода во время FLUSH_DOWNLOAD указывает поставщик или диспетчер очереди MAPI принимать входящие сообщения. FLUSH_FORCE может иметь значение с помощью одной из других флаги привести объект состояние для выполнения очистки независимо от времени. 
  
Не ожидается мог вызывать **SettingsDialog** или [Изменение пароля](imapistatus-changepassword.md) на подсистему MAPI, диспетчер очереди MAPI или адресной книги состояние объектов. Адрес и подсистемы объекты состояния книги поддерживают только **ValidateState**; объект состояния очереди MAPI поддерживает **FlushQueues** в дополнение к **ValidateState**.
  
## <a name="see-also"></a>См. также



[Таблицы состояния](status-tables.md)
  
[Объекты состояния MAPI](mapi-status-objects.md)

