---
title: Window_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: 08b65a5f0e108c5503e29c7e195d681d0a343521
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538454"
---
# <a name="window_type-complextype-visio-xml"></a><span data-ttu-id="ee872-102">Window_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="ee872-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ee872-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ee872-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee872-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ee872-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ee872-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ee872-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ee872-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ee872-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ee872-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ee872-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ee872-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ee872-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ee872-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ee872-109">Definition</span></span>

```XML
          <xs:complexType name="Window_Type">
          
          <xs:sequence>
    <xs:element name="StencilGroup"  type="StencilGroup_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="StencilGroupPos"  type="StencilGroupPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowRulers"  type="ShowRulers_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGrid"  type="ShowGrid_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowPageBreaks"  type="ShowPageBreaks_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowGuides"  type="ShowGuides_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ShowConnectionPoints"  type="ShowConnectionPoints_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
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
    
    <xs:element name="TabSplitterPos"  type="TabSplitterPos_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="WindowType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="WindowState"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Document"
  type="xsd:string"
    />
    <xs:attribute name="WindowLeft"
  type="xsd:short"
    />
    <xs:attribute name="WindowTop"
  type="xsd:short"
    />
    <xs:attribute name="WindowWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="WindowHeight"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ContainerType"
  type="xsd:token"
    />
    <xs:attribute name="Container"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Sheet"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReadOnly"
  type="xsd:boolean"
    />
    <xs:attribute name="ParentWindow"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Page"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ee872-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ee872-110">Elements and attributes</span></span>

<span data-ttu-id="ee872-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ee872-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ee872-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ee872-112">Child elements</span></span>

|<span data-ttu-id="ee872-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ee872-113">**Element**</span></span>|<span data-ttu-id="ee872-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ee872-114">**Type**</span></span>|<span data-ttu-id="ee872-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee872-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ee872-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="ee872-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="ee872-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-120">шовконнектионпоинтс</span><span class="sxs-lookup"><span data-stu-id="ee872-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="ee872-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="ee872-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="ee872-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="ee872-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="ee872-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="ee872-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="ee872-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-136">стенЦилграуп</span><span class="sxs-lookup"><span data-stu-id="ee872-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-138">стенЦилграуппос</span><span class="sxs-lookup"><span data-stu-id="ee872-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ee872-140">табсплиттерпос</span><span class="sxs-lookup"><span data-stu-id="ee872-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ee872-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="ee872-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ee872-142">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ee872-142">Attributes</span></span>

|<span data-ttu-id="ee872-143">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ee872-143">**Attribute**</span></span>|<span data-ttu-id="ee872-144">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ee872-144">**Type**</span></span>|<span data-ttu-id="ee872-145">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ee872-145">**Required**</span></span>|<span data-ttu-id="ee872-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ee872-146">**Description**</span></span>|<span data-ttu-id="ee872-147">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ee872-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ee872-148">Container</span><span class="sxs-lookup"><span data-stu-id="ee872-148">Container</span></span>  <br/> |<span data-ttu-id="ee872-149">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-150">optional</span></span>  <br/> ||<span data-ttu-id="ee872-151">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="ee872-152">ContainerType</span></span>  <br/> |<span data-ttu-id="ee872-153">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="ee872-153">xsd:token</span></span>  <br/> |<span data-ttu-id="ee872-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-154">optional</span></span>  <br/> ||<span data-ttu-id="ee872-155">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="ee872-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ee872-156">Document</span><span class="sxs-lookup"><span data-stu-id="ee872-156">Document</span></span>  <br/> |<span data-ttu-id="ee872-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ee872-157">xsd:string</span></span>  <br/> |<span data-ttu-id="ee872-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-158">optional</span></span>  <br/> ||<span data-ttu-id="ee872-159">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ee872-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ee872-160">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="ee872-160">ID</span></span>  <br/> |<span data-ttu-id="ee872-161">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-162">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-162">required</span></span>  <br/> ||<span data-ttu-id="ee872-163">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-164">Master</span><span class="sxs-lookup"><span data-stu-id="ee872-164">Master</span></span>  <br/> |<span data-ttu-id="ee872-165">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-166">optional</span></span>  <br/> ||<span data-ttu-id="ee872-167">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-168">Page</span><span class="sxs-lookup"><span data-stu-id="ee872-168">Page</span></span>  <br/> |<span data-ttu-id="ee872-169">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-170">optional</span></span>  <br/> ||<span data-ttu-id="ee872-171">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="ee872-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="ee872-173">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-174">optional</span></span>  <br/> ||<span data-ttu-id="ee872-175">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ee872-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="ee872-177">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ee872-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ee872-178">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-178">optional</span></span>  <br/> ||<span data-ttu-id="ee872-179">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ee872-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ee872-180">Таблица</span><span class="sxs-lookup"><span data-stu-id="ee872-180">Sheet</span></span>  <br/> |<span data-ttu-id="ee872-181">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-182">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-182">optional</span></span>  <br/> ||<span data-ttu-id="ee872-183">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-184">виевцентеркс</span><span class="sxs-lookup"><span data-stu-id="ee872-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="ee872-185">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="ee872-185">xsd:double</span></span>  <br/> |<span data-ttu-id="ee872-186">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-186">optional</span></span>  <br/> ||<span data-ttu-id="ee872-187">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="ee872-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee872-188">виевцентери</span><span class="sxs-lookup"><span data-stu-id="ee872-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="ee872-189">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="ee872-189">xsd:double</span></span>  <br/> |<span data-ttu-id="ee872-190">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-190">optional</span></span>  <br/> ||<span data-ttu-id="ee872-191">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="ee872-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee872-192">виевскале</span><span class="sxs-lookup"><span data-stu-id="ee872-192">ViewScale</span></span>  <br/> |<span data-ttu-id="ee872-193">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="ee872-193">xsd:double</span></span>  <br/> |<span data-ttu-id="ee872-194">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-194">optional</span></span>  <br/> ||<span data-ttu-id="ee872-195">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="ee872-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ee872-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="ee872-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="ee872-197">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-198">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-198">optional</span></span>  <br/> ||<span data-ttu-id="ee872-199">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="ee872-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="ee872-201">XSD: Short</span><span class="sxs-lookup"><span data-stu-id="ee872-201">xsd:short</span></span>  <br/> |<span data-ttu-id="ee872-202">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-202">optional</span></span>  <br/> ||<span data-ttu-id="ee872-203">Значения типа XSD: Short.</span><span class="sxs-lookup"><span data-stu-id="ee872-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="ee872-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="ee872-204">WindowState</span></span>  <br/> |<span data-ttu-id="ee872-205">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-206">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-206">optional</span></span>  <br/> ||<span data-ttu-id="ee872-207">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ee872-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="ee872-208">WindowTop</span></span>  <br/> |<span data-ttu-id="ee872-209">XSD: Short</span><span class="sxs-lookup"><span data-stu-id="ee872-209">xsd:short</span></span>  <br/> |<span data-ttu-id="ee872-210">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-210">optional</span></span>  <br/> ||<span data-ttu-id="ee872-211">Значения типа XSD: Short.</span><span class="sxs-lookup"><span data-stu-id="ee872-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="ee872-212">виндовтипе</span><span class="sxs-lookup"><span data-stu-id="ee872-212">WindowType</span></span>  <br/> |<span data-ttu-id="ee872-213">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="ee872-213">xsd:token</span></span>  <br/> |<span data-ttu-id="ee872-214">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-214">required</span></span>  <br/> ||<span data-ttu-id="ee872-215">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="ee872-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="ee872-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="ee872-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="ee872-217">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ee872-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ee872-218">необязательный</span><span class="sxs-lookup"><span data-stu-id="ee872-218">optional</span></span>  <br/> ||<span data-ttu-id="ee872-219">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ee872-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

