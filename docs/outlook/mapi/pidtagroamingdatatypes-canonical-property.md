---
title: Каноническое свойство PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2b29f47191bc1f12653ddcc4e78dd8b3401f0480
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587644"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>Каноническое свойство PidTagRoamingDatatypes

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску, которое указывает, какие свойства существуют на сообщение потока.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Идентификатор:  <br/> |0x7C06  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Конфигурация  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно быть задано к одному или нескольким из следующих значений:
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000002  <br/> |Указывает, что сообщение связанные сведения о папке (FAI) должен содержать потока словаря, сериализованным в основных XML-схеме и хранится в свойстве **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)). Если сообщение FAI не содержит потока словаря, приложения должен обрабатывать словаря как необходимости нет записей.  <br/> |
|0x00000004  <br/> |Указывает, что сообщение FAI должно содержать поток XML, хранящиеся в свойстве **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)), который использует произвольных схемы XML.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

