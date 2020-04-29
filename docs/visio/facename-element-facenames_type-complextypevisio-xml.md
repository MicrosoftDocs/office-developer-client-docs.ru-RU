---
title: Элемент Фаценаме (FaceNames_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Содержит сведения о шрифте.
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541017"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a>Элемент Фаценаме (FaceNames_Type complexType) (XML для Visio)

Содержит сведения о шрифте.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[фаценамес](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **фаценаме** .  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|чарсетс  <br/> |XSD: строка  <br/> |необязательный  <br/> |Поддерживаемые кодировки шрифта.  <br/> |Значения типа String: XSD.  <br/> |
|Flags  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Флаги, указывающие на следующие значения: отсутствующий шрифт, используемый по умолчанию шрифт, азиатский шрифт, сложный шрифт, вертикальный шрифт и тип шрифта.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Имя шрифта в виде строки Юникода UTF – 16.  <br/> ||
|панос  <br/> |XSD: строка  <br/> |необязательный  <br/> |Подпись паносе для шрифта. Паносе — это система классификации для гарнитур, которые классифицируются на основе их визуальных характеристик.  <br/> |Значения типа String: XSD.  <br/> |
|уникодеранжес  <br/> |XSD: строка  <br/> |необязательный  <br/> |Поддерживаемые диапазоны Юникода для шрифта.  <br/> |Значения типа String: XSD.  <br/> |
   

