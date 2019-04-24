---
title: Элемент SnapSettings (Документсеттингс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Указывает объекты, к которым привязываются фигуры при активации привязки в окне.
ms.openlocfilehash: 68c2bd198a20047ce4f56fe06630177a17319191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334491"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>Элемент SnapSettings (Документсеттингс_типе complexType) (' Visio XML ')

Указывает объекты, к которым привязываются фигуры при активации привязки в окне.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Снапсеттингс_типе](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
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
|[Документсеттингс](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Документсеттингс_типе](documentsettings_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие параметры документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

Нет.
  
## <a name="remarks"></a>Примечания

Значение может быть суммой значений, приведенных в следующей таблице.
  
|**Value**|**Описание**|
|:-----|:-----|
|нуль  <br/> |ПриВязывать к Nothing.  <br/> |
|1,1  <br/> |Привязка к промежуточным делениям линейки.  <br/> |
|2  <br/> |ПриВязать к сетке.  <br/> |
|SP4  <br/> |ПриВязывать к направляющим.  <br/> |
|8,5  <br/> |ПриКрепить к маркерам выделения.  <br/> |
|столбцов  <br/> |ПриВязать к вершинам.  <br/> |
|32  <br/> |ПриВязывать к точкам подключения.  <br/> |
|256  <br/> |Привязка к видимым краям фигур.  <br/> |
|512  <br/> |ПриВязать к полю выравнивания.  <br/> |
|1024  <br/> |ПриВязывать к параметрам расширений фигур.  <br/> |
|32768  <br/> |ПриКрепление отключена.  <br/> |
|65536  <br/> |ПриВязывать к пересечениям.  <br/> |
   

