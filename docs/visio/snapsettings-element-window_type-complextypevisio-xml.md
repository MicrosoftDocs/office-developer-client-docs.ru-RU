---
title: Элемент SnapSettings (Window_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b87a244-b331-7e93-d304-239f8ca77061
description: Определяет объекты, которые привязать фигуры при привязка активна в окне.
ms.openlocfilehash: 55558301b1f85f70f723d4282b438e4883d90c25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814903"
---
# <a name="snapsettings-element-windowtype-complextype-visio-xml"></a>Элемент SnapSettings (Window_Type complexType) ('Visio XML»)

Определяет объекты, которые привязать фигуры при привязка активна в окне.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Windows.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Окно](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Представляет окно в экземпляре Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  
## <a name="remarks"></a>Замечания

Значение может быть сумма значений в следующей таблице.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Привязать значение nothing.  <br/> |
|1  <br/> |Привязка к промежуточные деления линейки.  <br/> |
|2  <br/> |Привязка к сетке.  <br/> |
|4  <br/> |Привязка к описаниям.  <br/> |
|8  <br/> |Привязка маркеры выделения.  <br/> |
|16  <br/> |Привязка к вершинам.  <br/> |
|32  <br/> |Привязка точек подключения.  <br/> |
|256  <br/> |Привязка к видимым края фигур.  <br/> |
|512  <br/> |Привязка к рамке выравнивания.  <br/> |
|1024  <br/> |Привязка к параметры расширения фигуры.  <br/> |
|32768  <br/> |Оснастка отключены.  <br/> |
|65536  <br/> |Привязка к пересечения.  <br/> |
   

