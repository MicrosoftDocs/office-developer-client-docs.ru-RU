---
title: Каноническое свойство PidLidBusinessCardDisplayDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 34d29b9a15cc6f5a3f88a6477738eb63904e1fdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810216"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>Каноническое свойство PidLidBusinessCardDisplayDefinition

  
  
**Относится к**: Outlook 
  
Содержит сведения о пользовательские настройки для отображения в виде визитной карточки контакта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidBCDisplayDefinition  <br/> |
|Набор свойств:  <br/> |PSETID_Address  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008040  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контакт  <br/> |
   
## <a name="remarks"></a>Замечания

Макет визитной карточки может быть представлена как изображения и количество полей текст. Изображение может быть фотографий контактов или изображение карточки. Текстовые поля состоят из значения из другого свойства на контакт и строку необязательные настраиваемые метки, заданное пользователем. Обратите внимание, что значения несколькими byte хранятся в формате с прямым в буфере.
  
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

