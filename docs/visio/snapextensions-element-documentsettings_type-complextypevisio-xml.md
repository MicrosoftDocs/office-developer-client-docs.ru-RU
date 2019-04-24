---
title: Элемент SnapExtensions (Документсеттингс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Указывает, включен или отключен указанный параметр расширения привязки для активного окна.
ms.openlocfilehash: 9f21653fca7f1f5fa7be7449f1e588cf5ef67263
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334533"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>Элемент SnapExtensions (Документсеттингс_типе complexType) (' Visio XML ')

Указывает, включен или отключен указанный параметр расширения привязки для активного окна. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Снапекстенсионс_типе](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
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
|[Документсеттингс](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Документсеттингс_типе](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие параметры документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  
## <a name="remarks"></a>Примечания

Значение элемента **SnapExtensions** может быть суммой значений, приведенных в следующей таблице. 
  
|**Value**|**Описание**|
|:-----|:-----|
|нуль  <br/> |ПриВязывать к Nothing.  <br/> |
|1,1  <br/> |ПриКрепить к расширению поля выравнивания.  <br/> |
|2  <br/> |ПриВязать к расширению центральной оси.  <br/> |
|SP4  <br/> |ПриВязать к добавочному номеру тангенса.  <br/> |
|8,5  <br/> |ПриКрепить к добавочному номеру конечной точки.  <br/> |
|столбцов  <br/> |ПриВязать к средней точке.  <br/> |
|32  <br/> |ПриВязать к линейному добавочному номеру.  <br/> |
|64  <br/> |ПриКрепить к модулю кривизны.  <br/> |
|128  <br/> |ПриВязать к добавочному номеру конечной точки.  <br/> |
|256  <br/> |ПриКрепить к середине перпендикулярного расширения.  <br/> |
|512  <br/> |ПриВязать к горизонтальному добавочному номеру конечной точки.  <br/> |
|1024  <br/> |ПриКрепить к вертикальному добавочному номеру конечной точки.  <br/> |
|2048  <br/> |ПриВязать к добавочному номеру центра эллипса.  <br/> |
|4096  <br/> |ПриКрепить к расширению Изометрические углы.  <br/> |
   

