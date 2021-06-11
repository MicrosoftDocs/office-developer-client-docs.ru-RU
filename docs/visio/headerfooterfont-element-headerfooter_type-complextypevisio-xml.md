---
title: Элемент HeaderFooterFont (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: Указывает шрифт, используемый для текста загона и подножки.
ms.openlocfilehash: b87ba96d551bf943dd330aa428f2c943c9d29269
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541087"
---
# <a name="headerfooterfont-element-headerfooter_type-complextype-visio-xml"></a>Элемент HeaderFooterFont (HeaderFooter_Type complexType) (Visio XML)

Указывает шрифт, используемый для текста загона и подножки.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |document.xml  <br/> |
   
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
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |Содержит элементы для загона и подножки документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает набор символов шрифта. Эквивалент поля GDI LOGFONTlfCharSet.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает точность вырезки шрифта. Эквивалент поля GDI LOGFONTlfClipPrecision.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Escapement  <br/> |xsd:int  <br/> |необязательный  <br/> |Указывает атрибут побега шрифта. Эквивалент поля GDI LOGFONTlfEscapement.  <br/> |Значения типа xsd:int.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |необязательный  <br/> |Содержит сведения о шрифте.  <br/> |Значения типа xsd:string.  <br/> |
|Height  <br/> |xsd:int  <br/> |необязательный  <br/> |Указывает высоту фигуры в единицах рисования.  <br/> |Значения типа xsd:int.  <br/> |
|Курсив  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает, является ли шрифт italic. Эквивалент поля GDI LOGFONTlfItalic.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Вводное обучение  <br/> |xsd:int  <br/> |необязательный  <br/> |Указывает ориентацию шрифта. Эквивалент поля GDI LOGFONTlfOrientation.  <br/> |Значения типа xsd:int.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает атрибут точности вывода шрифта. Эквивалент поля GDI LOGFONTlfOutPrecision.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает поле и семейство шрифта. Эквивалент поля GDI LOGFONTlfPitchAndFamily.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Качество  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает качество вывода шрифта. Эквивалент поля GDI LOGFONTlfQuality.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает, является ли шрифт шрифтом выпадающего шрифта. Эквивалент поля GDI LOGFONTlfStrikeOut.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Подчеркнутый  <br/> |xsd:unsignedByte  <br/> |необязательный  <br/> |Указывает, подчеркивается ли шрифт. Эквивалент поля GDI LOGFONTlfUnderline.  <br/> |Значения типа xsd:unsignedByte.  <br/> |
|Насыщенность  <br/> |xsd:int  <br/> |необязательный  <br/> |Указывает вес шрифта. Эквивалент поля GDI LOGFONTlfWeight.  <br/> |Значения типа xsd:int.  <br/> |
|Width  <br/> |xsd:int  <br/> |необязательный  <br/> |Содержит ширину связанной фигуры в единицах рисования.  <br/> |Значения типа xsd:int.  <br/> |
   

