---
title: Элемент SnapExtensions (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Указывает, будет ли параметр расширения с определенным оснастке включена или отключена для активного окна.
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387617"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>Элемент SnapExtensions (DocumentSettings_Type complexType) ('Visio XML»)

Указывает, будет ли параметр расширения с определенным оснастке включена или отключена для активного окна. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, которые определяют параметры документов.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  
## <a name="remarks"></a>Замечания

Значение элемента **SnapExtensions** может быть сумма значений в следующей таблице. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Привязать значение nothing.  <br/> |
|1  <br/> |Привязка к расширение рамки выравнивания.  <br/> |
|2  <br/> |Привязка к расширение центр оси.  <br/> |
|4  <br/> |Привязка к график тангенс расширения.  <br/> |
|8  <br/> |Привязка к конечной точки расширения.  <br/> |
|16  <br/> |Привязка к середине расширения.  <br/> |
|32  <br/> |Привязка к линейное расширение.  <br/> |
|64  <br/> |Привязка к график расширения.  <br/> |
|128  <br/> |Привязка к перпендикулярная расширение конечной точки.  <br/> |
|256  <br/> |Привязка к среднее перпендикулярная расширения.  <br/> |
|512  <br/> |Привязка к горизонтальной расширение конечной точки.  <br/> |
|1024  <br/> |Привязка к вертикали расширение конечной точки.  <br/> |
|2048  <br/> |Привязка к расширение центр эллипса.  <br/> |
|4096  <br/> |Привязка к изометрические углы расширения.  <br/> |
   

