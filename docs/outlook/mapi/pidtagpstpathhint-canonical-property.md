---
title: Каноническое свойство PidTagPstPathHint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437310"
---
# <a name="pidtagpstpathhint-canonical-property"></a>Каноническое свойство PidTagPstPathHint

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Предоставляет имя личной таблицы хранения (PST-файла), которую пользователь может редактировать, в диалоговом окне Конфигурация. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PST_PATH_HINT, PR_PST_PATH_HINT_A PR_PST_PATH_HINT_W  <br/> |
|Идентификатор:  <br/> |0x6771  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Внутренняя таблица хранения личных данных (PST)  <br/> |
   
## <a name="remarks"></a>Примечания

Если вместо этого используется свойство **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)), откроется диалоговое окно Configuration (конфигурация), но пользователю не будет разрешено изменять путь и многие другие свойства.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]] 
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

