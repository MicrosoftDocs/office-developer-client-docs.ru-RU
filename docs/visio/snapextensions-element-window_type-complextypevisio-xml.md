---
title: Элемент SnapExtensions (Window_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7a12ae10-6aa4-c845-5ede-1c14c6dac80f
description: Указывает, будет ли параметр расширения с определенным оснастке включена или отключена для активного окна. Значение может быть сумма значений в следующей таблице.
ms.openlocfilehash: 0fe9ce4060fbd6366a188e17ed716cb74034f375
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814898"
---
# <a name="snapextensions-element-windowtype-complextype-visio-xml"></a>Элемент SnapExtensions (Window_Type complexType) ('Visio XML»)

Указывает, будет ли параметр расширения с определенным оснастке включена или отключена для активного окна. Значение может быть сумма значений в следующей таблице.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Windows.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="SnapExtensions" type="SnapExtensions_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Окно](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> ||
   
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
   

