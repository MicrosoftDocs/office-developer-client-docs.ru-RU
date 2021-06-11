---
title: HeaderFooterFont_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541073"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a><span data-ttu-id="076c8-102">HeaderFooterFont_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="076c8-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="076c8-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="076c8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="076c8-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="076c8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="076c8-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="076c8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="076c8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="076c8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="076c8-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="076c8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="076c8-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="076c8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="076c8-109">Определение</span><span class="sxs-lookup"><span data-stu-id="076c8-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="076c8-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="076c8-110">Elements and attributes</span></span>

<span data-ttu-id="076c8-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="076c8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="076c8-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="076c8-112">Child elements</span></span>

<span data-ttu-id="076c8-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="076c8-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="076c8-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="076c8-114">Attributes</span></span>

|<span data-ttu-id="076c8-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="076c8-115">**Attribute**</span></span>|<span data-ttu-id="076c8-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="076c8-116">**Type**</span></span>|<span data-ttu-id="076c8-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="076c8-117">**Required**</span></span>|<span data-ttu-id="076c8-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="076c8-118">**Description**</span></span>|<span data-ttu-id="076c8-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="076c8-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="076c8-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="076c8-120">CharSet</span></span>  <br/> |<span data-ttu-id="076c8-121">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-122">optional</span></span>  <br/> ||<span data-ttu-id="076c8-123">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="076c8-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="076c8-125">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-126">optional</span></span>  <br/> ||<span data-ttu-id="076c8-127">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-128">Escapement</span><span class="sxs-lookup"><span data-stu-id="076c8-128">Escapement</span></span>  <br/> |<span data-ttu-id="076c8-129">xsd:int</span><span class="sxs-lookup"><span data-stu-id="076c8-129">xsd:int</span></span>  <br/> |<span data-ttu-id="076c8-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-130">optional</span></span>  <br/> ||<span data-ttu-id="076c8-131">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="076c8-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="076c8-132">FaceName</span><span class="sxs-lookup"><span data-stu-id="076c8-132">FaceName</span></span>  <br/> |<span data-ttu-id="076c8-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="076c8-133">xsd:string</span></span>  <br/> |<span data-ttu-id="076c8-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-134">optional</span></span>  <br/> ||<span data-ttu-id="076c8-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="076c8-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="076c8-136">Height</span><span class="sxs-lookup"><span data-stu-id="076c8-136">Height</span></span>  <br/> |<span data-ttu-id="076c8-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="076c8-137">xsd:int</span></span>  <br/> |<span data-ttu-id="076c8-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-138">optional</span></span>  <br/> ||<span data-ttu-id="076c8-139">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="076c8-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="076c8-140">Курсив</span><span class="sxs-lookup"><span data-stu-id="076c8-140">Italic</span></span>  <br/> |<span data-ttu-id="076c8-141">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-142">optional</span></span>  <br/> ||<span data-ttu-id="076c8-143">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-144">Вводное обучение</span><span class="sxs-lookup"><span data-stu-id="076c8-144">Orientation</span></span>  <br/> |<span data-ttu-id="076c8-145">xsd:int</span><span class="sxs-lookup"><span data-stu-id="076c8-145">xsd:int</span></span>  <br/> |<span data-ttu-id="076c8-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-146">optional</span></span>  <br/> ||<span data-ttu-id="076c8-147">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="076c8-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="076c8-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="076c8-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="076c8-149">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-150">optional</span></span>  <br/> ||<span data-ttu-id="076c8-151">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="076c8-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="076c8-153">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-154">optional</span></span>  <br/> ||<span data-ttu-id="076c8-155">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-156">Качество</span><span class="sxs-lookup"><span data-stu-id="076c8-156">Quality</span></span>  <br/> |<span data-ttu-id="076c8-157">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-158">optional</span></span>  <br/> ||<span data-ttu-id="076c8-159">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-160">StrikeOut</span><span class="sxs-lookup"><span data-stu-id="076c8-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="076c8-161">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-162">optional</span></span>  <br/> ||<span data-ttu-id="076c8-163">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-164">Подчеркнутый</span><span class="sxs-lookup"><span data-stu-id="076c8-164">Underline</span></span>  <br/> |<span data-ttu-id="076c8-165">xsd:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="076c8-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="076c8-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-166">optional</span></span>  <br/> ||<span data-ttu-id="076c8-167">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="076c8-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="076c8-168">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="076c8-168">Weight</span></span>  <br/> |<span data-ttu-id="076c8-169">xsd:int</span><span class="sxs-lookup"><span data-stu-id="076c8-169">xsd:int</span></span>  <br/> |<span data-ttu-id="076c8-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-170">optional</span></span>  <br/> ||<span data-ttu-id="076c8-171">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="076c8-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="076c8-172">Width</span><span class="sxs-lookup"><span data-stu-id="076c8-172">Width</span></span>  <br/> |<span data-ttu-id="076c8-173">xsd:int</span><span class="sxs-lookup"><span data-stu-id="076c8-173">xsd:int</span></span>  <br/> |<span data-ttu-id="076c8-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="076c8-174">optional</span></span>  <br/> ||<span data-ttu-id="076c8-175">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="076c8-175">Values of the xsd:int type.</span></span>  <br/> |
   

