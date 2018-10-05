---
title: Элемент Windows ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Содержит элементы окна документа.
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386805"
---
# <a name="windows-element-visio-xml"></a>Элемент Windows ('Visio XML»)

Содержит элементы **окна** документа. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Windows.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

Нет.
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Представляет окно в экземпляре Microsoft Visio.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ClientHeight  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Представляет значение высоты области отображения  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ClientWidth  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Представляет ширины области отображения  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
   

