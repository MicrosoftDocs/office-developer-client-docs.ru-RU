---
title: Элемент SnapSettings (Документсеттингс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e86e943-bd29-0a7b-3d6a-d91281f98777
description: Указывает объекты, к которым привязываются фигуры при активации привязки в окне.
ms.openlocfilehash: 8d4be35a4cd66a1d3914dbda8162f4acb3d05bfa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540296"
---
# <a name="snapsettings-element-documentsettingstype-complextype-visio-xml"></a>Элемент SnapSettings (Документсеттингс_типе complexType) (XML для Visio)

Указывает объекты, к которым привязываются фигуры при активации привязки в окне.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Снапсеттингс_типе](snapsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
  
|**Значение**|**Описание**|
|:-----|:-----|
|нуль  <br/> |Привязывать к Nothing.  <br/> |
|1,1  <br/> |Привязка к промежуточным делениям линейки.  <br/> |
|2  <br/> |Привязать к сетке.  <br/> |
|SP4  <br/> |Привязывать к направляющим.  <br/> |
|8   <br/> |Прикрепить к маркерам выделения.  <br/> |
|столбцов  <br/> |Привязать к вершинам.  <br/> |
|32  <br/> |Привязывать к точкам подключения.  <br/> |
|256  <br/> |Привязка к видимым краям фигур.  <br/> |
|512  <br/> |Привязать к полю выравнивания.  <br/> |
|1024  <br/> |Привязывать к параметрам расширений фигур.  <br/> |
|32768  <br/> |Прикрепление отключена.  <br/> |
|65536  <br/> |Привязывать к пересечениям.  <br/> |
   

