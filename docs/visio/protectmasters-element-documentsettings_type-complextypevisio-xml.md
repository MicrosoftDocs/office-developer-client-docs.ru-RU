---
title: Элемент Протектмастерс (Документсеттингс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Указывает, запрещено ли пользователю создавать, редактировать или удалять основные фигуры. Пользователь по-прежнему может создавать новые фигуры из основной фигуры независимо от этого параметра.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540695"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a>Элемент Протектмастерс (Документсеттингс_типе complexType) (XML для Visio)

Указывает, запрещено ли пользователю создавать, редактировать или удалять основные фигуры. Пользователь по-прежнему может создавать новые фигуры из основной фигуры независимо от этого параметра. 
  
Диапазон допустимых значений для этого элемента: "0" или "1". Значение "0" указывает на то, что пользователи могут создавать, изменять или удалять основные фигуры. Значение "1" указывает на то, что пользователи не могут создавать, изменять или удалять основные фигуры.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Протектмастерс_типе](protectmasters_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
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
|[Документсеттингс](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Документсеттингс_типе](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие параметры документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  

