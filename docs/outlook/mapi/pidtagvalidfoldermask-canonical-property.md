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
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427796"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Каноническое свойство PidTagValidFolderMask

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску флагов, указывающих допустимость идентификаторов записей папок в хранилище сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Идентификатор:  <br/> |0x35DF  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Хранилище сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Идентификатор записи папки может стать недопустимым, если пользователь удаляет папку или повреждено хранилище сообщений.
  
Для битовой маски можно задать один или несколько из следующих флагов: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> Папка "Общие представления" имеет допустимый идентификатор записи. Просмотрите **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> Папка Finder имеет допустимый идентификатор записи. Просмотрите **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> Папка приема сообщений (IPM) имеет допустимый идентификатор записи. См. [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> В папке "Исходящие" IPM есть допустимый идентификатор записи. Просмотрите **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> У папки IPM Sent Items допустимый идентификатор записи. Просмотрите **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> Поддерево папки IPM имеет допустимый идентификатор записи. Просмотрите **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> Папка "Удаленные" IPM содержит допустимый идентификатор записи. Просмотрите **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> У папки Views допустимый идентификатор записи. Просмотрите **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

