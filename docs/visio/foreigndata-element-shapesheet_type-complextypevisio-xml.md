---
title: Элемент ForeignData (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Содержит MIME (Multipurpose Internet Mail Extensions) закодированный большого двоичного ОБЪЕКТА данных изображения, например метафайла Windows, точечного рисунка или данных OLE.
ms.openlocfilehash: d548ce8a6b05f8a9a104aee96c0982c6dbccc417
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813822"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a>Элемент ForeignData (ShapeSheet_Type complexType) ('Visio XML»)

Содержит MIME (Multipurpose Internet Mail Extensions) закодированный большого двоичного ОБЪЕКТА данных изображения, например метафайла Windows, точечного рисунка или данных OLE.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |страницы # .xml, главные # .xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Фигура](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Указывает связь с частью, содержащий данные изображения.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD: double  <br/> |необязательный  <br/> |Задает уровень сжатия, применяемой к файлу. Этот атрибут применяется только в том случае, если внешние данные растрового внешнего объект, например файл DIB, JPG, PNG, TIFF или GIF.  <br/> |Значения типа XSD: double.  <br/> |
|CompressionType  <br/> |XSD:Token  <br/> |необязательный  <br/> |Указывает тип сжатия, применяемой к файлу. Этот атрибут применяется только в случае растровых изображений внешнего объект, например файл DIB, JPG, PNG, TIFF или GIF внешних данных  <br/> |Значения типа xsd:token.  <br/> |
|ExtentX  <br/> |XSD: double  <br/> |необязательный  <br/> |Задает горизонтальную степени метафайла. Этот атрибут применяется только в том случае, если внешние данные метафайла.  <br/> |Значения типа XSD: double.  <br/> |
|ExtentY  <br/> |XSD: double  <br/> |необязательный  <br/> |Задает верхнюю границу метафайла. Этот атрибут применяется только в том случае, если внешние данные метафайла.  <br/> |Значения типа XSD: double.  <br/> |
|ForeignType  <br/> |XSD:Token  <br/> |Обязательный  <br/> |Указывает тип метафайла, EnhMetaFile, растровое изображение, объект или рукописного ввода.  <br/> |Значения типа xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> |Задает режим сопоставления метафайла. Этот атрибут применяется только в том случае, если внешние данные метафайла.  <br/> |Значения типа xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD: double  <br/> |необязательный  <br/> |Задает высоту объекта в единицах страницы. Этот атрибут применяется только в том случае, если внешних данных — это встроенный объект OLE2.  <br/> |Значения типа XSD: double.  <br/> |
|Тип объекта  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает тип объекта, целое число. Используется при внешнего типа — это объект.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD: double  <br/> |необязательный  <br/> |Задает ширину объекта в единицах страницы. Этот атрибут применяется только в том случае, если внешних данных — это встроенный объект OLE2.  <br/> |Значения типа XSD: double.  <br/> |
|ShowAsIcon  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, следует ли отображать или не отображать внедренные данные в виде значка.  <br/> |Значения типа xsd:boolean.  <br/> |
   

