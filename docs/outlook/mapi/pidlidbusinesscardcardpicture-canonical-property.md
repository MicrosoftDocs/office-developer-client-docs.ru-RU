---
title: Каноническое свойство PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8e241022504291ad70f45a3318a7901bbbba213f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810212"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a>Каноническое свойство PidLidBusinessCardCardPicture

  
  
**Относится к**: Outlook 
  
Содержит изображения, используемого на визитной карточки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidBCCardPicture  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008041  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этого свойства должны быть потока JPEG или в формате PNG (PNG). Это свойство следует использовать в сочетании со свойством **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) следующим образом: **dispidBCCardPicture** не должна быть установлена на контакта if ** dispidBCDisplayDefinition** не установлена. Это свойство также не должна быть этот параметр указан, если данные в **dispidBCCardPicture** не требуется изображение карточки. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
