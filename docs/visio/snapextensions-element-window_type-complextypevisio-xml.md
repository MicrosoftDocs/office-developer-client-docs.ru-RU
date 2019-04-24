---
title: Элемент SnapExtensions (Виндов_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Указывает, включен или отключен указанный параметр расширения привязки для активного окна. Значение может быть суммой значений, приведенных в следующей таблице.
ms.openlocfilehash: 57fde520d3dc8e0582c0062a599d5f38a73169b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334421"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a>Элемент SnapExtensions (Виндов_типе complexType) (' Visio XML ')

Указывает, включен или отключен указанный параметр расширения привязки для активного окна. Значение может быть суммой значений, приведенных в следующей таблице.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Снапекстенсионс_типе](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
   

