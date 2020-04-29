---
title: Элемент SnapExtensions (Window_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Указывает, включен или отключен указанный параметр расширения привязки для активного окна. Значение может быть суммой значений, приведенных в следующей таблице.
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540324"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>Элемент SnapExtensions (Window_Type complexType) (XML для Visio)

Указывает, включен или отключен указанный параметр расширения привязки для активного окна. Значение может быть суммой значений, приведенных в следующей таблице.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Windows. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
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
|4   <br/> |Привязать к добавочному номеру тангенса.  <br/> |
|8   <br/> |Прикрепить к добавочному номеру конечной точки.  <br/> |
|16   <br/> |Привязать к средней точке.  <br/> |
|32  <br/> |Привязать к линейному добавочному номеру.  <br/> |
|64  <br/> |Прикрепить к модулю кривизны.  <br/> |
|128  <br/> |Привязать к добавочному номеру конечной точки.  <br/> |
|256  <br/> |Прикрепить к середине перпендикулярного расширения.  <br/> |
|512  <br/> |Привязать к горизонтальному добавочному номеру конечной точки.  <br/> |
|1024  <br/> |Прикрепить к вертикальному добавочному номеру конечной точки.  <br/> |
|2048  <br/> |Привязать к добавочному номеру центра эллипса.  <br/> |
|4096  <br/> |Прикрепить к расширению Изометрические углы.  <br/> |
   

