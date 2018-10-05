---
title: Элемент HeaderFooterFont (HeaderFooter_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Задает шрифт, используемый для текста верхнего и нижнего колонтитулов.
ms.openlocfilehash: f14d973caddc77394881d1b1dfd62a43f10cd7bb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385972"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>Элемент HeaderFooterFont (HeaderFooter_Type complexType) ('Visio XML»)

Задает шрифт, используемый для текста верхнего и нижнего колонтитулов.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Содержит элементы для колонтитулов документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Набор символов  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Задает набор символов шрифта. Эквивалент в поле GDI LOGFONTlfCharSet.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Указывает точность отсечения шрифта. Эквивалент в поле GDI LOGFONTlfClipPrecision.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Наклон  <br/> |XSD: int  <br/> |необязательный  <br/> |Указывает атрибут наклон шрифта. Эквивалент в поле GDI LOGFONTlfEscapement.  <br/> |Значения типа XSD: int.  <br/> |
|Название значка  <br/> |XSD:String  <br/> |необязательный  <br/> |Содержит сведения о шрифта.  <br/> |Значения типа xsd:string.  <br/> |
|Height  <br/> |XSD: int  <br/> |необязательный  <br/> |Задает высоту фигуры в единицах документа.  <br/> |Значения типа XSD: int.  <br/> |
|Курсив  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Указывает, является ли шрифт курсивом. Эквивалент в поле GDI LOGFONTlfItalic.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Ориентация  <br/> |XSD: int  <br/> |необязательный  <br/> |Ориентация шрифта. Эквивалент в поле GDI LOGFONTlfOrientation.  <br/> |Значения типа XSD: int.  <br/> |
|OutPrecision  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Указывает атрибут точности вывода шрифта. Эквивалент в поле GDI LOGFONTlfOutPrecision.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Задает шаг и семейства шрифта. Эквивалент в поле GDI LOGFONTlfPitchAndFamily.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Качество  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Указывает качество шрифта. Эквивалент в поле GDI LOGFONTlfQuality.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Зачеркивание  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Указывает, является ли шрифт зачеркнутый шрифт. Эквивалент в поле GDI LOGFONTlfStrikeOut.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Подчеркивание  <br/> |XSD:unsignedByte  <br/> |необязательный  <br/> |Указывает, является ли шрифт подчеркнутым. Эквивалент в поле GDI LOGFONTlfUnderline.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Насыщенность  <br/> |XSD: int  <br/> |необязательный  <br/> |Задает Вес шрифта. Эквивалент в поле GDI LOGFONTlfWeight.  <br/> |Значения типа XSD: int.  <br/> |
|Width  <br/> |XSD: int  <br/> |необязательный  <br/> |Содержит ширину связанные фигуры в единицах документа.  <br/> |Значения типа XSD: int.  <br/> |
   

