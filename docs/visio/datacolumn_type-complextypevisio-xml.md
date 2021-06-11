---
title: DataColumn_Type ComplexType (Visio XML)
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
# <a name="datacolumn_type-complextype-visio-xml"></a><span data-ttu-id="9a035-102">DataColumn_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="9a035-102">DataColumn_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9a035-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9a035-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a035-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9a035-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a035-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9a035-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a035-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a035-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a035-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="9a035-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a035-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="9a035-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a035-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9a035-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9a035-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a035-110">Elements and attributes</span></span>

<span data-ttu-id="9a035-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9a035-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a035-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9a035-112">Child elements</span></span>

<span data-ttu-id="9a035-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="9a035-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9a035-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9a035-114">Attributes</span></span>

|<span data-ttu-id="9a035-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9a035-115">**Attribute**</span></span>|<span data-ttu-id="9a035-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9a035-116">**Type**</span></span>|<span data-ttu-id="9a035-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9a035-117">**Required**</span></span>|<span data-ttu-id="9a035-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9a035-118">**Description**</span></span>|<span data-ttu-id="9a035-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9a035-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a035-120">Календарь</span><span class="sxs-lookup"><span data-stu-id="9a035-120">Calendar</span></span>  <br/> |<span data-ttu-id="9a035-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9a035-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9a035-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-122">optional</span></span>  <br/> ||<span data-ttu-id="9a035-123">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9a035-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9a035-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="9a035-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="9a035-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a035-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9a035-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-126">required</span></span>  <br/> ||<span data-ttu-id="9a035-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a035-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a035-128">Денежный</span><span class="sxs-lookup"><span data-stu-id="9a035-128">Currency</span></span>  <br/> |<span data-ttu-id="9a035-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9a035-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9a035-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-130">optional</span></span>  <br/> ||<span data-ttu-id="9a035-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9a035-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9a035-132">DataType</span><span class="sxs-lookup"><span data-stu-id="9a035-132">DataType</span></span>  <br/> |<span data-ttu-id="9a035-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="9a035-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="9a035-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-134">optional</span></span>  <br/> ||<span data-ttu-id="9a035-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="9a035-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="9a035-136">Degree</span><span class="sxs-lookup"><span data-stu-id="9a035-136">Degree</span></span>  <br/> |<span data-ttu-id="9a035-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a035-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a035-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-138">optional</span></span>  <br/> ||<span data-ttu-id="9a035-139">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a035-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a035-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="9a035-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="9a035-141">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a035-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a035-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-142">optional</span></span>  <br/> ||<span data-ttu-id="9a035-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a035-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a035-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="9a035-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="9a035-145">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a035-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a035-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-146">optional</span></span>  <br/> ||<span data-ttu-id="9a035-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a035-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a035-148">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="9a035-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="9a035-149">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a035-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a035-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-150">optional</span></span>  <br/> ||<span data-ttu-id="9a035-151">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a035-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a035-152">Выбор метки</span><span class="sxs-lookup"><span data-stu-id="9a035-152">Label</span></span>  <br/> |<span data-ttu-id="9a035-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a035-153">xsd:string</span></span>  <br/> |<span data-ttu-id="9a035-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-154">required</span></span>  <br/> ||<span data-ttu-id="9a035-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a035-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a035-156">LangID</span><span class="sxs-lookup"><span data-stu-id="9a035-156">LangID</span></span>  <br/> |<span data-ttu-id="9a035-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a035-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a035-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-158">optional</span></span>  <br/> ||<span data-ttu-id="9a035-159">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a035-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a035-160">Mapped</span><span class="sxs-lookup"><span data-stu-id="9a035-160">Mapped</span></span>  <br/> |<span data-ttu-id="9a035-161">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="9a035-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9a035-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-162">optional</span></span>  <br/> ||<span data-ttu-id="9a035-163">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="9a035-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9a035-164">Имя</span><span class="sxs-lookup"><span data-stu-id="9a035-164">Name</span></span>  <br/> |<span data-ttu-id="9a035-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a035-165">xsd:string</span></span>  <br/> |<span data-ttu-id="9a035-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-166">required</span></span>  <br/> ||<span data-ttu-id="9a035-167">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a035-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a035-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="9a035-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="9a035-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a035-169">xsd:string</span></span>  <br/> |<span data-ttu-id="9a035-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-170">optional</span></span>  <br/> ||<span data-ttu-id="9a035-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a035-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a035-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="9a035-172">UnitType</span></span>  <br/> |<span data-ttu-id="9a035-173">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a035-173">xsd:string</span></span>  <br/> |<span data-ttu-id="9a035-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="9a035-174">optional</span></span>  <br/> ||<span data-ttu-id="9a035-175">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a035-175">Values of the xsd:string type.</span></span>  <br/> |
   

