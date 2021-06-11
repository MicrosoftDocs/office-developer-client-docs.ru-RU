---
title: Каноническое свойство PidLidToDoTitle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidToDoTitle
api_type:
- COM
ms.assetid: 94cf031f-4c78-441d-9c01-55905b4974e0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ed69d9bab84a5c572026bb9480249c1212e3376
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339944"
---
# <a name="pidlidtodotitle-canonical-property"></a>Каноническое свойство PidLidToDoTitle

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит указанный пользователем текст для идентификации этого объекта сообщения в консолидированном списке дел.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidToDoTitle  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085A4  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство не должно быть заданной задачей. Чтобы указать пустое свойство, не установите это свойство в строку нулевой длины, а удалите его. 
  
При маркировке объекта сообщения, а свойства не существует, клиент должен написать значение **PR_NORMALIZED_SUBJECT** [(PidTagNormalizedSubject)](pidtagnormalizedsubject-canonical-property.md)в это свойство.
  
В консолидированном списке дел, если этого свойства не существует, клиент должен **заменить** значение свойства PR_NORMALIZED_SUBJECT при отобращении этого свойства в списке дел. 
  
На объекте черновика сообщения, если клиент реализует флаги отправитель, это свойство должно быть установлено в том же значении, что **и dispidRequest** [(PidLidFlagRequest).](pidlidflagrequest-canonical-property.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на спецификации Exchange Server протокола
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с маркировкой.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)
  
[������������ �������� PidLidFlagRequest](pidlidflagrequest-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

