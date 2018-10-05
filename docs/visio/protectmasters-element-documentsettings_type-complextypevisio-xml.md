---
title: Элемент ProtectMasters (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Указывает, является ли пользователь, которым запрещен создание, изменение или удаление образцов фигур. Пользователь по-прежнему может создавать новые фигуры из главной формы, независимо от того, этот параметр.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386448"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>Элемент ProtectMasters (DocumentSettings_Type complexType) ('Visio XML»)

Указывает, является ли пользователь, которым запрещен создание, изменение или удаление образцов фигур. Пользователь по-прежнему может создавать новые фигуры из главной формы, независимо от того, этот параметр. 
  
Диапазон допустимых значений для этого элемента — "0" или "1". Значение "0" Указывает, что пользователи создание, изменение и удаление образцов фигур. Значение "1" Указывает, что пользователи не могут создать, изменить и удалить основной фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, которые определяют параметры документов.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  

