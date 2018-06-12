---
title: DocumentSettings_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 93623133e7d7fd096e063f0d9d5227d65dcc4736
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813653"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="ec15a-102">DocumentSettings_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ec15a-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ec15a-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ec15a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec15a-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ec15a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec15a-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ec15a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec15a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ec15a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec15a-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="ec15a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec15a-108">Нет</span><span class="sxs-lookup"><span data-stu-id="ec15a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec15a-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ec15a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec15a-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec15a-110">Elements and attributes</span></span>

<span data-ttu-id="ec15a-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ec15a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec15a-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ec15a-112">Child elements</span></span>

|<span data-ttu-id="ec15a-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ec15a-113">**Element**</span></span>|<span data-ttu-id="ec15a-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec15a-114">**Type**</span></span>|<span data-ttu-id="ec15a-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec15a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ec15a-116">AttachedToolbars</span><span class="sxs-lookup"><span data-stu-id="ec15a-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="ec15a-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="ec15a-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="ec15a-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="ec15a-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-126">ProtectBkgnds</span><span class="sxs-lookup"><span data-stu-id="ec15a-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-128">ProtectMasters</span><span class="sxs-lookup"><span data-stu-id="ec15a-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-130">ProtectShapes</span><span class="sxs-lookup"><span data-stu-id="ec15a-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-132">ProtectStyles</span><span class="sxs-lookup"><span data-stu-id="ec15a-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="ec15a-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="ec15a-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec15a-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="ec15a-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec15a-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ec15a-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ec15a-140">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec15a-140">Attributes</span></span>

|<span data-ttu-id="ec15a-141">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ec15a-141">**Attribute**</span></span>|<span data-ttu-id="ec15a-142">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec15a-142">**Type**</span></span>|<span data-ttu-id="ec15a-143">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="ec15a-143">**Required**</span></span>|<span data-ttu-id="ec15a-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec15a-144">**Description**</span></span>|<span data-ttu-id="ec15a-145">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ec15a-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec15a-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="ec15a-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="ec15a-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec15a-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec15a-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec15a-148">optional</span></span>  <br/> ||<span data-ttu-id="ec15a-149">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec15a-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec15a-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="ec15a-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="ec15a-151">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec15a-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec15a-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec15a-152">optional</span></span>  <br/> ||<span data-ttu-id="ec15a-153">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec15a-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec15a-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="ec15a-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="ec15a-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec15a-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec15a-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec15a-156">optional</span></span>  <br/> ||<span data-ttu-id="ec15a-157">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec15a-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec15a-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="ec15a-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="ec15a-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec15a-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec15a-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec15a-160">optional</span></span>  <br/> ||<span data-ttu-id="ec15a-161">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec15a-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec15a-162">TopPage</span><span class="sxs-lookup"><span data-stu-id="ec15a-162">TopPage</span></span>  <br/> |<span data-ttu-id="ec15a-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ec15a-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec15a-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec15a-164">optional</span></span>  <br/> ||<span data-ttu-id="ec15a-165">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ec15a-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

