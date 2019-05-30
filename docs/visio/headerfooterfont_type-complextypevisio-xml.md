---
title: Хеадерфутерфонт_типе complexType (XML для Visio)
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
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="8dd31-102">Хеадерфутерфонт_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8dd31-102">HeaderFooterFont_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8dd31-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8dd31-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8dd31-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8dd31-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8dd31-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8dd31-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8dd31-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8dd31-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8dd31-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="8dd31-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8dd31-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8dd31-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8dd31-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8dd31-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8dd31-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8dd31-110">Elements and attributes</span></span>

<span data-ttu-id="8dd31-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8dd31-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8dd31-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8dd31-112">Child elements</span></span>

<span data-ttu-id="8dd31-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="8dd31-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8dd31-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8dd31-114">Attributes</span></span>

|<span data-ttu-id="8dd31-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8dd31-115">**Attribute**</span></span>|<span data-ttu-id="8dd31-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8dd31-116">**Type**</span></span>|<span data-ttu-id="8dd31-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8dd31-117">**Required**</span></span>|<span data-ttu-id="8dd31-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8dd31-118">**Description**</span></span>|<span data-ttu-id="8dd31-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8dd31-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8dd31-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="8dd31-120">CharSet</span></span>  <br/> |<span data-ttu-id="8dd31-121">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-122">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-123">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-124">КлиппреЦисион</span><span class="sxs-lookup"><span data-stu-id="8dd31-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="8dd31-125">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-126">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-127">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-128">Последовательное преобразование</span><span class="sxs-lookup"><span data-stu-id="8dd31-128">Escapement</span></span>  <br/> |<span data-ttu-id="8dd31-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="8dd31-129">xsd:int</span></span>  <br/> |<span data-ttu-id="8dd31-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-130">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-131">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8dd31-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-132">Фаценаме</span><span class="sxs-lookup"><span data-stu-id="8dd31-132">FaceName</span></span>  <br/> |<span data-ttu-id="8dd31-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="8dd31-133">xsd:string</span></span>  <br/> |<span data-ttu-id="8dd31-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-134">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="8dd31-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-136">Height</span><span class="sxs-lookup"><span data-stu-id="8dd31-136">Height</span></span>  <br/> |<span data-ttu-id="8dd31-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="8dd31-137">xsd:int</span></span>  <br/> |<span data-ttu-id="8dd31-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-138">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-139">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8dd31-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-140">Курсив</span><span class="sxs-lookup"><span data-stu-id="8dd31-140">Italic</span></span>  <br/> |<span data-ttu-id="8dd31-141">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-142">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-143">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-144">Вводное обучение</span><span class="sxs-lookup"><span data-stu-id="8dd31-144">Orientation</span></span>  <br/> |<span data-ttu-id="8dd31-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="8dd31-145">xsd:int</span></span>  <br/> |<span data-ttu-id="8dd31-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-146">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-147">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8dd31-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-148">Точность</span><span class="sxs-lookup"><span data-stu-id="8dd31-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="8dd31-149">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-150">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-151">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="8dd31-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="8dd31-153">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-154">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-155">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-156">Отображения</span><span class="sxs-lookup"><span data-stu-id="8dd31-156">Quality</span></span>  <br/> |<span data-ttu-id="8dd31-157">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-158">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-159">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-160">Зачеркнутый</span><span class="sxs-lookup"><span data-stu-id="8dd31-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="8dd31-161">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-162">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-163">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-164">Подчеркнутый</span><span class="sxs-lookup"><span data-stu-id="8dd31-164">Underline</span></span>  <br/> |<span data-ttu-id="8dd31-165">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="8dd31-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="8dd31-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-166">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-167">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="8dd31-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-168">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="8dd31-168">Weight</span></span>  <br/> |<span data-ttu-id="8dd31-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="8dd31-169">xsd:int</span></span>  <br/> |<span data-ttu-id="8dd31-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-170">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8dd31-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="8dd31-172">Width</span><span class="sxs-lookup"><span data-stu-id="8dd31-172">Width</span></span>  <br/> |<span data-ttu-id="8dd31-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="8dd31-173">xsd:int</span></span>  <br/> |<span data-ttu-id="8dd31-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="8dd31-174">optional</span></span>  <br/> ||<span data-ttu-id="8dd31-175">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="8dd31-175">Values of the xsd:int type.</span></span>  <br/> |
   

