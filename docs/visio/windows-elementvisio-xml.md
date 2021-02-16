---
title: Элемент Windows (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Содержит элементы Window для документа.
ms.openlocfilehash: fcffcd5257b14c0ae0203a41f369536e583c1798
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538447"
---
# <a name="windows-element-visio-xml"></a>Элемент Windows (Visio XML)

Содержит элементы **Window** для документа. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Windows_Type](windows_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |windows.xml  <br/> |
   
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
|[Window](window-element-windows_type-complextypevisio-xml.md) <br/> |[Window_Type](window_type-complextypevisio-xml.md) <br/> |Представляет открытое окно в экземпляре Microsoft Visio.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ClientHeight  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Представляет измерение высоты области отображения  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ClientWidth  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Представляет размер ширины области отображения  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
   

