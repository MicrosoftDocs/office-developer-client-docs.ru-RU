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
|Связанные свойства:  <br/> |ПР_ВАЛИД_ФОЛДЕР_МАСК  <br/> |
|Идентификатор:  <br/> |0x35DF  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Хранилище сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Идентификатор записи папки может стать недопустимым, если пользователь удаляет папку или повреждено хранилище сообщений.
  
Для битовой маски можно задать один или несколько из следующих флагов: 
  
ФОЛДЕР_КОММОН_ВИЕВС_ВАЛИД 
  
> Папка "Общие представления" имеет допустимый идентификатор записи. Обратитесь к разделу **пр_коммон_виевс_ентрид** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
ФОЛДЕР_ФИНДЕР_ВАЛИД 
  
> Папка Finder имеет допустимый идентификатор записи. Обратитесь к разделу **пр_финдер_ентрид** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
ФОЛДЕР_ИПМ_ИНБОКС_ВАЛИД 
  
> Папка приема сообщений (IPM) имеет допустимый идентификатор записи. См. [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md). 
    
ФОЛДЕР_ИПМ_АУТБОКС_ВАЛИД 
  
> В папке "исХодящие" IPM есть допустимый идентификатор записи. Обратитесь к разделу **пр_ипм_аутбокс_ентрид** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
ФОЛДЕР_ИПМ_СЕНТМАИЛ_ВАЛИД 
  
> У папки IPM Sent Items допустимый идентификатор записи. Обратитесь к разделу **пр_ипм_сентмаил_ентрид** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
ФОЛДЕР_ИПМ_СУБТРИ_ВАЛИД 
  
> Поддерево папки IPM имеет допустимый идентификатор записи. Обратитесь к разделу **пр_ипм_субтри_ентрид** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
ФОЛДЕР_ИПМ_ВАСТЕБАСКЕТ_ВАЛИД 
  
> Папка "Удаленные" IPM содержит допустимый идентификатор записи. Обратитесь к разделу **пр_ипм_вастебаскет_ентрид** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
ФОЛДЕР_ВИЕВС_ВАЛИД 
  
> У папки Views допустимый идентификатор записи. Обратитесь к разделу **пр_виевс_ентрид** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

