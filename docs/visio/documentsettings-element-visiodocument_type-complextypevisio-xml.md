---
title: Элемент DocumentSettings (VisioDocument_Type complexType) (Visio XML)
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
# <a name="documentsettings-element-visiodocument_type-complextype-visio-xml"></a>Элемент DocumentSettings (VisioDocument_Type complexType) (Visio XML)

Содержит элементы, определяющие параметры документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |document.xml  <br/> |
   
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
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Корневой элемент документа Microsoft Visio.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Файл MIME (multipurpose Internet Mail Extensions), закодированный в microsoft Visio user interface (VSU), представляющий настраиваемые панели инструментов.  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Содержит имя файла пользовательского интерфейса Microsoft Visio (VSU), который определяет настраиваемые меню и ускорители для документа.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Содержит имя файла пользовательского интерфейса Microsoft Visio (VSU), который определяет настраиваемые панели инструментов и панели состояния для документа.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Указывает, включена ли функция динамической сетки для документа или окна.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, к которые фигуры примеся, когда в документе включено приклейка.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Указывает, может ли пользователь удалять или редактировать фоновые страницы.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Указывает, может ли пользователь создавать, редактировать или удалять хозяинов. Независимо от этого параметра пользователь по-прежнему может создавать экземпляры этастеров.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Указывает, может ли пользователь выбирать фигуры, для элемента LockSelect для элемента **"LockSelect"** установлено 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Указывает, может ли пользователь создавать или редактировать стили.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **SnapAngle.**  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Указывает, включен ли определенный параметр расширения оснастки для активного окна.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Указывает объекты, которые фигуры оснастки, когда оснастка активна в окне.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ИД элемента **StyleSheet.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ИД элемента **StyleSheet.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ИД элемента **StyleSheet.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ИД элемента **StyleSheet.**  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|TopPage  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает ИД страницы, которая должна отображаться при открытом документе в Microsoft Visio.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

