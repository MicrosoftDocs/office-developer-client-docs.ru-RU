---
title: Элемент SnapSettings (DocumentSettings_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Определяет объекты, которые привязать фигуры при привязка активна в окне.
ms.openlocfilehash: 68c2bd198a20047ce4f56fe06630177a17319191
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401680"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>Элемент SnapSettings (DocumentSettings_Type complexType) ('Visio XML»)

Определяет объекты, которые привязать фигуры при привязка активна в окне.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="SnapSettings" type="SnapSettings_Type" minOccurs="0" maxOccurs="1" >
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
   

