---
title: Открытие папки хранилища сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436540"
---
# <a name="opening-a-message-store-folder"></a>Открытие папки хранилища сообщений

**Относится к**: Outlook 2013 | Outlook 2016 
  
Перед открытием любой папки ее идентификатор записи должен быть доступен. Для большинства папок это означает, что они PR_ENTRYID **свойства.** Для специальных папок, например некоторых папок поддеревьев IPM и других корневых папок, MAPI определяет специальные свойства идентификатора записи, доступные путем вызова метода **IMAPIProp::GetProps** в хранилище сообщений. Эти идентификаторы записей всегда являются долгосрочными и именуются следующим образом: 
  
|**Folder**|**Свойство идентификатора записи**|
|:-----|:-----|
|����� ����������  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)(только класс сообщения IPM)  <br/> |
|папка "Удаленные"  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)  <br/> |
|����� �������������  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)  <br/> |
|IPM �������� �����  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId)](pidtagipmsubtreeentryid-canonical-property.md)  <br/> |
|�������� ����� ����������� ������  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)  <br/> |
|Общая корневая папка представлений  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId)](pidtagcommonviewsentryid-canonical-property.md)  <br/> |
|Корневая папка личных представлений  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)  <br/> |
|Корневая папка контактов  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId)](pidtagipmcontactentryid-canonical-property.md)  <br/> |
|Корневая папка черновиков  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId)](pidtagipmdraftsentryid-canonical-property.md)  <br/> |
|Корневая папка журнала  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId)](pidtagipmjournalentryid-canonical-property.md)  <br/> |
|Корневая папка календаря  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Корневая папка Notes  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId)](pidtagipmnoteentryid-canonical-property.md)  <br/> |
|Корневая папка задач  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId)](pidtagipmtaskentryid-canonical-property.md)  <br/> |
   
Прежде чем пытаться получить один из этих идентификаторов специальных записей, извлекаете **PR-VALID_FOLDER_MASK \_** ([PidTagValidFolderMask)](pidtagvalidfoldermask-canonical-property.md)в хранилище сообщений. **PR \_ VALID_FOLDER_MASK** это битоваяmask, которая определяет, какой из специальных идентификаторов записей существует. Для каждой специальной папки существует один бит. Если бит установлен, это означает, что соответствующая папка поддерживается и имеет допустимый идентификатор записи. Например, если папка "Удаленные" существует и имеет допустимый идентификатор записи, IPM_WASTEBASKET_VALID папки будет установлен в PR_VALID_FOLDER_MASK \_ .  
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Откройте папку, в которой размещаются все входящие сообщения определенного класса
  
1. Вызовите [IMsgStore::GetReceiveFolder,](imsgstore-getreceivefolder.md) чтобы получить идентификатор записи, установив для параметра  _lpszMessageClass_ указатель на строку символов, идентифицируя класс сообщения. Например, если вы хотите открыть "Входящие" для поддревы IPM, указать  _lpszMessageClass_ на IPM. Если вы хотите открыть папку получения сообщений IPC, установите для нее указатель на IPC. 

   Если зарегистрированная папка получения для класса сообщений не зарегистрирована, **GetReceiveFolder** выбирает папку получения, связанный класс сообщения которой соответствует самому длинному из возможных префиксов переданного класса сообщений. Дополнительные сведения см. в [папках получения MAPI.](mapi-receive-folders.md) 
   
   Обратите **внимание, PR_IPM_OUTBOX_ENTRYID** используется для открытия папки "Outbox" только для сообщений IPM. Если вы открываете папку "Outbox" для сообщений IPC, используйте вместо нее идентификатор записи для папки получения. Входящие и исходяющие сообщения IPC помещаются в папку получения. 
    
2. Вызовите один из четырех методов **OpenEntry,** чтобы открыть папку и вернуть указатель интерфейса, который можно использовать для доступа к ней. Для открытия папки можно вызвать любой из следующих методов: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   Выбор конкретного метода зависит от открываемой папки и доступных на данный момент объектов. Так как метод **IMAPISession** может открыть любую папку для любого хранения сообщений в текущем профиле, вызовите **этот метод OpenEntry,** если вы ничего не знаете о папке, которая должна быть открыта. Если вы знаете, какое хранилище сообщений принадлежит папке, и у вас есть указатель на хранилище сообщений, вызовите **IMsgStore::OpenEntry.** 
    
   Например, используйте метод **IMsgStore** для открытия папки получения. Если у вас есть указатель на объект для логотипа поставщика магазина сообщений, вызовите **IMSLogon::OpenEntry.** Так как эти вызовы проходят непосредственно к поставщику store сообщений, а не через MAPI, обработка будет быстрее. Если открываемая папка является вложенной папкой уже открытой папки, вызовите метод **IMAPIContainer::OpenEntry** для открытой папки. Метод **IMAPIContainer** открывает только вложенные папки открытой папки и является единственным методом, гарантированно работать с краткосрочными идентификаторами записей. 
    
3. Если вы хотите иметь возможность вносить изменения в папку для открытия, укажите уровень доступа, установив флаг MAPI BEST ACCESS или MAPI MODIFY в вызове \_ \_ \_ **OpenEntry.** Эти флаги являются предложениями для поставщика хранения сообщений предоставить самый высокий уровень доступа, для MAPI BEST ACCESS, или для чтения \_ и записи, для MAPI MODIFY, при открытии \_ \_ папки. 

   Так как эти флаги являются только предложениями, папка может быть открыта или не открыта с помощью нужного уровня доступа. С помощью свойства **PR_ACCESS** ([PidTagAccess)](pidtagaccess-canonical-property.md)можно определить диапазон операций, которые можно выполнить с открытой папкой. 
    
   Однако поскольку многие поставщики store сообщений вычисляют значение этого свойства по требованию, а не поддерживают его как свойство папки или в качестве столбца в таблице иерархии, его искомый процесс может потребовать много времени. Альтернативная стратегия — попытаться выполнить любую операцию и при необходимости вернуть ошибку.
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

