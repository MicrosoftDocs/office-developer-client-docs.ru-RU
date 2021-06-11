---
title: Каноническое свойство PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357808"
---
# <a name="pidlidflagrequest-canonical-property"></a>Каноническое свойство PidLidFlagRequest

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет состояние запроса на собрание.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidRequest  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008530  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Флажки  <br/> |
   
## <a name="remarks"></a>Примечания

В Microsoft Office Outlook запрос на собрание — это элемент встречи.
  
Это свойство содержит указанный пользователем текст, связанный с флагом, и должно быть задано, если объект сообщения помечен или завершен, но не должен существовать для объекта, связанного с собранием. Клиенты могут не поддерживать это свойство и всегда писать "Follow up" (при необходимости переведено на язык пользователя) в качестве значения строки, когда это свойство должно быть заданной. Это свойство должно быть условно проигнорировано в зависимости от значений свойств **dispidFlagStringEnum** [(PidLidFlagString)](pidlidflagstring-canonical-property.md)и **dispidValidFlagStringProof** [(PidLidValidFlagStringProof).](pidlidvalidflagstringproof-canonical-property.md)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с маркировкой.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

