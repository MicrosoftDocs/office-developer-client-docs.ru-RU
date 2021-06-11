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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Перед открытием любой папки должен быть доступен ее идентификатор записи. Для большинства папок это означает повторное PR_ENTRYID **свойств.** Для специальных папок, например некоторых папок подтримки IPM и других корневых папок, MAPI определяет специальные свойства идентификатора записи, доступные путем вызова метода **IMAPIProp::GetProps** магазина сообщений. Эти идентификаторы записи всегда являются долгосрочными и называются следующим образом: 
  
|**Folder**|**Свойство идентификатора входа**|
|:-----|:-----|
|����� ����������  <br/> |**PR_IPM_OUTBOX_ENTRYID** [(PidTagIpmOutboxEntryId)](pidtagipmoutboxentryid-canonical-property.md)(только класс сообщений IPM)  <br/> |
|папка "Удаленные"  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** [(PidTagIpmWastebasketEntryId)](pidtagipmwastebasketentryid-canonical-property.md)  <br/> |
|����� �������������  <br/> |**PR_IPM_SENTMAIL_ENTRYID** [(PidTagIpmSentMailEntryId)](pidtagipmsentmailentryid-canonical-property.md)  <br/> |
|IPM �������� �����  <br/> |**PR_IPM_SUBTREE_ENTRYID** [(PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|�������� ����� ����������� ������  <br/> |**PR_FINDER_ENTRYID** [(PidTagFinderEntryId)](pidtagfinderentryid-canonical-property.md)  <br/> |
|Общие представления корневой папки  <br/> |**PR_COMMON_VIEWS_ENTRYID** [(PidTagCommonViewsEntryId)](pidtagcommonviewsentryid-canonical-property.md)  <br/> |
|Корневая папка личных представлений  <br/> |**PR_VIEWS_ENTRYID** [(PidTagViewsEntryId)](pidtagviewsentryid-canonical-property.md)  <br/> |
|Корневая папка контактов  <br/> |**PR_IPM_CONTACT_ENTRYID** [(PidTagIpmContactEntryId)](pidtagipmcontactentryid-canonical-property.md)  <br/> |
|Корневая папка черновиков  <br/> |**PR_IPM_DRAFTS_ENTRYID** [(PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Корневая папка журнала  <br/> |**PR_IPM_JOURNAL_ENTRYID** [(PidTagIpmJournalEntryId)](pidtagipmjournalentryid-canonical-property.md)  <br/> |
|Корневая папка календаря  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** [(PidTagIpmAppointmentEntryId)](pidtagipmappointmententryid-canonical-property.md)  <br/> |
|Корневая папка Notes  <br/> |**PR_IPM_NOTE_ENTRYID** [(PidTagIpmNoteEntryId)](pidtagipmnoteentryid-canonical-property.md)  <br/> |
|Корневая папка задач  <br/> |**PR_IPM_TASK_ENTRYID** [(PidTagIpmTaskEntryId)](pidtagipmtaskentryid-canonical-property.md)  <br/> |
   
Прежде чем попытаться получить один из этих специальных идентификаторов записи, **\_ VALID_FOLDER_MASK** pr [(PidTagValidFolderMask)](pidtagvalidfoldermask-canonical-property.md)свойство магазина сообщений. **PR \_ VALID_FOLDER_MASK** — это битмаска, которая определяет, какие из специальных идентификаторов записи существуют. Существует один бит для каждой из специальных папок. Если бит за установлен, он указывает, что соответствующая папка поддерживается и имеет допустимый идентификатор записи. Например, если папка "Удаленные элементы" существует и имеет допустимый идентификатор записи, IPM_WASTEBASKET_VALID папка будет PR_VALID_FOLDER_MASK \_ .  
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Откройте папку, в которой размещаются все входящие сообщения определенного класса
  
1. Вызов [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) для получения идентификатора записи, задан параметр  _lpszMessageClass,_ указывающий на строку символов, определяющий класс сообщения. Например, если вы хотите открыть почтовый ящик для подтрия IPM, указать  _lpszMessageClass_ в IPM. Если вы хотите открыть папку получения сообщений IPC, установите ее в точку IPC. 

   Если для класса сообщений не зарегистрирована папка получения, **GetReceiveFolder** выбирает папку получения, связанная с классом сообщений, которая соответствует максимально возможной префиксу пройденного класса сообщений. Дополнительные сведения см. в [папках MAPI Receive.](mapi-receive-folders.md) 
   
   Обратите внимание, **PR_IPM_OUTBOX_ENTRYID** используется для открытия папки "Избокс" только для сообщений IPM. Если вы открываете почтовый ящик для сообщений IPC, используйте вместо него идентификатор записи для его папки получения. Входящие и исходяющие сообщения IPC размещаются в папке получения. 
    
2. Вызов одного из четырех методов **OpenEntry,** чтобы открыть папку и вернуть указатель интерфейса, который можно использовать для доступа к ней. Чтобы открыть папку, можно вызвать любой из следующих методов: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   Выбор определенного метода зависит от открываемой папки и доступных в данный момент объектов. Так как метод **IMAPISession** может открыть любую папку для любого магазина сообщений в текущем профиле, позвоните этому **OpenEntry,** если вы ничего не знаете об открываемой папке. Если вы знаете, какой магазин сообщений владеет папкой и у вас есть указатель в хранилище сообщений, позвоните **в IMsgStore::OpenEntry**. 
    
   Например, используйте метод **IMsgStore** для открытия папки получения. Если у вас есть указатель на объект logon поставщика магазина сообщений, позвоните **по телефону IMSLogon::OpenEntry**. Поскольку эти вызовы идут непосредственно к поставщику магазина сообщений, а не через MAPI, обработка будет проходить быстрее. Если открываемая папка является подмостком уже открытой папки, позвоните в **метод IMAPIContainer::OpenEntry** открытой папки. Метод **IMAPIContainer** открывает только подмостки открытой папки и является единственным методом, гарантируемым для работы с краткосрочными идентификаторами записи. 
    
3. Если вы хотите внести изменения в открываемую папку, укажите уровень доступа, установив флаг MAPI BEST ACCESS или MAPI MODIFY в \_ \_ \_ **вызове OpenEntry.** Эти флаги являются предложениями поставщику магазина сообщений предоставить самый высокий уровень доступа для MAPI BEST ACCESS или для чтения и записи для MAPI MODIFY при открытии \_ \_ \_ папки. 

   Поскольку эти флаги являются только предложениями, папка может открываться или не открываться с ожидаемом уровнем доступа. С помощью PR_ACCESS **свойства** [PidTagAccess](pidtagaccess-canonical-property.md)можно определить диапазон операций, которые можно выполнить в открытой папке. 
    
   Однако, поскольку многие поставщики магазинов сообщений вычисляют значение для этого свойства по требованию, а не поддерживают его в качестве свойства папки или столбца в таблице иерархии, его истощение может потребовать много времени. Альтернативной стратегией является попытка любой операции, необходимой для выполнения и при необходимости возврата ошибки.
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

