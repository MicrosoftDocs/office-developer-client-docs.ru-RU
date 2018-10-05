---
title: HeaderFooterFont_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397249"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="516e3-102">HeaderFooterFont_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="516e3-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="516e3-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="516e3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="516e3-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="516e3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="516e3-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="516e3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="516e3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="516e3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="516e3-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="516e3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="516e3-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="516e3-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="516e3-109">Определение</span><span class="sxs-lookup"><span data-stu-id="516e3-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="516e3-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="516e3-110">Elements and attributes</span></span>

<span data-ttu-id="516e3-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="516e3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="516e3-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="516e3-112">Child elements</span></span>

<span data-ttu-id="516e3-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="516e3-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="516e3-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="516e3-114">Attributes</span></span>

|<span data-ttu-id="516e3-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="516e3-115">**Attribute**</span></span>|<span data-ttu-id="516e3-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="516e3-116">**Type**</span></span>|<span data-ttu-id="516e3-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="516e3-117">**Required**</span></span>|<span data-ttu-id="516e3-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="516e3-118">**Description**</span></span>|<span data-ttu-id="516e3-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="516e3-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="516e3-120">Набор символов</span><span class="sxs-lookup"><span data-stu-id="516e3-120">CharSet</span></span>  <br/> |<span data-ttu-id="516e3-121">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-122">optional</span></span>  <br/> ||<span data-ttu-id="516e3-123">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-124">ClipPrecision</span><span class="sxs-lookup"><span data-stu-id="516e3-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="516e3-125">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-126">optional</span></span>  <br/> ||<span data-ttu-id="516e3-127">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-128">Наклон</span><span class="sxs-lookup"><span data-stu-id="516e3-128">Escapement</span></span>  <br/> |<span data-ttu-id="516e3-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="516e3-129">xsd:int</span></span>  <br/> |<span data-ttu-id="516e3-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-130">optional</span></span>  <br/> ||<span data-ttu-id="516e3-131">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="516e3-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="516e3-132">Название значка</span><span class="sxs-lookup"><span data-stu-id="516e3-132">FaceName</span></span>  <br/> |<span data-ttu-id="516e3-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="516e3-133">xsd:string</span></span>  <br/> |<span data-ttu-id="516e3-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-134">optional</span></span>  <br/> ||<span data-ttu-id="516e3-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="516e3-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="516e3-136">Height</span><span class="sxs-lookup"><span data-stu-id="516e3-136">Height</span></span>  <br/> |<span data-ttu-id="516e3-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="516e3-137">xsd:int</span></span>  <br/> |<span data-ttu-id="516e3-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-138">optional</span></span>  <br/> ||<span data-ttu-id="516e3-139">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="516e3-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="516e3-140">Курсив</span><span class="sxs-lookup"><span data-stu-id="516e3-140">Italic</span></span>  <br/> |<span data-ttu-id="516e3-141">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-142">optional</span></span>  <br/> ||<span data-ttu-id="516e3-143">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-144">Ориентация</span><span class="sxs-lookup"><span data-stu-id="516e3-144">Orientation</span></span>  <br/> |<span data-ttu-id="516e3-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="516e3-145">xsd:int</span></span>  <br/> |<span data-ttu-id="516e3-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-146">optional</span></span>  <br/> ||<span data-ttu-id="516e3-147">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="516e3-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="516e3-148">OutPrecision</span><span class="sxs-lookup"><span data-stu-id="516e3-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="516e3-149">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-150">optional</span></span>  <br/> ||<span data-ttu-id="516e3-151">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="516e3-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="516e3-153">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-154">optional</span></span>  <br/> ||<span data-ttu-id="516e3-155">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-156">Качество</span><span class="sxs-lookup"><span data-stu-id="516e3-156">Quality</span></span>  <br/> |<span data-ttu-id="516e3-157">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-158">optional</span></span>  <br/> ||<span data-ttu-id="516e3-159">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-160">Зачеркивание</span><span class="sxs-lookup"><span data-stu-id="516e3-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="516e3-161">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-162">optional</span></span>  <br/> ||<span data-ttu-id="516e3-163">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-164">Подчеркивание</span><span class="sxs-lookup"><span data-stu-id="516e3-164">Underline</span></span>  <br/> |<span data-ttu-id="516e3-165">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="516e3-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="516e3-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-166">optional</span></span>  <br/> ||<span data-ttu-id="516e3-167">Значения типа xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="516e3-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="516e3-168">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="516e3-168">Weight</span></span>  <br/> |<span data-ttu-id="516e3-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="516e3-169">xsd:int</span></span>  <br/> |<span data-ttu-id="516e3-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-170">optional</span></span>  <br/> ||<span data-ttu-id="516e3-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="516e3-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="516e3-172">Width</span><span class="sxs-lookup"><span data-stu-id="516e3-172">Width</span></span>  <br/> |<span data-ttu-id="516e3-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="516e3-173">xsd:int</span></span>  <br/> |<span data-ttu-id="516e3-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="516e3-174">optional</span></span>  <br/> ||<span data-ttu-id="516e3-175">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="516e3-175">Values of the xsd:int type.</span></span>  <br/> |
   

