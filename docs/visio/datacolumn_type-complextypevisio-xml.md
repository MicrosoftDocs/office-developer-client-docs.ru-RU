---
title: DataColumn_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 9d334190b686f3b2c5e25a31336c668c957e820f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813533"
---
# <a name="datacolumntype-complextype-visio-xml"></a><span data-ttu-id="f23b6-102">DataColumn_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f23b6-102">DataColumn_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f23b6-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f23b6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f23b6-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f23b6-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f23b6-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f23b6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f23b6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f23b6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f23b6-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="f23b6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f23b6-108">Нет</span><span class="sxs-lookup"><span data-stu-id="f23b6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f23b6-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f23b6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f23b6-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f23b6-110">Elements and attributes</span></span>

<span data-ttu-id="f23b6-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="f23b6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f23b6-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f23b6-112">Child elements</span></span>

<span data-ttu-id="f23b6-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="f23b6-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f23b6-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f23b6-114">Attributes</span></span>

|<span data-ttu-id="f23b6-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f23b6-115">**Attribute**</span></span>|<span data-ttu-id="f23b6-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f23b6-116">**Type**</span></span>|<span data-ttu-id="f23b6-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="f23b6-117">**Required**</span></span>|<span data-ttu-id="f23b6-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f23b6-118">**Description**</span></span>|<span data-ttu-id="f23b6-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f23b6-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f23b6-120">Календарь</span><span class="sxs-lookup"><span data-stu-id="f23b6-120">Calendar</span></span>  <br/> |<span data-ttu-id="f23b6-121">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f23b6-121">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f23b6-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-122">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-123">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f23b6-123">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="f23b6-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="f23b6-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f23b6-125">xsd:string</span></span>  <br/> |<span data-ttu-id="f23b6-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-126">required</span></span>  <br/> ||<span data-ttu-id="f23b6-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f23b6-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-128">Денежный</span><span class="sxs-lookup"><span data-stu-id="f23b6-128">Currency</span></span>  <br/> |<span data-ttu-id="f23b6-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f23b6-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f23b6-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-130">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-131">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f23b6-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-132">DataType</span><span class="sxs-lookup"><span data-stu-id="f23b6-132">DataType</span></span>  <br/> |<span data-ttu-id="f23b6-133">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f23b6-133">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f23b6-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-134">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-135">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f23b6-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-136">Степень</span><span class="sxs-lookup"><span data-stu-id="f23b6-136">Degree</span></span>  <br/> |<span data-ttu-id="f23b6-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f23b6-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f23b6-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-138">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-139">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f23b6-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-140">DisplayOrder</span><span class="sxs-lookup"><span data-stu-id="f23b6-140">DisplayOrder</span></span>  <br/> |<span data-ttu-id="f23b6-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f23b6-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f23b6-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-142">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f23b6-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-144">DisplayWidth</span><span class="sxs-lookup"><span data-stu-id="f23b6-144">DisplayWidth</span></span>  <br/> |<span data-ttu-id="f23b6-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f23b6-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f23b6-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-146">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f23b6-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-148">Гиперссылка</span><span class="sxs-lookup"><span data-stu-id="f23b6-148">Hyperlink</span></span>  <br/> |<span data-ttu-id="f23b6-149">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f23b6-149">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f23b6-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-150">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-151">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f23b6-151">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-152">Метка</span><span class="sxs-lookup"><span data-stu-id="f23b6-152">Label</span></span>  <br/> |<span data-ttu-id="f23b6-153">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f23b6-153">xsd:string</span></span>  <br/> |<span data-ttu-id="f23b6-154">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-154">required</span></span>  <br/> ||<span data-ttu-id="f23b6-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f23b6-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-156">LangID</span><span class="sxs-lookup"><span data-stu-id="f23b6-156">LangID</span></span>  <br/> |<span data-ttu-id="f23b6-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f23b6-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f23b6-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-158">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-159">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f23b6-159">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-160">Сопоставленные</span><span class="sxs-lookup"><span data-stu-id="f23b6-160">Mapped</span></span>  <br/> |<span data-ttu-id="f23b6-161">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f23b6-161">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f23b6-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-162">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-163">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f23b6-163">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-164">Имя</span><span class="sxs-lookup"><span data-stu-id="f23b6-164">Name</span></span>  <br/> |<span data-ttu-id="f23b6-165">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f23b6-165">xsd:string</span></span>  <br/> |<span data-ttu-id="f23b6-166">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-166">required</span></span>  <br/> ||<span data-ttu-id="f23b6-167">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f23b6-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-168">OrigLabel</span><span class="sxs-lookup"><span data-stu-id="f23b6-168">OrigLabel</span></span>  <br/> |<span data-ttu-id="f23b6-169">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f23b6-169">xsd:string</span></span>  <br/> |<span data-ttu-id="f23b6-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-170">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f23b6-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f23b6-172">UnitType</span><span class="sxs-lookup"><span data-stu-id="f23b6-172">UnitType</span></span>  <br/> |<span data-ttu-id="f23b6-173">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f23b6-173">xsd:string</span></span>  <br/> |<span data-ttu-id="f23b6-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="f23b6-174">optional</span></span>  <br/> ||<span data-ttu-id="f23b6-175">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f23b6-175">Values of the xsd:string type.</span></span>  <br/> |
   

