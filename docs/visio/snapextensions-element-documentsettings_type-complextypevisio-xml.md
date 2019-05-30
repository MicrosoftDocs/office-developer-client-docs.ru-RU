---
title: Элемент SnapExtensions (Документсеттингс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d55b6676-125f-7cf1-509d-21dee548f5a1
description: Указывает, включен или отключен указанный параметр расширения привязки для активного окна.
ms.openlocfilehash: 86ff7f32d6e12b2f0d7a8387d8e5b7ae9870b5fa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540380"
---
# <a name="snapextensions-element-documentsettingstype-complextype-visio-xml"></a>Элемент SnapExtensions (Документсеттингс_типе complexType) (XML для Visio)

Указывает, включен или отключен указанный параметр расширения привязки для активного окна. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Снапекстенсионс_типе](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
  
|**Значение**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Привязывать к Nothing.  <br/> |
|1,1  <br/> |Прикрепить к расширению поля выравнивания.  <br/> |
|2  <br/> |Привязать к расширению центральной оси.  <br/> |
|SP4  <br/> |Привязать к добавочному номеру тангенса.  <br/> |
|8   <br/> |Прикрепить к добавочному номеру конечной точки.  <br/> |
|столбцов  <br/> |Привязать к средней точке.  <br/> |
|32  <br/> |Привязать к линейному добавочному номеру.  <br/> |
|64  <br/> |Прикрепить к модулю кривизны.  <br/> |
|128  <br/> |Привязать к добавочному номеру конечной точки.  <br/> |
|256  <br/> |Прикрепить к середине перпендикулярного расширения.  <br/> |
|512  <br/> |Привязать к горизонтальному добавочному номеру конечной точки.  <br/> |
|1024  <br/> |Прикрепить к вертикальному добавочному номеру конечной точки.  <br/> |
|2048  <br/> |Привязать к добавочному номеру центра эллипса.  <br/> |
|4096  <br/> |Прикрепить к расширению Изометрические углы.  <br/> |
   

