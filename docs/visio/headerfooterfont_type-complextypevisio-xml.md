---
title: HeaderFooterFont_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813885"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="20187-102">HeaderFooterFont_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="20187-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="20187-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="20187-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20187-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="20187-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="20187-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="20187-105">**Schema file**</span></span> <br/> |<span data-ttu-id="20187-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="20187-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="20187-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="20187-107">**Extension base**</span></span> <br/> |<span data-ttu-id="20187-108">Нет</span><span class="sxs-lookup"><span data-stu-id="20187-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="20187-109">Определение</span><span class="sxs-lookup"><span data-stu-id="20187-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="20187-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="20187-110">Elements and attributes</span></span>

<span data-ttu-id="20187-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="20187-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="20187-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="20187-112">Child elements</span></span>

<span data-ttu-id="20187-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="20187-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20187-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="20187-114">Attributes</span></span>

|<span data-ttu-id="20187-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="20187-115">**Attribute**</span></span>|<span data-ttu-id="20187-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="20187-116">**Type**</span></span>|<span data-ttu-id="20187-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="20187-117">**Required**</span></span>|<span data-ttu-id="20187-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="20187-118">**Description**</span></span>|<span data-ttu-id="20187-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="20187-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="20187-120">Набор символов</span><span class="sxs-lookup"><span data-stu-id="20187-120">CharSet</span></span>  <br/> |<span data-ttu-id="20187-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-122">optional</span></span>  <br/> ||<span data-ttu-id="20187-123">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="20187-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="20187-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-126">optional</span></span>  <br/> ||<span data-ttu-id="20187-127">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-128">Наклон</span><span class="sxs-lookup"><span data-stu-id="20187-128">Escapement</span></span>  <br/> |<span data-ttu-id="20187-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="20187-129">xsd:int</span></span>  <br/> |<span data-ttu-id="20187-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-130">optional</span></span>  <br/> ||<span data-ttu-id="20187-131">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="20187-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="20187-132">Название значка</span><span class="sxs-lookup"><span data-stu-id="20187-132">FaceName</span></span>  <br/> |<span data-ttu-id="20187-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="20187-133">xsd:string</span></span>  <br/> |<span data-ttu-id="20187-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-134">optional</span></span>  <br/> ||<span data-ttu-id="20187-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="20187-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="20187-136">Height</span><span class="sxs-lookup"><span data-stu-id="20187-136">Height</span></span>  <br/> |<span data-ttu-id="20187-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="20187-137">xsd:int</span></span>  <br/> |<span data-ttu-id="20187-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-138">optional</span></span>  <br/> ||<span data-ttu-id="20187-139">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="20187-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="20187-140">Курсив</span><span class="sxs-lookup"><span data-stu-id="20187-140">Italic</span></span>  <br/> |<span data-ttu-id="20187-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-142">optional</span></span>  <br/> ||<span data-ttu-id="20187-143">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-144">Ориентация</span><span class="sxs-lookup"><span data-stu-id="20187-144">Orientation</span></span>  <br/> |<span data-ttu-id="20187-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="20187-145">xsd:int</span></span>  <br/> |<span data-ttu-id="20187-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-146">optional</span></span>  <br/> ||<span data-ttu-id="20187-147">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="20187-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="20187-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="20187-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="20187-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-150">optional</span></span>  <br/> ||<span data-ttu-id="20187-151">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="20187-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="20187-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-154">optional</span></span>  <br/> ||<span data-ttu-id="20187-155">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-156">Качество</span><span class="sxs-lookup"><span data-stu-id="20187-156">Quality</span></span>  <br/> |<span data-ttu-id="20187-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-158">optional</span></span>  <br/> ||<span data-ttu-id="20187-159">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-160">Зачеркивание</span><span class="sxs-lookup"><span data-stu-id="20187-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="20187-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-162">optional</span></span>  <br/> ||<span data-ttu-id="20187-163">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-164">Подчеркивание</span><span class="sxs-lookup"><span data-stu-id="20187-164">Underline</span></span>  <br/> |<span data-ttu-id="20187-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="20187-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="20187-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-166">optional</span></span>  <br/> ||<span data-ttu-id="20187-167">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="20187-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="20187-168">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="20187-168">Weight</span></span>  <br/> |<span data-ttu-id="20187-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="20187-169">xsd:int</span></span>  <br/> |<span data-ttu-id="20187-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-170">optional</span></span>  <br/> ||<span data-ttu-id="20187-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="20187-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="20187-172">Width</span><span class="sxs-lookup"><span data-stu-id="20187-172">Width</span></span>  <br/> |<span data-ttu-id="20187-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="20187-173">xsd:int</span></span>  <br/> |<span data-ttu-id="20187-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="20187-174">optional</span></span>  <br/> ||<span data-ttu-id="20187-175">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="20187-175">Values of the xsd:int type.</span></span>  <br/> |
   

