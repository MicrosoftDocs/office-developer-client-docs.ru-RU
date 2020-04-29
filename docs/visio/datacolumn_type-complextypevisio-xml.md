---
title: DataColumn_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541213"
---
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="ca137-102">DataColumn_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="ca137-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="ca137-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ca137-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca137-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ca137-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ca137-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ca137-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ca137-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ca137-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ca137-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ca137-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ca137-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ca137-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca137-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ca137-109">Definition</span></span>

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ca137-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca137-110">Elements and attributes</span></span>

<span data-ttu-id="ca137-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ca137-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ca137-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ca137-112">Child elements</span></span>

<span data-ttu-id="ca137-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="ca137-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca137-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca137-114">Attributes</span></span>

|<span data-ttu-id="ca137-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ca137-115">**Attribute**</span></span>|<span data-ttu-id="ca137-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca137-116">**Type**</span></span>|<span data-ttu-id="ca137-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ca137-117">**Required**</span></span>|<span data-ttu-id="ca137-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca137-118">**Description**</span></span>|<span data-ttu-id="ca137-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ca137-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ca137-120">Календарь</span><span class="sxs-lookup"><span data-stu-id="ca137-120">Calendar</span></span>  <br/> |<span data-ttu-id="ca137-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ca137-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ca137-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-122">optional</span></span>  <br/> ||<span data-ttu-id="ca137-123">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ca137-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ca137-124">колумннамеид</span><span class="sxs-lookup"><span data-stu-id="ca137-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="ca137-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ca137-125">xsd:string</span></span>  <br/> |<span data-ttu-id="ca137-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-126">required</span></span>  <br/> ||<span data-ttu-id="ca137-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ca137-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ca137-128">Денежный</span><span class="sxs-lookup"><span data-stu-id="ca137-128">Currency</span></span>  <br/> |<span data-ttu-id="ca137-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ca137-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ca137-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-130">optional</span></span>  <br/> ||<span data-ttu-id="ca137-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ca137-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ca137-132">DataType</span><span class="sxs-lookup"><span data-stu-id="ca137-132">DataType</span></span>  <br/> |<span data-ttu-id="ca137-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ca137-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ca137-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-134">optional</span></span>  <br/> ||<span data-ttu-id="ca137-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ca137-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ca137-136">Degree</span><span class="sxs-lookup"><span data-stu-id="ca137-136">Degree</span></span>  <br/> |<span data-ttu-id="ca137-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ca137-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca137-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-138">optional</span></span>  <br/> ||<span data-ttu-id="ca137-139">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ca137-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca137-140">дисплайордер</span><span class="sxs-lookup"><span data-stu-id="ca137-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="ca137-141">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ca137-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca137-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-142">optional</span></span>  <br/> ||<span data-ttu-id="ca137-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ca137-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca137-144">дисплайвидс</span><span class="sxs-lookup"><span data-stu-id="ca137-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="ca137-145">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ca137-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca137-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-146">optional</span></span>  <br/> ||<span data-ttu-id="ca137-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ca137-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca137-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="ca137-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="ca137-149">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ca137-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ca137-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-150">optional</span></span>  <br/> ||<span data-ttu-id="ca137-151">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ca137-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ca137-152">Label</span><span class="sxs-lookup"><span data-stu-id="ca137-152">Label</span></span>  <br/> |<span data-ttu-id="ca137-153">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ca137-153">xsd:string</span></span>  <br/> |<span data-ttu-id="ca137-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-154">required</span></span>  <br/> ||<span data-ttu-id="ca137-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ca137-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ca137-156">LangID</span><span class="sxs-lookup"><span data-stu-id="ca137-156">LangID</span></span>  <br/> |<span data-ttu-id="ca137-157">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ca137-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca137-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-158">optional</span></span>  <br/> ||<span data-ttu-id="ca137-159">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ca137-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca137-160">Распределен</span><span class="sxs-lookup"><span data-stu-id="ca137-160">Mapped</span></span>  <br/> |<span data-ttu-id="ca137-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ca137-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ca137-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-162">optional</span></span>  <br/> ||<span data-ttu-id="ca137-163">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ca137-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ca137-164">Имя</span><span class="sxs-lookup"><span data-stu-id="ca137-164">Name</span></span>  <br/> |<span data-ttu-id="ca137-165">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ca137-165">xsd:string</span></span>  <br/> |<span data-ttu-id="ca137-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-166">required</span></span>  <br/> ||<span data-ttu-id="ca137-167">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ca137-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ca137-168">ориглабел</span><span class="sxs-lookup"><span data-stu-id="ca137-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="ca137-169">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ca137-169">xsd:string</span></span>  <br/> |<span data-ttu-id="ca137-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-170">optional</span></span>  <br/> ||<span data-ttu-id="ca137-171">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ca137-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ca137-172">униттипе</span><span class="sxs-lookup"><span data-stu-id="ca137-172">UnitType</span></span>  <br/> |<span data-ttu-id="ca137-173">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ca137-173">xsd:string</span></span>  <br/> |<span data-ttu-id="ca137-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca137-174">optional</span></span>  <br/> ||<span data-ttu-id="ca137-175">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ca137-175">Values of the xsd:string type.</span></span>  <br/> |
   

