---
title: Документсеттингс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8fb61b5f-1bab-78b6-c56c-384e52609397
ms.openlocfilehash: 704591a2bf03f3eaf4d93b167475a8bae286da3e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349037"
---
# <a name="documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="906da-102">Документсеттингс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="906da-102">DocumentSettings_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="906da-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="906da-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="906da-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="906da-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="906da-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="906da-105">**Schema file**</span></span> <br/> |<span data-ttu-id="906da-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="906da-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="906da-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="906da-107">**Extension base**</span></span> <br/> |<span data-ttu-id="906da-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="906da-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="906da-109">Определение</span><span class="sxs-lookup"><span data-stu-id="906da-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="906da-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="906da-110">Elements and attributes</span></span>

<span data-ttu-id="906da-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="906da-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="906da-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="906da-112">Child elements</span></span>

|<span data-ttu-id="906da-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="906da-113">**Element**</span></span>|<span data-ttu-id="906da-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="906da-114">**Type**</span></span>|<span data-ttu-id="906da-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="906da-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="906da-116">Аттачедтулбарс</span><span class="sxs-lookup"><span data-stu-id="906da-116">AttachedToolbars</span></span>](attachedtoolbars-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-117">Аттачедтулбарс_типе</span><span class="sxs-lookup"><span data-stu-id="906da-117">AttachedToolbars_Type</span></span>](attachedtoolbars_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-118">CustomMenusFile</span><span class="sxs-lookup"><span data-stu-id="906da-118">CustomMenusFile</span></span>](custommenusfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-119">Кустомменусфиле_типе</span><span class="sxs-lookup"><span data-stu-id="906da-119">CustomMenusFile_Type</span></span>](custommenusfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-120">CustomToolbarsFile</span><span class="sxs-lookup"><span data-stu-id="906da-120">CustomToolbarsFile</span></span>](customtoolbarsfile-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-121">Кустомтулбарсфиле_типе</span><span class="sxs-lookup"><span data-stu-id="906da-121">CustomToolbarsFile_Type</span></span>](customtoolbarsfile_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-122">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="906da-122">DynamicGridEnabled</span></span>](dynamicgridenabled-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-123">Динамикгриденаблед_типе</span><span class="sxs-lookup"><span data-stu-id="906da-123">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-124">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="906da-124">GlueSettings</span></span>](gluesettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-125">Глуесеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="906da-125">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-126">Протектбкгндс</span><span class="sxs-lookup"><span data-stu-id="906da-126">ProtectBkgnds</span></span>](protectbkgnds-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-127">Протектбкгндс_типе</span><span class="sxs-lookup"><span data-stu-id="906da-127">ProtectBkgnds_Type</span></span>](protectbkgnds_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-128">Протектмастерс</span><span class="sxs-lookup"><span data-stu-id="906da-128">ProtectMasters</span></span>](protectmasters-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-129">Протектмастерс_типе</span><span class="sxs-lookup"><span data-stu-id="906da-129">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-130">Протектшапес</span><span class="sxs-lookup"><span data-stu-id="906da-130">ProtectShapes</span></span>](protectshapes-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-131">Протектшапес_типе</span><span class="sxs-lookup"><span data-stu-id="906da-131">ProtectShapes_Type</span></span>](protectshapes_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-132">Протектстилес</span><span class="sxs-lookup"><span data-stu-id="906da-132">ProtectStyles</span></span>](protectstyles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-133">Протектстилес_типе</span><span class="sxs-lookup"><span data-stu-id="906da-133">ProtectStyles_Type</span></span>](protectstyles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-134">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="906da-134">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-135">Снапанглес_типе</span><span class="sxs-lookup"><span data-stu-id="906da-135">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-136">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="906da-136">SnapExtensions</span></span>](snapextensions-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-137">Снапекстенсионс_типе</span><span class="sxs-lookup"><span data-stu-id="906da-137">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="906da-138">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="906da-138">SnapSettings</span></span>](snapsettings-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="906da-139">Снапсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="906da-139">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="906da-140">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="906da-140">Attributes</span></span>

|<span data-ttu-id="906da-141">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="906da-141">**Attribute**</span></span>|<span data-ttu-id="906da-142">**Тип**</span><span class="sxs-lookup"><span data-stu-id="906da-142">**Type**</span></span>|<span data-ttu-id="906da-143">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="906da-143">**Required**</span></span>|<span data-ttu-id="906da-144">**Описание**</span><span class="sxs-lookup"><span data-stu-id="906da-144">**Description**</span></span>|<span data-ttu-id="906da-145">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="906da-145">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="906da-146">DefaultFillStyle</span><span class="sxs-lookup"><span data-stu-id="906da-146">DefaultFillStyle</span></span>  <br/> |<span data-ttu-id="906da-147">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="906da-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="906da-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="906da-148">optional</span></span>  <br/> ||<span data-ttu-id="906da-149">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="906da-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="906da-150">DefaultGuideStyle</span><span class="sxs-lookup"><span data-stu-id="906da-150">DefaultGuideStyle</span></span>  <br/> |<span data-ttu-id="906da-151">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="906da-151">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="906da-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="906da-152">optional</span></span>  <br/> ||<span data-ttu-id="906da-153">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="906da-153">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="906da-154">DefaultLineStyle</span><span class="sxs-lookup"><span data-stu-id="906da-154">DefaultLineStyle</span></span>  <br/> |<span data-ttu-id="906da-155">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="906da-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="906da-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="906da-156">optional</span></span>  <br/> ||<span data-ttu-id="906da-157">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="906da-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="906da-158">DefaultTextStyle</span><span class="sxs-lookup"><span data-stu-id="906da-158">DefaultTextStyle</span></span>  <br/> |<span data-ttu-id="906da-159">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="906da-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="906da-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="906da-160">optional</span></span>  <br/> ||<span data-ttu-id="906da-161">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="906da-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="906da-162">Навышена</span><span class="sxs-lookup"><span data-stu-id="906da-162">TopPage</span></span>  <br/> |<span data-ttu-id="906da-163">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="906da-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="906da-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="906da-164">optional</span></span>  <br/> ||<span data-ttu-id="906da-165">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="906da-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

