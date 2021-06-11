---
title: Window_Type ComplexType (Visio XML)
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
# <a name="window_type-complextype-visio-xml"></a><span data-ttu-id="9da0b-102">Window_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9da0b-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9da0b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9da0b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9da0b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9da0b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9da0b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9da0b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9da0b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9da0b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9da0b-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="9da0b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9da0b-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="9da0b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9da0b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9da0b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9da0b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9da0b-110">Elements and attributes</span></span>

<span data-ttu-id="9da0b-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9da0b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9da0b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9da0b-112">Child elements</span></span>

|<span data-ttu-id="9da0b-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9da0b-113">**Element**</span></span>|<span data-ttu-id="9da0b-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9da0b-114">**Type**</span></span>|<span data-ttu-id="9da0b-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9da0b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9da0b-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="9da0b-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="9da0b-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="9da0b-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="9da0b-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="9da0b-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="9da0b-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="9da0b-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="9da0b-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="9da0b-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="9da0b-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="9da0b-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="9da0b-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="9da0b-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="9da0b-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9da0b-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="9da0b-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9da0b-142">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9da0b-142">Attributes</span></span>

|<span data-ttu-id="9da0b-143">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9da0b-143">**Attribute**</span></span>|<span data-ttu-id="9da0b-144">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9da0b-144">**Type**</span></span>|<span data-ttu-id="9da0b-145">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9da0b-145">**Required**</span></span>|<span data-ttu-id="9da0b-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9da0b-146">**Description**</span></span>|<span data-ttu-id="9da0b-147">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9da0b-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9da0b-148">Container</span><span class="sxs-lookup"><span data-stu-id="9da0b-148">Container</span></span>  <br/> |<span data-ttu-id="9da0b-149">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-150">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="9da0b-152">ContainerType</span></span>  <br/> |<span data-ttu-id="9da0b-153">xsd:token</span><span class="sxs-lookup"><span data-stu-id="9da0b-153">xsd:token</span></span>  <br/> |<span data-ttu-id="9da0b-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-154">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-155">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="9da0b-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-156">Document</span><span class="sxs-lookup"><span data-stu-id="9da0b-156">Document</span></span>  <br/> |<span data-ttu-id="9da0b-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9da0b-157">xsd:string</span></span>  <br/> |<span data-ttu-id="9da0b-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-158">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-159">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9da0b-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-160">ID</span><span class="sxs-lookup"><span data-stu-id="9da0b-160">ID</span></span>  <br/> |<span data-ttu-id="9da0b-161">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-162">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-162">required</span></span>  <br/> ||<span data-ttu-id="9da0b-163">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-164">Master</span><span class="sxs-lookup"><span data-stu-id="9da0b-164">Master</span></span>  <br/> |<span data-ttu-id="9da0b-165">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-166">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-167">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-168">Page</span><span class="sxs-lookup"><span data-stu-id="9da0b-168">Page</span></span>  <br/> |<span data-ttu-id="9da0b-169">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-170">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-171">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="9da0b-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="9da0b-173">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-174">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-175">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="9da0b-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="9da0b-177">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9da0b-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9da0b-178">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-178">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-179">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9da0b-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-180">Таблица</span><span class="sxs-lookup"><span data-stu-id="9da0b-180">Sheet</span></span>  <br/> |<span data-ttu-id="9da0b-181">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-182">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-182">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-183">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="9da0b-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="9da0b-185">xsd:double</span><span class="sxs-lookup"><span data-stu-id="9da0b-185">xsd:double</span></span>  <br/> |<span data-ttu-id="9da0b-186">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-186">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-187">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="9da0b-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="9da0b-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="9da0b-189">xsd:double</span><span class="sxs-lookup"><span data-stu-id="9da0b-189">xsd:double</span></span>  <br/> |<span data-ttu-id="9da0b-190">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-190">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-191">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="9da0b-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="9da0b-192">ViewScale</span></span>  <br/> |<span data-ttu-id="9da0b-193">xsd:double</span><span class="sxs-lookup"><span data-stu-id="9da0b-193">xsd:double</span></span>  <br/> |<span data-ttu-id="9da0b-194">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-194">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-195">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="9da0b-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="9da0b-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="9da0b-197">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-198">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-198">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-199">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="9da0b-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="9da0b-201">xsd:short</span><span class="sxs-lookup"><span data-stu-id="9da0b-201">xsd:short</span></span>  <br/> |<span data-ttu-id="9da0b-202">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-202">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-203">Значения xsd:short типа.</span><span class="sxs-lookup"><span data-stu-id="9da0b-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="9da0b-204">WindowState</span></span>  <br/> |<span data-ttu-id="9da0b-205">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-206">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-206">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-207">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="9da0b-208">WindowTop</span></span>  <br/> |<span data-ttu-id="9da0b-209">xsd:short</span><span class="sxs-lookup"><span data-stu-id="9da0b-209">xsd:short</span></span>  <br/> |<span data-ttu-id="9da0b-210">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-210">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-211">Значения xsd:short типа.</span><span class="sxs-lookup"><span data-stu-id="9da0b-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="9da0b-212">WindowType</span></span>  <br/> |<span data-ttu-id="9da0b-213">xsd:token</span><span class="sxs-lookup"><span data-stu-id="9da0b-213">xsd:token</span></span>  <br/> |<span data-ttu-id="9da0b-214">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-214">required</span></span>  <br/> ||<span data-ttu-id="9da0b-215">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="9da0b-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="9da0b-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="9da0b-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="9da0b-217">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9da0b-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9da0b-218">необязательный</span><span class="sxs-lookup"><span data-stu-id="9da0b-218">optional</span></span>  <br/> ||<span data-ttu-id="9da0b-219">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9da0b-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

