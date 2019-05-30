---
title: Виндов_типе complexType (XML для Visio)
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
# <a name="windowtype-complextype-visio-xml"></a><span data-ttu-id="4770d-102">Виндов_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="4770d-102">Window_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4770d-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4770d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4770d-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4770d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4770d-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4770d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4770d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4770d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4770d-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4770d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4770d-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="4770d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4770d-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4770d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4770d-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4770d-110">Elements and attributes</span></span>

<span data-ttu-id="4770d-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4770d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4770d-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4770d-112">Child elements</span></span>

|<span data-ttu-id="4770d-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4770d-113">**Element**</span></span>|<span data-ttu-id="4770d-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4770d-114">**Type**</span></span>|<span data-ttu-id="4770d-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4770d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4770d-116">DynamicGridEnabled</span><span class="sxs-lookup"><span data-stu-id="4770d-116">DynamicGridEnabled</span></span>](dynamicgridenabled-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-117">Динамикгриденаблед_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-117">DynamicGridEnabled_Type</span></span>](dynamicgridenabled_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-118">GlueSettings</span><span class="sxs-lookup"><span data-stu-id="4770d-118">GlueSettings</span></span>](gluesettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-119">Глуесеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-119">GlueSettings_Type</span></span>](gluesettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-120">Шовконнектионпоинтс</span><span class="sxs-lookup"><span data-stu-id="4770d-120">ShowConnectionPoints</span></span>](showconnectionpoints-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-121">Шовконнектионпоинтс_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-121">ShowConnectionPoints_Type</span></span>](showconnectionpoints_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-122">ShowGrid</span><span class="sxs-lookup"><span data-stu-id="4770d-122">ShowGrid</span></span>](showgrid-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-123">Шовгрид_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-123">ShowGrid_Type</span></span>](showgrid_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-124">ShowGuides</span><span class="sxs-lookup"><span data-stu-id="4770d-124">ShowGuides</span></span>](showguides-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-125">Шовгуидес_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-125">ShowGuides_Type</span></span>](showguides_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-126">ShowPageBreaks</span><span class="sxs-lookup"><span data-stu-id="4770d-126">ShowPageBreaks</span></span>](showpagebreaks-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-127">Шовпажебреакс_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-127">ShowPageBreaks_Type</span></span>](showpagebreaks_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-128">ShowRulers</span><span class="sxs-lookup"><span data-stu-id="4770d-128">ShowRulers</span></span>](showrulers-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-129">Шоврулерс_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-129">ShowRulers_Type</span></span>](showrulers_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-130">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="4770d-130">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-131">Снапанглес_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-131">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-132">SnapExtensions</span><span class="sxs-lookup"><span data-stu-id="4770d-132">SnapExtensions</span></span>](snapextensions-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-133">Снапекстенсионс_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-133">SnapExtensions_Type</span></span>](snapextensions_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-134">SnapSettings</span><span class="sxs-lookup"><span data-stu-id="4770d-134">SnapSettings</span></span>](snapsettings-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-135">Снапсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-135">SnapSettings_Type</span></span>](snapsettings_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-136">СтенЦилграуп</span><span class="sxs-lookup"><span data-stu-id="4770d-136">StencilGroup</span></span>](stencilgroup-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-137">СтенЦилграуп_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-137">StencilGroup_Type</span></span>](stencilgroup_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-138">СтенЦилграуппос</span><span class="sxs-lookup"><span data-stu-id="4770d-138">StencilGroupPos</span></span>](stencilgrouppos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-139">СтенЦилграуппос_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-139">StencilGroupPos_Type</span></span>](stencilgrouppos_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="4770d-140">Табсплиттерпос</span><span class="sxs-lookup"><span data-stu-id="4770d-140">TabSplitterPos</span></span>](tabsplitterpos-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4770d-141">Табсплиттерпос_типе</span><span class="sxs-lookup"><span data-stu-id="4770d-141">TabSplitterPos_Type</span></span>](tabsplitterpos_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4770d-142">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4770d-142">Attributes</span></span>

|<span data-ttu-id="4770d-143">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4770d-143">**Attribute**</span></span>|<span data-ttu-id="4770d-144">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4770d-144">**Type**</span></span>|<span data-ttu-id="4770d-145">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4770d-145">**Required**</span></span>|<span data-ttu-id="4770d-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4770d-146">**Description**</span></span>|<span data-ttu-id="4770d-147">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4770d-147">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4770d-148">Container</span><span class="sxs-lookup"><span data-stu-id="4770d-148">Container</span></span>  <br/> |<span data-ttu-id="4770d-149">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-150">optional</span></span>  <br/> ||<span data-ttu-id="4770d-151">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-152">ContainerType</span><span class="sxs-lookup"><span data-stu-id="4770d-152">ContainerType</span></span>  <br/> |<span data-ttu-id="4770d-153">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="4770d-153">xsd:token</span></span>  <br/> |<span data-ttu-id="4770d-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-154">optional</span></span>  <br/> ||<span data-ttu-id="4770d-155">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="4770d-155">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="4770d-156">Document</span><span class="sxs-lookup"><span data-stu-id="4770d-156">Document</span></span>  <br/> |<span data-ttu-id="4770d-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4770d-157">xsd:string</span></span>  <br/> |<span data-ttu-id="4770d-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-158">optional</span></span>  <br/> ||<span data-ttu-id="4770d-159">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4770d-159">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4770d-160">ID</span><span class="sxs-lookup"><span data-stu-id="4770d-160">ID</span></span>  <br/> |<span data-ttu-id="4770d-161">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-161">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-162">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-162">required</span></span>  <br/> ||<span data-ttu-id="4770d-163">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-163">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-164">Master</span><span class="sxs-lookup"><span data-stu-id="4770d-164">Master</span></span>  <br/> |<span data-ttu-id="4770d-165">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-165">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-166">optional</span></span>  <br/> ||<span data-ttu-id="4770d-167">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-168">Page</span><span class="sxs-lookup"><span data-stu-id="4770d-168">Page</span></span>  <br/> |<span data-ttu-id="4770d-169">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-169">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-170">optional</span></span>  <br/> ||<span data-ttu-id="4770d-171">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-171">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-172">ParentWindow</span><span class="sxs-lookup"><span data-stu-id="4770d-172">ParentWindow</span></span>  <br/> |<span data-ttu-id="4770d-173">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-173">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-174">optional</span></span>  <br/> ||<span data-ttu-id="4770d-175">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-175">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-176">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4770d-176">ReadOnly</span></span>  <br/> |<span data-ttu-id="4770d-177">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="4770d-177">xsd:boolean</span></span>  <br/> |<span data-ttu-id="4770d-178">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-178">optional</span></span>  <br/> ||<span data-ttu-id="4770d-179">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="4770d-179">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="4770d-180">Таблица</span><span class="sxs-lookup"><span data-stu-id="4770d-180">Sheet</span></span>  <br/> |<span data-ttu-id="4770d-181">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-181">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-182">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-182">optional</span></span>  <br/> ||<span data-ttu-id="4770d-183">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-183">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-184">Виевцентеркс</span><span class="sxs-lookup"><span data-stu-id="4770d-184">ViewCenterX</span></span>  <br/> |<span data-ttu-id="4770d-185">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="4770d-185">xsd:double</span></span>  <br/> |<span data-ttu-id="4770d-186">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-186">optional</span></span>  <br/> ||<span data-ttu-id="4770d-187">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="4770d-187">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4770d-188">Виевцентери</span><span class="sxs-lookup"><span data-stu-id="4770d-188">ViewCenterY</span></span>  <br/> |<span data-ttu-id="4770d-189">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="4770d-189">xsd:double</span></span>  <br/> |<span data-ttu-id="4770d-190">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-190">optional</span></span>  <br/> ||<span data-ttu-id="4770d-191">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="4770d-191">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4770d-192">Виевскале</span><span class="sxs-lookup"><span data-stu-id="4770d-192">ViewScale</span></span>  <br/> |<span data-ttu-id="4770d-193">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="4770d-193">xsd:double</span></span>  <br/> |<span data-ttu-id="4770d-194">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-194">optional</span></span>  <br/> ||<span data-ttu-id="4770d-195">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="4770d-195">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="4770d-196">WindowHeight</span><span class="sxs-lookup"><span data-stu-id="4770d-196">WindowHeight</span></span>  <br/> |<span data-ttu-id="4770d-197">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-197">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-198">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-198">optional</span></span>  <br/> ||<span data-ttu-id="4770d-199">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-199">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-200">WindowLeft</span><span class="sxs-lookup"><span data-stu-id="4770d-200">WindowLeft</span></span>  <br/> |<span data-ttu-id="4770d-201">XSD: Short</span><span class="sxs-lookup"><span data-stu-id="4770d-201">xsd:short</span></span>  <br/> |<span data-ttu-id="4770d-202">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-202">optional</span></span>  <br/> ||<span data-ttu-id="4770d-203">Значения типа XSD: Short.</span><span class="sxs-lookup"><span data-stu-id="4770d-203">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="4770d-204">WindowState</span><span class="sxs-lookup"><span data-stu-id="4770d-204">WindowState</span></span>  <br/> |<span data-ttu-id="4770d-205">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-205">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-206">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-206">optional</span></span>  <br/> ||<span data-ttu-id="4770d-207">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-207">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4770d-208">WindowTop</span><span class="sxs-lookup"><span data-stu-id="4770d-208">WindowTop</span></span>  <br/> |<span data-ttu-id="4770d-209">XSD: Short</span><span class="sxs-lookup"><span data-stu-id="4770d-209">xsd:short</span></span>  <br/> |<span data-ttu-id="4770d-210">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-210">optional</span></span>  <br/> ||<span data-ttu-id="4770d-211">Значения типа XSD: Short.</span><span class="sxs-lookup"><span data-stu-id="4770d-211">Values of the xsd:short type.</span></span>  <br/> |
|<span data-ttu-id="4770d-212">Виндовтипе</span><span class="sxs-lookup"><span data-stu-id="4770d-212">WindowType</span></span>  <br/> |<span data-ttu-id="4770d-213">XSD: маркер</span><span class="sxs-lookup"><span data-stu-id="4770d-213">xsd:token</span></span>  <br/> |<span data-ttu-id="4770d-214">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-214">required</span></span>  <br/> ||<span data-ttu-id="4770d-215">Значения типа маркера XSD:.</span><span class="sxs-lookup"><span data-stu-id="4770d-215">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="4770d-216">WindowWidth</span><span class="sxs-lookup"><span data-stu-id="4770d-216">WindowWidth</span></span>  <br/> |<span data-ttu-id="4770d-217">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="4770d-217">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4770d-218">необязательный</span><span class="sxs-lookup"><span data-stu-id="4770d-218">optional</span></span>  <br/> ||<span data-ttu-id="4770d-219">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="4770d-219">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

