---
title: Элемент rel (Солутион_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Задает отношение к части с XML-документом решения, связанным с этим решением.
ms.openlocfilehash: 1fe48579da28501b74fedd507f3e44d59736ae87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542767"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a>Элемент rel (Солутион_типе complexType) (XML для Visio)

Задает отношение к части с XML-документом решения, связанным с этим решением.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Рел_типе](rel_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Pages. XML, Masters. XML, recordsets. XML, Page #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Решение](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[Солутион_типе](solution_type-complextypevisio-xml.md) <br/> |Задает один экземпляр XML-файла решения, хранящегося в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|р:ИД  <br/> |XSD: строка  <br/> См. раздел "Замечания".  <br/> |Обязательный  <br/> |Задает отношение к части.  <br/> |"rId #"  <br/> См. раздел "Замечания".  <br/> |
   
## <a name="remarks"></a>Примечания

Значение атрибута **р:ИД** должно быть типом **ст_релатионшипид** . Тип **ст_релатионшипид** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом. Число должно быть уникальным среди всех родственных элементов элемента **rel** . 
  
Для получения дополнительных сведений о типе Ст_релатионшипид, ознакомьтесь со [спецификацией ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).
  

