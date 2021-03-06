---
title: Элемент SnapSettings (DocumentSettings_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Указывает объекты, формуя привязку к при активной оснастке в окне.
ms.openlocfilehash: 8d4be35a4cd66a1d3914dbda8162f4acb3d05bfa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540296"
---
# <a name="snapsettings-element-documentsettings_type-complextype-visio-xml"></a>Элемент SnapSettings (DocumentSettings_Type ComplexType) (Visio XML)

Указывает объекты, формуя привязку к при активной оснастке в окне.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |document.xml  <br/> |
   
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
|[DocumentSettings](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, указывающие параметры документов.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  
## <a name="remarks"></a>Примечания

Значение может быть суммой значений в следующей таблице.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0  <br/> |прикрепление ничего.  <br/> |
|1  <br/> |прикрепление для подразделений линейки.  <br/> |
|2  <br/> |прикрепление в сетку.  <br/> |
|4   <br/> |прикрепление руководства.  <br/> |
|8   <br/> |прикрепление к ручкам выбора.  <br/> |
|16   <br/> |прикрепление на вершины.  <br/> |
|32  <br/> |прикрепление к точкам подключения.  <br/> |
|256  <br/> |прикрепление видимые края фигур.  <br/> |
|512  <br/> |прикрепление поле выравнивания.  <br/> |
|1024  <br/> |прикрепление для настройки параметров расширений.  <br/> |
|32768  <br/> |прикрепление отключен.  <br/> |
|65536  <br/> |прикрепление пересечения.  <br/> |
   

