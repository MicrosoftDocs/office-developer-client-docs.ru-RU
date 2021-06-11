---
title: Каноническое свойство PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331579"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Каноническое свойство PidLidMeetingType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает тип запроса собрания или обновления собрания.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidMeetingType  <br/> |
|Набор свойств:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000026  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Собрания  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этого свойства должно быть установлено в одном из следующих значений:
  
|**Свойство**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Неустановлено.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Начальный запрос на собрание.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Полное обновление.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Информационное обновление.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |После этого был получен более новый запрос на собрание или обновление собрания.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Это устанавливается в копии делегатора, когда делегат обрабатывает объекты, связанные с собраниями.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрания и ответных сообщений.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

