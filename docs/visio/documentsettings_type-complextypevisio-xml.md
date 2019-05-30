---
title: Документсеттингс_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 0ec1f0dc21d7795e659fcdb512a912a00d1aacd6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540016"
---
# <a name="documentsettingstype-complextype-visio-xml"></a>Документсеттингс_типе complexType (XML для Visio)

## <a name="type-information"></a>Сведения о типе

|||
|:-----|:-----|
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Файл схемы** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Базовый элемент расширения** <br/> |Отсутствует  <br/> |
   
## <a name="definition"></a>Определение

```XML
          <xs:complexType name="DocumentSettings_Type">
          
          <xs:all>
    <xs:element name="GlueSettings"  type="GlueSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapSettings"  type="SnapSettings_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapExtensions"  type="SnapExtensions_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="SnapAngles"  type="SnapAngles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DynamicGridEnabled"  type="DynamicGridEnabled_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectStyles"  type="ProtectStyles_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectShapes"  type="ProtectShapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectMasters"  type="ProtectMasters_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ProtectBkgnds"  type="ProtectBkgnds_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomMenusFile"  type="CustomMenusFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CustomToolbarsFile"  type="CustomToolbarsFile_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="AttachedToolbars"  type="AttachedToolbars_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="TopPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultTextStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultLineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultFillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DefaultGuideStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Аттачедтулбарс](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Аттачедтулбарс_типе](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[CustomMenusFile](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Кустомменусфиле_типе](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[CustomToolbarsFile](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Кустомтулбарсфиле_типе](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[DynamicGridEnabled](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Динамикгриденаблед_типе](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[GlueSettings](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Глуесеттингс_типе](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[Протектбкгндс](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Протектбкгндс_типе](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[Протектмастерс](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Протектмастерс_типе](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[Протектшапес](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Протектшапес_типе](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[Протектстилес](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Протектстилес_типе](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[SnapAngles](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Снапанглес_типе](snapangles_type-complextypevisio-xml.md) <br/> ||
|[SnapExtensions](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Снапекстенсионс_типе](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[SnapSettings](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[Снапсеттингс_типе](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|DefaultFillStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|DefaultGuideStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|DefaultLineStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|DefaultTextStyle  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
|Навышена  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> ||Значения типа XSD: Унсигнединт.  <br/> |
   

