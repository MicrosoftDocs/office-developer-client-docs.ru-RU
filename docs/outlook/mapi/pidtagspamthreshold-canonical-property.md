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
ms.openlocfilehash: d43a0229f232f9437d1746799534c0f2d6fba83f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346314"
---
# <a name="pidtagspamthreshold-canonical-property"></a>Каноническое свойство PidTagSpamThreshold

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Длинное значение, которое указывает уровень фильтрации нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SPAM_THRESHOLD  <br/> |
|Длинный ИД (КРЫШКА):  <br/> | 0x041B  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Спам  <br/> |
   
## <a name="values"></a>Значения

Фильтрация нежелательной почты может выполняться следующим образом:
  
|**Уровень нежелательной почты**|**Значение**|
|:-----|:-----|
|Нет  <br/> |0xFFFFFFFF  <br/> |
|Низкие  <br/> |0x00000006  <br/> |
|Средняя  <br/> |0x00000005  <br/> |
|Высокие  <br/> |0x00000003  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Microsoft Exchange Server спецификации протокола.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списков разрешающих и заблокированных сообщений, а также определение нежелательных сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

