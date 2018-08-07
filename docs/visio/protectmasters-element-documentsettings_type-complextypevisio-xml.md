---
title: Элемент ProtectMasters (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Указывает, является ли пользователь, которым запрещен создание, изменение или удаление образцов фигур. Пользователь по-прежнему может создавать новые фигуры из главной формы, независимо от того, этот параметр.
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814488"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>Элемент ProtectMasters (DocumentSettings_Type complexType) ('Visio XML»)

Указывает, является ли пользователь, которым запрещен создание, изменение или удаление образцов фигур. Пользователь по-прежнему может создавать новые фигуры из главной формы, независимо от того, этот параметр. 
  
Диапазон допустимых значений для этого элемента — "0" или "1". Значение "0" Указывает, что пользователи создание, изменение и удаление образцов фигур. Значение "1" Указывает, что пользователи не могут создать, изменить и удалить основной фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, которые определяют параметры документов.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  

