---
title: DocumentSettings_Type complexType (XML для Visio)
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
# <a name="documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="90694-102">DocumentSettings_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="90694-102">DocumentSettings_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="90694-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="90694-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90694-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="90694-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="90694-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="90694-105">**Schema file**</span></span> <br/> |<span data-ttu-id="90694-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="90694-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="90694-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="90694-107">**Extension base**</span></span> <br/> |<span data-ttu-id="90694-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="90694-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="90694-109">Определение</span><span class="sxs-lookup"><span data-stu-id="90694-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="90694-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="90694-110">Elements and attributes</span></span>

<span data-ttu-id="90694-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="90694-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="90694-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="90694-112">Child elements</span></span>

|<span data-ttu-id="90694-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="90694-113">**Element**</span></span>|<span data-ttu-id="90694-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="90694-114">**Type**</span></span>|<span data-ttu-id="90694-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90694-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="90694-116">аттачедтулбарс</span><span class="sxs-lookup"><span data-stu-id="90694-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-117">AttachedToolbars_Type</span><span class="sxs-lookup"><span data-stu-id="90694-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="90694-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-119">CustomMenusFile_Type</span><span class="sxs-lookup"><span data-stu-id="90694-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="90694-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-121">CustomToolbarsFile_Type</span><span class="sxs-lookup"><span data-stu-id="90694-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="90694-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-123">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="90694-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="90694-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-125">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="90694-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-126">протектбкгндс</span><span class="sxs-lookup"><span data-stu-id="90694-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-127">ProtectBkgnds_Type</span><span class="sxs-lookup"><span data-stu-id="90694-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-128">протектмастерс</span><span class="sxs-lookup"><span data-stu-id="90694-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-129">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="90694-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-130">протектшапес</span><span class="sxs-lookup"><span data-stu-id="90694-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-131">ProtectShapes_Type</span><span class="sxs-lookup"><span data-stu-id="90694-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-132">протектстилес</span><span class="sxs-lookup"><span data-stu-id="90694-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-133">ProtectStyles_Type</span><span class="sxs-lookup"><span data-stu-id="90694-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="90694-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-135">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="90694-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="90694-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-137">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="90694-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="90694-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="90694-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="90694-139">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="90694-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="90694-140">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="90694-140">Attributes</span></span>

|<span data-ttu-id="90694-141">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="90694-141">**Attribute**</span></span>|<span data-ttu-id="90694-142">**Тип**</span><span class="sxs-lookup"><span data-stu-id="90694-142">**Type**</span></span>|<span data-ttu-id="90694-143">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="90694-143">**Required**</span></span>|<span data-ttu-id="90694-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90694-144">**Description**</span></span>|<span data-ttu-id="90694-145">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="90694-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="90694-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="90694-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="90694-147">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="90694-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="90694-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="90694-148">optional</span></span>  <br/> ||<span data-ttu-id="90694-149">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="90694-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="90694-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="90694-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="90694-151">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="90694-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="90694-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="90694-152">optional</span></span>  <br/> ||<span data-ttu-id="90694-153">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="90694-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="90694-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="90694-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="90694-155">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="90694-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="90694-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="90694-156">optional</span></span>  <br/> ||<span data-ttu-id="90694-157">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="90694-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="90694-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="90694-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="90694-159">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="90694-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="90694-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="90694-160">optional</span></span>  <br/> ||<span data-ttu-id="90694-161">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="90694-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="90694-162">Навышена</span><span class="sxs-lookup"><span data-stu-id="90694-162">TopPage</span></span>  <br/> |<span data-ttu-id="90694-163">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="90694-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="90694-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="90694-164">optional</span></span>  <br/> ||<span data-ttu-id="90694-165">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="90694-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

