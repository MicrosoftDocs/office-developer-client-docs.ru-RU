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
ms.openlocfilehash: 2ac4a30d6afc7e5245441bfe2d501169dd3a9447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586125"
---
# <a name="opening-a-message-store-folder"></a>Открытие папки хранилища сообщений

**Применимо к**: Outlook 2013 | Outlook 2016 
  
Прежде чем можно открыть любой папке, его идентификатор записи должны быть доступны. Для большинства папок это означает, извлечение их свойств **PR_ENTRYID** . Для специальных папок, таких как некоторые из папки поддерева IPM и другие корневой папки MAPI определяет свойства идентификатор специальные запись, доступных пользователям, вызвав метод **IMAPIProp::GetProps** хранилища сообщений. Следующие идентификаторы записей, всегда долгосрочного и имеют следующим образом: 
  
|**Folder**|**Свойство идентификатора записи**|
|:-----|:-----|
|����� ����������  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (Только для класса сообщений IPM)  <br/> |
|����� "���������"  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|����� �������������  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM �������� �����  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|�������� ����� ����������� ������  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|Общие представления корневой папки  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|Корневой папки личными представлениями  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|Корневой папки Контакты  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|Корневой папке «Черновики»  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|Корневой папки журнала  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|Корневой папки календаря  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Заметки о корневой папки  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|Задачи корневой папки  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
Перед попыткой получить один из этих идентификаторов специальные запись извлечения **связей с Общественностью\_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) свойство хранилища сообщений. **Связей с Общественностью\_VALID_FOLDER_MASK** является битовой маской, который определяет, какой из специальных запись существует идентификаторы. Существует один бит для каждого из специальных папок. Если бит задан, он указывает, что соответствующую папку поддерживается и имеет идентификатор записей. Например, если папки «Удаленные» существует и имеет идентификатор записей, папка\_IPM_WASTEBASKET_VALID бит будет установлен в **PR_VALID_FOLDER_MASK**. 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>Откройте папку, где помещаются все входящие сообщения определенного класса
  
1. Вызов [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) для получения его идентификатор записи, для параметра _lpszMessageClass_ для указания на строку символов, идентифицирующий класс сообщения. Например если требуется открыть папку "Входящие" для вашей поддерева IPM пункты _lpszMessageClass_ IPM. Чтобы открыть папку получения сообщений производственных Издержек, установите его для указания на производственных Издержек. 

   Если папка не зарегистрирован получения для класса сообщений, **GetReceiveFolder** выберет переданную папку получения которого класс связанного сообщения соответствует длинным возможные префикс класса сообщений. Дополнительные сведения можно [Получить папки MAPI](mapi-receive-folders.md). 
   
   Обратите внимание на то, что свойство **PR_IPM_OUTBOX_ENTRYID** используется для открытия папке Исходящие только для сообщений IPM. При открытии исходящие сообщения производственных Издержек, вместо этого использовать идентификатор записи для его получения папки. Входящие и исходящие сообщения производственных Издержек, помещаются в папку получения. 
    
2. Вызов одного из четырех способов **OpenEntry** откройте папку и возвращает указатель интерфейса, которые можно использовать для доступа к нему. Можно вызвать любой из следующих методов, чтобы открыть папку: 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   Выбор конкретного метода зависит от папки для открытия и объекты, которые доступны во время. Так как метод **IMAPISession** можно открыть любой папки для любого хранилища сообщений в текущий профиль, вызовите этот **OpenEntry** , если вы не знаете никаких сведений о папке, чтобы открыть. Если вы знаете, какие хранилища сообщений несет ответственность за папке и иметь указатель для хранилища сообщений, вызовите **IMsgStore::OpenEntry**. 
    
   Например используйте метод **IMsgStore** откройте папку получения. Если у вас есть указатель на объект входа поставщика хранилища сообщений, вызовите **IMSLogon::OpenEntry**. Так как эти вызовы перейти непосредственно к поставщику хранилища сообщений, а не через MAPI, обработка выполняется быстрее. Если к папке, которая открывается вложенной папки, которые уже открыты, вызовите метод **IMAPIContainer::OpenEntry** открыть папку. Метод **IMAPIContainer** только открывает вложенные папки в настоящее время открыт и единственный метод гарантированно работать с краткосрочных идентификаторы записей. 
    
3. Если требуется внести изменения в папке, чтобы открыть задать уровень доступа, задав либо MAPI\_НАИБОЛЕЕ\_доступа или MAPI\_флаг изменения в вызове **OpenEntry** . Эти флаги имеют предложения для поставщика хранилища сообщений для предоставления высший уровень доступа, для MAPI\_НАИБОЛЕЕ\_доступ или доступ на чтение/запись, для MAPI\_изменения, при открытии в папку. 

   Так как эти флаги не только предложения, папка или не удается открыть с уровнем доступа, который предполагается, что. Извлекая свойство **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)), можно определить диапазон операций, которые могут быть выполнены на открыть папку. 
    
   Тем не менее так как многие поставщики хранилища сообщений вычисление значения для этого свойства на запросами, а не поддерживать его как свойство папку или на столбец в таблице их иерархии, его получения может быть занимать много времени. Альтернативный способ — это попытаться любые операции, необходимые для выполнения и возвращает ошибку, если это необходимо.
    
## <a name="see-also"></a>См. также

- [Каноническое свойство PidTagEntryId](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

