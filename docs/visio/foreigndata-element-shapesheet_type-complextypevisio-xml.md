---
title: Элемент ForeignData (ShapeSheet_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Содержит MIME (многоцелевые расширения интернет-почты), закодированные BLOB данных изображений, таких как Windows, bitmap или данные OLE.
ms.openlocfilehash: 6b130b5a50a51d5d909b843e805d197735dc7146
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539844"
---
# <a name="foreigndata-element-shapesheet_type-complextype-visio-xml"></a>Элемент ForeignData (ShapeSheet_Type ComplexType) (Visio XML)

Содержит MIME (многоцелевые расширения интернет-почты), закодированные BLOB данных изображений, таких как Windows, bitmap или данные OLE.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие фигуру в **элементе Master,** **Page** или group shape.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Rel](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Rel_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Указывает отношение к части, содержащей данные изображения.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |необязательный  <br/> |Указывает уровень сжатия, примененный к файлу. Этот атрибут имеет смысл только в том случае, если иностранные данные — это иностранный объект на основе raster, например DIB, JPG, PNG, TIFF или GIF-файл.  <br/> |Значения типа xsd:double.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |необязательный  <br/> |Указывает тип сжатия, примененного к файлу. Этот атрибут имеет смысл только в том случае, если иностранные данные — это иностранный объект на основе raster, например DIB, JPG, PNG, TIFF или ФАЙЛ GIF.  <br/> |Значения типа xsd:token.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |необязательный  <br/> |Указывает горизонтальную степень метафила. Этот атрибут имеет смысл только в том случае, если иностранные данные — это метафильм.  <br/> |Значения типа xsd:double.  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |необязательный  <br/> |Указывает вертикальную степень метафила. Этот атрибут имеет смысл только в том случае, если иностранные данные — это метафильм.  <br/> |Значения типа xsd:double.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |Обязательный  <br/> |Указывает метафил, тип EnhMetaFile, Bitmap, Object или Ink.  <br/> |Значения типа xsd:token.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Указывает режим сопоставления метафизических данных. Этот атрибут имеет смысл только в том случае, если иностранные данные — это метафильм.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |необязательный  <br/> |Указывает высоту объекта в единицах страниц. Этот атрибут имеет смысл только в том случае, если иностранные данные — это встроенный объект OLE2.  <br/> |Значения типа xsd:double.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Integer indicator of object type. Используется, когда иностранный тип является объектом.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |необязательный  <br/> |Указывает ширину объекта в единицах страниц. Этот атрибут имеет смысл только в том случае, если иностранные данные — это встроенный объект OLE2.  <br/> |Значения типа xsd:double.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, показывать или не показывать встроенные данные в качестве значка.  <br/> |Значения типа xsd:boolean.  <br/> |
   

