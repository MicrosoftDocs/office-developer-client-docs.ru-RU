---
title: Window_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c514ce79-0920-4f1b-5332-0bdef146e802
ms.openlocfilehash: dc4dda48c037f7af03ee22a07bee288ce5d30872
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815170"
---
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="70215-102">Window_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="70215-102">Window_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="70215-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="70215-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="70215-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="70215-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="70215-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="70215-105">**Schema file**</span></span> <br/> |<span data-ttu-id="70215-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="70215-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="70215-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="70215-107">**Extension base**</span></span> <br/> |<span data-ttu-id="70215-108">Нет</span><span class="sxs-lookup"><span data-stu-id="70215-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="70215-109">Определение</span><span class="sxs-lookup"><span data-stu-id="70215-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="70215-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="70215-110">Elements and attributes</span></span>

<span data-ttu-id="70215-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="70215-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="70215-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="70215-112">Child elements</span></span>

|<span data-ttu-id="70215-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="70215-113">**Element**</span></span>|<span data-ttu-id="70215-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="70215-114">**Type**</span></span>|<span data-ttu-id="70215-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="70215-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="70215-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="70215-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-117">DynamicGridEnabled_Type</span><span class="sxs-lookup"><span data-stu-id="70215-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="70215-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-119">GlueSettings_Type</span><span class="sxs-lookup"><span data-stu-id="70215-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-120">ShowConnectionPoints</span><span class="sxs-lookup"><span data-stu-id="70215-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-121">ShowConnectionPoints_Type</span><span class="sxs-lookup"><span data-stu-id="70215-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="70215-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-123">ShowGrid_Type</span><span class="sxs-lookup"><span data-stu-id="70215-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="70215-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-125">ShowGuides_Type</span><span class="sxs-lookup"><span data-stu-id="70215-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="70215-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-127">ShowPageBreaks_Type</span><span class="sxs-lookup"><span data-stu-id="70215-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="70215-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-129">ShowRulers_Type</span><span class="sxs-lookup"><span data-stu-id="70215-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="70215-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-131">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="70215-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="70215-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-133">SnapExtensions_Type</span><span class="sxs-lookup"><span data-stu-id="70215-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="70215-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-135">SnapSettings_Type</span><span class="sxs-lookup"><span data-stu-id="70215-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-136">StencilGroup</span><span class="sxs-lookup"><span data-stu-id="70215-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-137">StencilGroup_Type</span><span class="sxs-lookup"><span data-stu-id="70215-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-138">StencilGroupPos</span><span class="sxs-lookup"><span data-stu-id="70215-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-139">StencilGroupPos_Type</span><span class="sxs-lookup"><span data-stu-id="70215-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="70215-140">TabSplitterPos</span><span class="sxs-lookup"><span data-stu-id="70215-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="70215-141">TabSplitterPos_Type</span><span class="sxs-lookup"><span data-stu-id="70215-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="70215-142">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="70215-142">Attributes</span></span>

