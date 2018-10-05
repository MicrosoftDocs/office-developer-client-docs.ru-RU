---
title: Элемент DocumentSettings (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46712e1f-4e02-974f-c224-85db47666ae1
description: Содержит элементы, которые определяют параметры документов.
ms.openlocfilehash: e86dc5a0875006cb8bd1bbaffd36037a07fd5c0f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396472"
---
# <a name="documentsettings-element-visiodocumenttype-complextype-visio-xml"></a>Элемент DocumentSettings (VisioDocument_Type complexType) ('Visio XML»)

Содержит элементы, которые определяют параметры документов.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DocumentSettings_Type](documentsettings_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Document.XML  <br/> |
   
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
|[AttachedToolbars](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[AttachedToolbars_Type](attachedtoolbars_type-complextypevisio-xml.md) <br/> |Microsoft Visio пользовательского интерфейса (VSU) файл представляющие настраиваемые панели инструментов в кодировке MIME (Multipurpose Internet Mail Extensions).  <br/> |
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomMenusFile_Type](custommenusfile_type-complextypevisio-xml.md) <br/> |Содержит имя файла Microsoft Visio пользовательского интерфейса (.vsu), который определяет пользовательские меню и сочетания клавиш для документа.  <br/> |
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[CustomToolbarsFile_Type](customtoolbarsfile_type-complextypevisio-xml.md) <br/> |Содержит имя файла интерфейса (.vsu) пользователя Microsoft Visio, который определяет пользовательские панели инструментов и строки состояния для документа.  <br/> |
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[DynamicGridEnabled_Type](dynamicgridenabled_type-complextypevisio-xml.md) <br/> |Указывает, включена ли функция динамической таблицы для документа или окна.  <br/> |
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[GlueSettings_Type](gluesettings_type-complextypevisio-xml.md) <br/> |Определяет объекты, которые связывания фигуры на при включении связывающих в документе.  <br/> |
|[ProtectBkgnds](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectBkgnds_Type](protectbkgnds_type-complextypevisio-xml.md) <br/> |Указывает, является ли пользователь не сможет удаление или изменение фона страниц.  <br/> |
|[ProtectMasters](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectMasters_Type](protectmasters_type-complextypevisio-xml.md) <br/> |Указывает, является ли пользователь, которым запрещен создание, изменение и удаление шаблонов. Независимо от того, этот параметр, пользователь может по-прежнему создавать экземпляры образцов.  <br/> |
|[ProtectShapes](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectShapes_Type](protectshapes_type-complextypevisio-xml.md) <br/> |Указывает, является ли пользователь не сможет выбирать фигуры, которые имеют их **LockSelect** элемент, установите значение 1.  <br/> |
|[ProtectStyles](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[ProtectStyles_Type](protectstyles_type-complextypevisio-xml.md) <br/> |Указывает, является ли пользователь, которым запрещен создании или изменении стилей.  <br/> |
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapAngles_Type](snapangles_type-complextypevisio-xml.md) <br/> |Содержит коллекцию элементов **SnapAngle** .  <br/> |
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapExtensions_Type](snapextensions_type-complextypevisio-xml.md) <br/> |Указывает, будет ли параметр расширения с определенным оснастке включена или отключена для активного окна.  <br/> |
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[SnapSettings_Type](snapsettings_type-complextypevisio-xml.md) <br/> |Определяет объекты, которые привязать фигуры при привязка активна в окне.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор элемента **таблицы стилей** .  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DefaultGuideStyle  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор элемента **таблицы стилей** .  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DefaultLineStyle  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор элемента **таблицы стилей** .  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DefaultTextStyle  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Указывает идентификатор элемента **таблицы стилей** .  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|TopPage  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает идентификатор страницы, которое должно отображаться при открытии документа с Microsoft Visio.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
   

