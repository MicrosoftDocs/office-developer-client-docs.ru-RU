---
title: Хеадерфутерфонт_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335625"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a><span data-ttu-id="1e607-102">Хеадерфутерфонт_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="1e607-102">HeaderFooterFont_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1e607-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1e607-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e607-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1e607-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1e607-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1e607-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1e607-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1e607-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1e607-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1e607-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1e607-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1e607-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1e607-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1e607-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1e607-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1e607-110">Elements and attributes</span></span>

<span data-ttu-id="1e607-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1e607-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1e607-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1e607-112">Child elements</span></span>

<span data-ttu-id="1e607-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="1e607-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e607-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1e607-114">Attributes</span></span>

|<span data-ttu-id="1e607-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1e607-115">**Attribute**</span></span>|<span data-ttu-id="1e607-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1e607-116">**Type**</span></span>|<span data-ttu-id="1e607-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1e607-117">**Required**</span></span>|<span data-ttu-id="1e607-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1e607-118">**Description**</span></span>|<span data-ttu-id="1e607-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1e607-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1e607-120">CharSet</span><span class="sxs-lookup"><span data-stu-id="1e607-120">CharSet</span></span>  <br/> |<span data-ttu-id="1e607-121">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-121">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-122">optional</span></span>  <br/> ||<span data-ttu-id="1e607-123">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-123">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-124">КлиппреЦисион</span><span class="sxs-lookup"><span data-stu-id="1e607-124">ClipPrecision</span></span>  <br/> |<span data-ttu-id="1e607-125">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-125">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-126">optional</span></span>  <br/> ||<span data-ttu-id="1e607-127">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-127">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-128">ПоСледовательное преобразование</span><span class="sxs-lookup"><span data-stu-id="1e607-128">Escapement</span></span>  <br/> |<span data-ttu-id="1e607-129">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1e607-129">xsd:int</span></span>  <br/> |<span data-ttu-id="1e607-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-130">optional</span></span>  <br/> ||<span data-ttu-id="1e607-131">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1e607-131">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="1e607-132">Фаценаме</span><span class="sxs-lookup"><span data-stu-id="1e607-132">FaceName</span></span>  <br/> |<span data-ttu-id="1e607-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1e607-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1e607-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-134">optional</span></span>  <br/> ||<span data-ttu-id="1e607-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1e607-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1e607-136">Height</span><span class="sxs-lookup"><span data-stu-id="1e607-136">Height</span></span>  <br/> |<span data-ttu-id="1e607-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1e607-137">xsd:int</span></span>  <br/> |<span data-ttu-id="1e607-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-138">optional</span></span>  <br/> ||<span data-ttu-id="1e607-139">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1e607-139">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="1e607-140">Курсив</span><span class="sxs-lookup"><span data-stu-id="1e607-140">Italic</span></span>  <br/> |<span data-ttu-id="1e607-141">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-141">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-142">optional</span></span>  <br/> ||<span data-ttu-id="1e607-143">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-143">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-144">Вводное обучение</span><span class="sxs-lookup"><span data-stu-id="1e607-144">Orientation</span></span>  <br/> |<span data-ttu-id="1e607-145">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1e607-145">xsd:int</span></span>  <br/> |<span data-ttu-id="1e607-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-146">optional</span></span>  <br/> ||<span data-ttu-id="1e607-147">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1e607-147">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="1e607-148">Точность</span><span class="sxs-lookup"><span data-stu-id="1e607-148">OutPrecision</span></span>  <br/> |<span data-ttu-id="1e607-149">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-149">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-150">optional</span></span>  <br/> ||<span data-ttu-id="1e607-151">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-151">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-152">PitchAndFamily</span><span class="sxs-lookup"><span data-stu-id="1e607-152">PitchAndFamily</span></span>  <br/> |<span data-ttu-id="1e607-153">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-153">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-154">optional</span></span>  <br/> ||<span data-ttu-id="1e607-155">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-155">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-156">Отображения</span><span class="sxs-lookup"><span data-stu-id="1e607-156">Quality</span></span>  <br/> |<span data-ttu-id="1e607-157">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-157">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-158">optional</span></span>  <br/> ||<span data-ttu-id="1e607-159">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-159">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-160">Зачеркнутый</span><span class="sxs-lookup"><span data-stu-id="1e607-160">StrikeOut</span></span>  <br/> |<span data-ttu-id="1e607-161">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-161">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-162">optional</span></span>  <br/> ||<span data-ttu-id="1e607-163">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-163">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-164">Подчеркнутый</span><span class="sxs-lookup"><span data-stu-id="1e607-164">Underline</span></span>  <br/> |<span data-ttu-id="1e607-165">XSD: Унсигнедбите</span><span class="sxs-lookup"><span data-stu-id="1e607-165">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="1e607-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-166">optional</span></span>  <br/> ||<span data-ttu-id="1e607-167">Значения типа XSD: Унсигнедбите.</span><span class="sxs-lookup"><span data-stu-id="1e607-167">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="1e607-168">Насыщенность</span><span class="sxs-lookup"><span data-stu-id="1e607-168">Weight</span></span>  <br/> |<span data-ttu-id="1e607-169">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1e607-169">xsd:int</span></span>  <br/> |<span data-ttu-id="1e607-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-170">optional</span></span>  <br/> ||<span data-ttu-id="1e607-171">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1e607-171">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="1e607-172">Width</span><span class="sxs-lookup"><span data-stu-id="1e607-172">Width</span></span>  <br/> |<span data-ttu-id="1e607-173">XSD: int</span><span class="sxs-lookup"><span data-stu-id="1e607-173">xsd:int</span></span>  <br/> |<span data-ttu-id="1e607-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="1e607-174">optional</span></span>  <br/> ||<span data-ttu-id="1e607-175">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="1e607-175">Values of the xsd:int type.</span></span>  <br/> |
   

