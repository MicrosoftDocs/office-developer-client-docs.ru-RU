---
title: Элемент Rel (Master_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Указывает отношение к части с соответствующим мастером XML.
ms.openlocfilehash: 032c1ef4a94bb6acf18587a1257fe82285124e87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542802"
---
# <a name="rel-element-master_type-complextype-visio-xml"></a>Элемент Rel (Master_Type ComplexType) (Visio XML)

Указывает отношение к части с соответствующим мастером XML.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |Указывает один экземпляр мастера XML, хранимого в рисунке.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|r:id  <br/> |xsd:string  <br/> См. раздел "Замечания".  <br/> |Обязательный  <br/> |Указывает отношение к части.  <br/> |"rId#"  <br/> См. раздел "Замечания".  <br/> |
   
## <a name="remarks"></a>Примечания

Значение атрибута **r:id** должно быть **ST_RelationshipID** типом. Тип **ST_RelationshipID** — это строка, которая должна быть в формате "rId#", где конечным персонажем должно быть число. Номер должен быть уникальным среди всех элементов sibling элемента **Rel.** 
  
Дополнительные сведения о типе ST_RelationshipID см. в спецификации [ISO/IEC 29500 Часть 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)
  

