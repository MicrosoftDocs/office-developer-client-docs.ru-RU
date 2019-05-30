---
title: Элемент Shapes (Пажеконтентс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Содержит коллекцию элементов Shape.
ms.openlocfilehash: 5d248dd2683a1ccc153d15477c888e1b13d24d0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542123"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a>Элемент Shapes (Пажеконтентс_типе complexType) (XML для Visio)

Содержит коллекцию элементов Shape.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Шапес_типе](shapes_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |страница #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Мастерконтентс](mastercontents-elementvisio-xml.md) <br/> |[Пажеконтентс_типе](pagecontents_type-complextypevisio-xml.md) <br/> |Задает сведения о фигурах в образце в веб-документе.  <br/> |
|[Пажеконтентс](pagecontents-elementvisio-xml.md) <br/> |[Пажеконтентс_типе](pagecontents_type-complextypevisio-xml.md) <br/> |Задает сведения о фигурах в образце в веб-документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Шапешит_типе](shapesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие фигуру в **главной**, **странице**или элементе фигуры группы.  <br/> |
   
### <a name="attributes"></a>Атрибуты

Нет.
  

