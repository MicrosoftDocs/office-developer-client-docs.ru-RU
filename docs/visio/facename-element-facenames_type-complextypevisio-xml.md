---
title: Элемент Фаценаме (Фаценамес_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Содержит сведения о шрифте.
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322605"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>Элемент Фаценаме (Фаценамес_типе complexType) (' Visio XML ')

Содержит сведения о шрифте.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Фаценаме_типе](facename_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Фаценамес](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Фаценамес_типе](facenames_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **фаценаме** .  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Чарсетс  <br/> |XSD: строка  <br/> |необязательный  <br/> |Поддерживаемые кодировки шрифта.  <br/> |Значения типа String: XSD.  <br/> |
|Flags  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Флаги, указывающие на следующие значения: отсутствующий шрифт, используемый по умолчанию шрифт, азиатский шрифт, сложный шрифт, вертикальный шрифт и тип шрифта.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Имя шрифта в виде строки Юникода UTF – 16.  <br/> ||
|Панос  <br/> |XSD: строка  <br/> |необязательный  <br/> |Подпись паносе для шрифта. Паносе — это система классификации для гарнитур, которые классифицируются на основе их визуальных характеристик.  <br/> |Значения типа String: XSD.  <br/> |
|Уникодеранжес  <br/> |XSD: строка  <br/> |необязательный  <br/> |Поддерживаемые диапазоны Юникода для шрифта.  <br/> |Значения типа String: XSD.  <br/> |
   

