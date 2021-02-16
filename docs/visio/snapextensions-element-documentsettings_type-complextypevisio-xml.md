---
title: Элемент SnapExtensions (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Указывает, включен ли определенный параметр расширения оснастки для активного окна.
ms.openlocfilehash: 86ff7f32d6e12b2f0d7a8387d8e5b7ae9870b5fa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540380"
---
# <a name="snapextensions-element-documentsettings_type-complextype-visio-xml"></a>Элемент SnapExtensions (DocumentSettings_Type complexType) (Visio XML)

Указывает, включен ли определенный параметр расширения оснастки для активного окна. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml  <br/> |
   
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
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие параметры документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  
## <a name="remarks"></a>Примечания

Значение элемента **SnapExtensions** может быть суммой значений в следующей таблице. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Прикрепить к ничего не нужно.  <br/> |
|1   <br/> |Прикрепление к расширению выравнивания.  <br/> |
|2   <br/> |Прикрепление к центру расширения оси.  <br/> |
|4   <br/> |Прикрепление к расширению тангента кривой.  <br/> |
|8   <br/> |Прикрепление к расширению конечной точки.  <br/> |
|16   <br/> |Прикрепление к расширению средней точки.  <br/> |
|32  <br/> |Прикрепление к линейному расширению.  <br/> |
|64  <br/> |Прикрепление к расширению кривой.  <br/> |
|128  <br/> |Прикрепление к перпендикулярного расширения конечной точки.  <br/> |
|256  <br/> |Прикрепление к перпендикулярном расширению средней точки.  <br/> |
|512  <br/> |Прикрепление к горизонтальному расширению конечной точки.  <br/> |
|1024  <br/> |Прикрепление к вертикальному расширению конечной точки.  <br/> |
|2048  <br/> |Прикрепление к расширению центра эллипса.  <br/> |
|4096  <br/> |Прикрепление к расширению изометрических углов.  <br/> |
   

