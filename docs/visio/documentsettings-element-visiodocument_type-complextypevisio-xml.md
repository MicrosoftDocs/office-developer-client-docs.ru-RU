---
title: Элемент Документсеттингс (VisioDocument_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Содержит элементы, определяющие параметры документа.
ms.openlocfilehash: 0d8e0809afae7b3de059166343577bb58f0eb01b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540072"
---
# <a name="documentsettings-element-visiodocument_type-complextype-visio-xml"></a>Элемент Документсеттингс (VisioDocument_Type complexType) (XML для Visio)

Содержит элементы, определяющие параметры документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DocumentSettings" type="DocumentSettings_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[висиодокумент](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Корневой элемент документа Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[аттачедтулбарс](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Зашифрованный в формате MIME файл пользовательского интерфейса Microsoft Visio (VSU), представляющий настраиваемые панели инструментов.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Содержит имя файла пользовательского интерфейса Microsoft Visio (VSU), определяющего настраиваемые меню и ускорители для документа.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Содержит имя файла пользовательского интерфейса Microsoft Visio (VSU), которое определяет настраиваемые панели инструментов и строки состояния документа.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Указывает, включена ли динамическая сетка для документа или окна.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, на которые фигуры привязываются при включении параметра приклеивание в документе.  <br/> |
|[протектбкгндс](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Указывает, запрещается ли пользователю удалять или редактировать фоновые страницы.  <br/> |
|[протектмастерс](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Указывает, запрещено ли создавать, редактировать или удалять образцы. Независимо от этого параметра, пользователь по-прежнему может создавать экземпляры образцов.  <br/> |
|[протектшапес](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Указывает, запрещается ли пользователю выбирать фигуры, для которых для элемента **LockSelect** задано значение 1.  <br/> |
|[протектстилес](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Указывает, запрещено ли пользователю создавать или редактировать стили.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **снапангле** .  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Указывает, включен или отключен указанный параметр расширения привязки для активного окна.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, к которым привязываются фигуры при активации привязки в окне.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор элемента **StyleSheet** .  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|DefaultGuideStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор элемента **StyleSheet** .  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|DefaultLineStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор элемента **StyleSheet** .  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|DefaultTextStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает идентификатор элемента **StyleSheet** .  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Навышена  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Указывает идентификатор страницы, которая будет отображаться при открытии документа в Microsoft Visio.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
   

