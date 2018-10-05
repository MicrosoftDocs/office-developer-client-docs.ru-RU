---
title: DataColumn_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 69f994b9516b04ddca8d26a645161772dc77c470
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388660"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="cc275-102">DataColumn_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="cc275-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cc275-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="cc275-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc275-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="cc275-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cc275-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="cc275-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cc275-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cc275-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cc275-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="cc275-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cc275-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="cc275-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc275-109">Определение</span><span class="sxs-lookup"><span data-stu-id="cc275-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="cc275-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="cc275-110">Elements and attributes</span></span>

<span data-ttu-id="cc275-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="cc275-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cc275-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cc275-112">Child elements</span></span>

<span data-ttu-id="cc275-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="cc275-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cc275-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cc275-114">Attributes</span></span>

|<span data-ttu-id="cc275-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="cc275-115">**Attribute**</span></span>|<span data-ttu-id="cc275-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cc275-116">**Type**</span></span>|<span data-ttu-id="cc275-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="cc275-117">**Required**</span></span>|<span data-ttu-id="cc275-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cc275-118">**Description**</span></span>|<span data-ttu-id="cc275-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="cc275-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc275-120">Календарь</span><span class="sxs-lookup"><span data-stu-id="cc275-120">Calendar</span></span>  <br/> |<span data-ttu-id="cc275-121">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cc275-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cc275-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-122">optional</span></span>  <br/> ||<span data-ttu-id="cc275-123">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cc275-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cc275-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="cc275-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="cc275-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="cc275-125">xsd:string</span></span>  <br/> |<span data-ttu-id="cc275-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-126">required</span></span>  <br/> ||<span data-ttu-id="cc275-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cc275-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cc275-128">Денежный</span><span class="sxs-lookup"><span data-stu-id="cc275-128">Currency</span></span>  <br/> |<span data-ttu-id="cc275-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cc275-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cc275-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-130">optional</span></span>  <br/> ||<span data-ttu-id="cc275-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cc275-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cc275-132">DataType</span><span class="sxs-lookup"><span data-stu-id="cc275-132">DataType</span></span>  <br/> |<span data-ttu-id="cc275-133">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="cc275-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="cc275-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-134">optional</span></span>  <br/> ||<span data-ttu-id="cc275-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="cc275-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="cc275-136">Степень</span><span class="sxs-lookup"><span data-stu-id="cc275-136">Degree</span></span>  <br/> |<span data-ttu-id="cc275-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc275-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc275-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-138">optional</span></span>  <br/> ||<span data-ttu-id="cc275-139">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc275-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc275-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="cc275-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="cc275-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc275-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc275-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-142">optional</span></span>  <br/> ||<span data-ttu-id="cc275-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc275-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc275-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="cc275-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="cc275-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc275-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc275-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-146">optional</span></span>  <br/> ||<span data-ttu-id="cc275-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc275-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc275-148">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="cc275-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="cc275-149">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="cc275-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cc275-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-150">optional</span></span>  <br/> ||<span data-ttu-id="cc275-151">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="cc275-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cc275-152">Метка</span><span class="sxs-lookup"><span data-stu-id="cc275-152">Label</span></span>  <br/> |<span data-ttu-id="cc275-153">XSD:String</span><span class="sxs-lookup"><span data-stu-id="cc275-153">xsd:string</span></span>  <br/> |<span data-ttu-id="cc275-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-154">required</span></span>  <br/> ||<span data-ttu-id="cc275-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cc275-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cc275-156">LangID</span><span class="sxs-lookup"><span data-stu-id="cc275-156">LangID</span></span>  <br/> |<span data-ttu-id="cc275-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc275-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc275-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-158">optional</span></span>  <br/> ||<span data-ttu-id="cc275-159">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc275-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc275-160">Сопоставленные</span><span class="sxs-lookup"><span data-stu-id="cc275-160">Mapped</span></span>  <br/> |<span data-ttu-id="cc275-161">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="cc275-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cc275-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-162">optional</span></span>  <br/> ||<span data-ttu-id="cc275-163">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="cc275-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="cc275-164">Имя</span><span class="sxs-lookup"><span data-stu-id="cc275-164">Name</span></span>  <br/> |<span data-ttu-id="cc275-165">XSD:String</span><span class="sxs-lookup"><span data-stu-id="cc275-165">xsd:string</span></span>  <br/> |<span data-ttu-id="cc275-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-166">required</span></span>  <br/> ||<span data-ttu-id="cc275-167">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cc275-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cc275-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="cc275-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="cc275-169">XSD:String</span><span class="sxs-lookup"><span data-stu-id="cc275-169">xsd:string</span></span>  <br/> |<span data-ttu-id="cc275-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-170">optional</span></span>  <br/> ||<span data-ttu-id="cc275-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cc275-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cc275-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="cc275-172">UnitType</span></span>  <br/> |<span data-ttu-id="cc275-173">XSD:String</span><span class="sxs-lookup"><span data-stu-id="cc275-173">xsd:string</span></span>  <br/> |<span data-ttu-id="cc275-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="cc275-174">optional</span></span>  <br/> ||<span data-ttu-id="cc275-175">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cc275-175">Values of the xsd:string type.</span></span>  <br/> |
   

