---
title: Датаколумн_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344704"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="e4140-102">Датаколумн_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="e4140-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e4140-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e4140-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e4140-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e4140-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e4140-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e4140-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e4140-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e4140-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e4140-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="e4140-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e4140-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="e4140-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e4140-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e4140-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e4140-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e4140-110">Elements and attributes</span></span>

<span data-ttu-id="e4140-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e4140-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e4140-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e4140-112">Child elements</span></span>

<span data-ttu-id="e4140-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="e4140-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e4140-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e4140-114">Attributes</span></span>

|<span data-ttu-id="e4140-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e4140-115">**Attribute**</span></span>|<span data-ttu-id="e4140-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e4140-116">**Type**</span></span>|<span data-ttu-id="e4140-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e4140-117">**Required**</span></span>|<span data-ttu-id="e4140-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e4140-118">**Description**</span></span>|<span data-ttu-id="e4140-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e4140-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e4140-120">Календарь</span><span class="sxs-lookup"><span data-stu-id="e4140-120">Calendar</span></span>  <br/> |<span data-ttu-id="e4140-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="e4140-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="e4140-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-122">optional</span></span>  <br/> ||<span data-ttu-id="e4140-123">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="e4140-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="e4140-124">Колумннамеид</span><span class="sxs-lookup"><span data-stu-id="e4140-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="e4140-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e4140-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e4140-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-126">required</span></span>  <br/> ||<span data-ttu-id="e4140-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e4140-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e4140-128">Денежный</span><span class="sxs-lookup"><span data-stu-id="e4140-128">Currency</span></span>  <br/> |<span data-ttu-id="e4140-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="e4140-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="e4140-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-130">optional</span></span>  <br/> ||<span data-ttu-id="e4140-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="e4140-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="e4140-132">DataType</span><span class="sxs-lookup"><span data-stu-id="e4140-132">DataType</span></span>  <br/> |<span data-ttu-id="e4140-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="e4140-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="e4140-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-134">optional</span></span>  <br/> ||<span data-ttu-id="e4140-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="e4140-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="e4140-136">Degree</span><span class="sxs-lookup"><span data-stu-id="e4140-136">Degree</span></span>  <br/> |<span data-ttu-id="e4140-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="e4140-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e4140-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-138">optional</span></span>  <br/> ||<span data-ttu-id="e4140-139">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="e4140-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e4140-140">Дисплайордер</span><span class="sxs-lookup"><span data-stu-id="e4140-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="e4140-141">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="e4140-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e4140-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-142">optional</span></span>  <br/> ||<span data-ttu-id="e4140-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="e4140-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e4140-144">Дисплайвидс</span><span class="sxs-lookup"><span data-stu-id="e4140-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="e4140-145">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="e4140-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e4140-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-146">optional</span></span>  <br/> ||<span data-ttu-id="e4140-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="e4140-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e4140-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="e4140-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="e4140-149">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="e4140-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e4140-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-150">optional</span></span>  <br/> ||<span data-ttu-id="e4140-151">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e4140-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e4140-152">Label</span><span class="sxs-lookup"><span data-stu-id="e4140-152">Label</span></span>  <br/> |<span data-ttu-id="e4140-153">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e4140-153">xsd:string</span></span>  <br/> |<span data-ttu-id="e4140-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-154">required</span></span>  <br/> ||<span data-ttu-id="e4140-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e4140-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e4140-156">LangID</span><span class="sxs-lookup"><span data-stu-id="e4140-156">LangID</span></span>  <br/> |<span data-ttu-id="e4140-157">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="e4140-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e4140-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-158">optional</span></span>  <br/> ||<span data-ttu-id="e4140-159">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="e4140-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e4140-160">Распределен</span><span class="sxs-lookup"><span data-stu-id="e4140-160">Mapped</span></span>  <br/> |<span data-ttu-id="e4140-161">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="e4140-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e4140-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-162">optional</span></span>  <br/> ||<span data-ttu-id="e4140-163">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="e4140-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e4140-164">Имя</span><span class="sxs-lookup"><span data-stu-id="e4140-164">Name</span></span>  <br/> |<span data-ttu-id="e4140-165">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e4140-165">xsd:string</span></span>  <br/> |<span data-ttu-id="e4140-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-166">required</span></span>  <br/> ||<span data-ttu-id="e4140-167">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e4140-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e4140-168">Ориглабел</span><span class="sxs-lookup"><span data-stu-id="e4140-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="e4140-169">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e4140-169">xsd:string</span></span>  <br/> |<span data-ttu-id="e4140-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-170">optional</span></span>  <br/> ||<span data-ttu-id="e4140-171">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e4140-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e4140-172">Униттипе</span><span class="sxs-lookup"><span data-stu-id="e4140-172">UnitType</span></span>  <br/> |<span data-ttu-id="e4140-173">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e4140-173">xsd:string</span></span>  <br/> |<span data-ttu-id="e4140-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="e4140-174">optional</span></span>  <br/> ||<span data-ttu-id="e4140-175">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e4140-175">Values of the xsd:string type.</span></span>  <br/> |
   

