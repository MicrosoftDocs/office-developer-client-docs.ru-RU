---
title: Каноническое свойство PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 605e2f528ea0afc1a35348320abaffeb142d9921
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590724"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Каноническое свойство PidTagValidFolderMask

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску флагов, указывающие на правильность идентификаторы записей папок в хранилище сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Идентификатор:  <br/> |0x35DF  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Хранение сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Идентификатор записи папки могут стать недопустимыми, если пользователь удаляет папку или повреждения хранилища сообщений.
  
Для Битовая маска, которая может быть установлено одно или несколько из следующих флагов: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> Общие папки "представления" имеет идентификатор записей. В разделе **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> Папки поиска с идентификатором записей. В разделе **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Получать сообщения электронной почты — это (IPM) папки с идентификатором записей. В разделе [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> Папка исходящих IPM имеет идентификатор записей. В разделе **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> Папка Отправленные IPM имеет идентификатор записей. В разделе **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> Папка поддерева IPM имеет идентификатор записей. В разделе **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> Папки "Удаленные IPM" имеет идентификатор записей. В разделе **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> Папки "представления" имеет идентификатор записей. В разделе **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

