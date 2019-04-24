---
title: Элемент DocumentSheet (Висиодокумент_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b8673e1-b913-52db-2d1d-b3e8f4b8f952
description: Указывает структуру DocumentSheet.
ms.openlocfilehash: a2594e0325cc2743036a03998eb7ac71ed2183c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356366"
---
# <a name="documentsheet-element-visiodocumenttype-complextype-visio-xml"></a>Элемент DocumentSheet (Висиодокумент_типе complexType) (' Visio XML ')

Указывает структуру DocumentSheet.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Документшит_типе](documentsheet_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DocumentSheet" type="DocumentSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Висиодокумент](visiodocument-elementvisio-xml.md) <br/> |[Висиодокумент_типе](visiodocument_type-complextypevisio-xml.md) <br/> |Корневой элемент документа Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Целл_типе](cell_type-complextypevisio-xml.md) <br/> |Указывает ячейку в элементе DocumentSheet.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Искустомнаме  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, было ли имя настроено пользователем.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Искустомнамеу  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, настроено ли универсальное имя пользователем.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |необязательный  <br/> |Задает зависящее от языка имя DocumentSheet.  <br/> |Значения типа String: XSD.  <br/> |
|NameU  <br/> |XSD: строка  <br/> |необязательный  <br/> |Указывает имя DocumentSheet, не зависящее от языка.  <br/> |Значения типа String: XSD.  <br/> |
|UniqueID  <br/> |XSD: строка  <br/> |необязательный  <br/> |Необязательный атрибут типа string. GUID (глобальный уникальный идентификатор), определяющий фигуру.  <br/> |Значения типа String: XSD.  <br/> |
   

