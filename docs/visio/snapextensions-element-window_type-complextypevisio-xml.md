---
title: Элемент SnapExtensions (Window_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Указывает, включен или отключен определенный параметр расширения оснастки для активного окна. Значение может быть суммой значений в следующей таблице.
ms.openlocfilehash: bf3a6ae8cbeaadca8d4d899d96c916ee13ce9dfc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540324"
---
# <a name="snapextensions-element-window_type-complextype-visio-xml"></a>Элемент SnapExtensions (Window_Type complexType) (Visio XML)

Указывает, включен или отключен определенный параметр расширения оснастки для активного окна. Значение может быть суммой значений в следующей таблице.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |windows.xml  <br/> |
   
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

Значение элемента **SnapExtensions** может быть суммой значений в следующей таблице. 
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |прикрепление ничего.  <br/> |
|1  <br/> |прикрепление выравнивание расширения окна.  <br/> |
|2  <br/> |прикрепление в центр расширения оси.  <br/> |
|4   <br/> |прикрепление изогнутые расширения по касательной.  <br/> |
|8   <br/> |прикрепление расширения конечной точки.  <br/> |
|16   <br/> |прикрепление до середины расширения.  <br/> |
|32  <br/> |прикрепление линейное расширение.  <br/> |
|64  <br/> |прикрепление для кривой расширения.  <br/> |
|128  <br/> |прикрепление перпендикулярного расширения конечной точки.  <br/> |
|256  <br/> |прикрепление до средней точки перпендикулярного расширения.  <br/> |
|512  <br/> |прикрепление горизонтальное расширение конечной точки.  <br/> |
|1024  <br/> |прикрепление вертикального расширения конечной точки.  <br/> |
|2048  <br/> |прикрепление расширение центра эллипса.  <br/> |
|4096  <br/> |прикрепление расширения изометрических углов.  <br/> |
   

