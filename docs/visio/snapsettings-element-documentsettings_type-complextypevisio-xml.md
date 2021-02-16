---
title: Элемент SnapSettings (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Указывает объекты, которые фигуры оснастки, когда оснастка активна в окне.
ms.openlocfilehash: 8d4be35a4cd66a1d3914dbda8162f4acb3d05bfa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540296"
---
# <a name="snapsettings-element-documentsettings_type-complextype-visio-xml"></a>Элемент SnapSettings (DocumentSettings_Type complexType) (Visio XML)

Указывает объекты, которые фигуры оснастки, когда оснастка активна в окне.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml  <br/> |
   
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
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие параметры документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  
## <a name="remarks"></a>Примечания

Значение может быть суммой значений в следующей таблице.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |Прикрепить к ничего не нужно.  <br/> |
|1   <br/> |Прикрепление к подразделам линейки.  <br/> |
|2   <br/> |Прикрепление к сетке.  <br/> |
|4   <br/> |Прикрепление к руководствам.  <br/> |
|8   <br/> |Прикрепление к окнам выделения.  <br/> |
|16   <br/> |Прикрепление к вершинам.  <br/> |
|32  <br/> |Прикрепление к точкам подключения.  <br/> |
|256  <br/> |Прикрепление к видимым краям фигур.  <br/> |
|512  <br/> |Прикрепление к окну выравнивания.  <br/> |
|1024  <br/> |Прикрепление к вариантам расширений фигур.  <br/> |
|32768  <br/> |Прикрепление отключено.  <br/> |
|65536  <br/> |Прикрепление к пересечениям.  <br/> |
   