|<span data-ttu-id="70215-143">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="70215-143">**Attribute**</span></span>|<span data-ttu-id="70215-144">**Тип**</span><span class="sxs-lookup"><span data-stu-id="70215-144">**Type**</span></span>|<span data-ttu-id="70215-145">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="70215-145">**Required**</span></span>|<span data-ttu-id="70215-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="70215-146">**Description**</span></span>|<span data-ttu-id="70215-147">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="70215-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="70215-148">Контейнер</span><span class="sxs-lookup"><span data-stu-id="70215-148">Container</span></span>  <br/> |<span data-ttu-id="70215-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-150">optional</span></span>  <br/> ||<span data-ttu-id="70215-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="70215-152">ContainerType</span></span>  <br/> |<span data-ttu-id="70215-153">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="70215-153">xsd:token</span></span>  <br/> |<span data-ttu-id="70215-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-154">optional</span></span>  <br/> ||<span data-ttu-id="70215-155">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="70215-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="70215-156">Документ</span><span class="sxs-lookup"><span data-stu-id="70215-156">Document</span></span>  <br/> |<span data-ttu-id="70215-157">XSD:String</span><span class="sxs-lookup"><span data-stu-id="70215-157">xsd:string</span></span>  <br/> |<span data-ttu-id="70215-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-158">optional</span></span>  <br/> ||<span data-ttu-id="70215-159">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="70215-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="70215-160">ID</span><span class="sxs-lookup"><span data-stu-id="70215-160">ID</span></span>  <br/> |<span data-ttu-id="70215-161">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-162">Обязательный</span><span class="sxs-lookup"><span data-stu-id="70215-162">required</span></span>  <br/> ||<span data-ttu-id="70215-163">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-164">Master</span><span class="sxs-lookup"><span data-stu-id="70215-164">Master</span></span>  <br/> |<span data-ttu-id="70215-165">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-166">optional</span></span>  <br/> ||<span data-ttu-id="70215-167">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-168">Page</span><span class="sxs-lookup"><span data-stu-id="70215-168">Page</span></span>  <br/> |<span data-ttu-id="70215-169">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-170">optional</span></span>  <br/> ||<span data-ttu-id="70215-171">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="70215-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="70215-173">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-174">optional</span></span>  <br/> ||<span data-ttu-id="70215-175">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="70215-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="70215-177">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="70215-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="70215-178">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-178">optional</span></span>  <br/> ||<span data-ttu-id="70215-179">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="70215-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="70215-180">Лист</span><span class="sxs-lookup"><span data-stu-id="70215-180">Sheet</span></span>  <br/> |<span data-ttu-id="70215-181">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-182">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-182">optional</span></span>  <br/> ||<span data-ttu-id="70215-183">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-184">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="70215-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="70215-185">XSD: double</span><span class="sxs-lookup"><span data-stu-id="70215-185">xsd:double</span></span>  <br/> |<span data-ttu-id="70215-186">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-186">optional</span></span>  <br/> ||<span data-ttu-id="70215-187">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="70215-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="70215-188">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="70215-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="70215-189">XSD: double</span><span class="sxs-lookup"><span data-stu-id="70215-189">xsd:double</span></span>  <br/> |<span data-ttu-id="70215-190">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-190">optional</span></span>  <br/> ||<span data-ttu-id="70215-191">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="70215-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="70215-192">ViewScale</span><span class="sxs-lookup"><span data-stu-id="70215-192">ViewScale</span></span>  <br/> |<span data-ttu-id="70215-193">XSD: double</span><span class="sxs-lookup"><span data-stu-id="70215-193">xsd:double</span></span>  <br/> |<span data-ttu-id="70215-194">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-194">optional</span></span>  <br/> ||<span data-ttu-id="70215-195">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="70215-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="70215-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="70215-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="70215-197">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-198">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-198">optional</span></span>  <br/> ||<span data-ttu-id="70215-199">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="70215-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="70215-201">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="70215-201">xsd:short</span></span>  <br/> |<span data-ttu-id="70215-202">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-202">optional</span></span>  <br/> ||<span data-ttu-id="70215-203">Значения типа xsd:short.</span><span class="sxs-lookup"><span data-stu-id="70215-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="70215-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="70215-204">WindowState</span></span>  <br/> |<span data-ttu-id="70215-205">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-206">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-206">optional</span></span>  <br/> ||<span data-ttu-id="70215-207">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="70215-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="70215-208">WindowTop</span></span>  <br/> |<span data-ttu-id="70215-209">XSD:Short</span><span class="sxs-lookup"><span data-stu-id="70215-209">xsd:short</span></span>  <br/> |<span data-ttu-id="70215-210">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-210">optional</span></span>  <br/> ||<span data-ttu-id="70215-211">Значения типа xsd:short.</span><span class="sxs-lookup"><span data-stu-id="70215-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="70215-212">WindowType</span><span class="sxs-lookup"><span data-stu-id="70215-212">WindowType</span></span>  <br/> |<span data-ttu-id="70215-213">XSD:Token</span><span class="sxs-lookup"><span data-stu-id="70215-213">xsd:token</span></span>  <br/> |<span data-ttu-id="70215-214">Обязательный</span><span class="sxs-lookup"><span data-stu-id="70215-214">required</span></span>  <br/> ||<span data-ttu-id="70215-215">Значения типа xsd:token.</span><span class="sxs-lookup"><span data-stu-id="70215-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="70215-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="70215-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="70215-217">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="70215-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="70215-218">необязательный</span><span class="sxs-lookup"><span data-stu-id="70215-218">optional</span></span>  <br/> ||<span data-ttu-id="70215-219">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="70215-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

