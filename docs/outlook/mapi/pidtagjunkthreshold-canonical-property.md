---
title: Каноническое свойство PidTagJunkThreshold
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkThreshold
api_type:
- HeaderDef
ms.assetid: 8067e2b5-02df-4b96-8f66-509f5a48c8aa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7d4337105b2dcae94956f0b1badf66c663467dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565664"
---
# <a name="pidtagjunkthreshold-canonical-property"></a>Каноническое свойство PidTagJunkThreshold

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, агрессивности входящую почту направляются в папку нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_JUNK_THRESHOLD  <br/> |
|Идентификатор:  <br/> |0x6101  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Нежелательной почты  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство соответствует высокий / низкий / отсутствует filter параметр. Значение «0xFFFFFFFF» указывает, что фильтрации нежелательной почты не следует применять, но по-прежнему должны применяться черные списки. Значение «0x80000000» указывает, что все почтовые сообщения, нежелательной почты, за исключением тех сообщения от отправителей в список надежных отправителей или отправленных получателям в список надежных получателей. Доступны следующие значения:
  
|**Значение**|**Описание**|
|:-----|:-----|
|0xFFFFFFFF  <br/> |Без фильтрации нежелательной почты  <br/> |
|0x00000006  <br/> |Фильтрация низкой нежелательной почты  <br/> |
|0x00000003  <br/> |Фильтрация высоким нежелательной почты  <br/> |
|0x80000000  <br/> |Только Надежные списки  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
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

