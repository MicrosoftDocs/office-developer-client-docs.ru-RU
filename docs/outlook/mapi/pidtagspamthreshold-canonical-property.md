---
title: Каноническое свойство PidTagSpamThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2b2d6b8e-e3dd-4a9b-8bb5-53add675605d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 24a033269b072712fea6e9957d0ffac3573ce3a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811927"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Каноническое свойство PidTagSpamThreshold

  
  
**Относится к**: Outlook 
  
Значение типа long, указывающее уровень фильтрации нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> | 0x041B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Нежелательной почты  <br/> |
   
## <a name="values"></a>Values

Доступны следующие значения для фильтрации нежелательной почты:
  
|**Уровень нежелательной почты**|**Значение**|
|:-----|:-----|
|Нет  <br/> |0xFFFFFFFF  <br/> |
|Low  <br/> |0x00000006  <br/> |
|Средний  <br/> |0x00000005  <br/> |
|High  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Microsoft Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.
    
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
