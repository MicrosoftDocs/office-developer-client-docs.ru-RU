---
title: Мастер_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 22b619149fc5393f085ca6e245c65ed6058538ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538069"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="0d4f1-102">Мастер_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="0d4f1-102">Master_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0d4f1-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0d4f1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d4f1-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0d4f1-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0d4f1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0d4f1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0d4f1-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0d4f1-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="0d4f1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0d4f1-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0d4f1-109">Definition</span></span>

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0d4f1-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0d4f1-110">Elements and attributes</span></span>

<span data-ttu-id="0d4f1-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0d4f1-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0d4f1-112">Child elements</span></span>

|<span data-ttu-id="0d4f1-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-113">**Element**</span></span>|<span data-ttu-id="0d4f1-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-114">**Type**</span></span>|<span data-ttu-id="0d4f1-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0d4f1-116">Icon</span><span class="sxs-lookup"><span data-stu-id="0d4f1-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d4f1-117">Икон_типе</span><span class="sxs-lookup"><span data-stu-id="0d4f1-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0d4f1-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="0d4f1-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d4f1-119">Пажешит_типе</span><span class="sxs-lookup"><span data-stu-id="0d4f1-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="0d4f1-120">Rel</span><span class="sxs-lookup"><span data-stu-id="0d4f1-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0d4f1-121">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="0d4f1-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0d4f1-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0d4f1-122">Attributes</span></span>

|<span data-ttu-id="0d4f1-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-123">**Attribute**</span></span>|<span data-ttu-id="0d4f1-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-124">**Type**</span></span>|<span data-ttu-id="0d4f1-125">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-125">**Required**</span></span>|<span data-ttu-id="0d4f1-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-126">**Description**</span></span>|<span data-ttu-id="0d4f1-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0d4f1-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0d4f1-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="0d4f1-128">AlignName</span></span>  <br/> |<span data-ttu-id="0d4f1-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0d4f1-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0d4f1-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-130">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="0d4f1-132">BaseID</span></span>  <br/> |<span data-ttu-id="0d4f1-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0d4f1-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0d4f1-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-134">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="0d4f1-136">Hidden</span></span>  <br/> |<span data-ttu-id="0d4f1-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0d4f1-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0d4f1-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-138">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-139">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="0d4f1-140">IconSize</span></span>  <br/> |<span data-ttu-id="0d4f1-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0d4f1-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0d4f1-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-142">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-143">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="0d4f1-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="0d4f1-145">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0d4f1-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0d4f1-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-146">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-147">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-148">ID</span><span class="sxs-lookup"><span data-stu-id="0d4f1-148">ID</span></span>  <br/> |<span data-ttu-id="0d4f1-149">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0d4f1-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0d4f1-150">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-150">required</span></span>  <br/> ||<span data-ttu-id="0d4f1-151">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-152">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="0d4f1-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="0d4f1-153">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0d4f1-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0d4f1-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-154">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-155">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-156">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="0d4f1-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0d4f1-157">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0d4f1-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0d4f1-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-158">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-159">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="0d4f1-160">MasterType</span></span>  <br/> |<span data-ttu-id="0d4f1-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0d4f1-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0d4f1-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-162">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-163">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="0d4f1-164">MatchByName</span></span>  <br/> |<span data-ttu-id="0d4f1-165">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="0d4f1-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0d4f1-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-166">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-167">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-168">Имя</span><span class="sxs-lookup"><span data-stu-id="0d4f1-168">Name</span></span>  <br/> |<span data-ttu-id="0d4f1-169">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0d4f1-169">xsd:string</span></span>  <br/> |<span data-ttu-id="0d4f1-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-170">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-171">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-172">NameU</span><span class="sxs-lookup"><span data-stu-id="0d4f1-172">NameU</span></span>  <br/> |<span data-ttu-id="0d4f1-173">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0d4f1-173">xsd:string</span></span>  <br/> |<span data-ttu-id="0d4f1-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-174">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-175">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="0d4f1-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="0d4f1-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="0d4f1-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="0d4f1-178">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-178">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-179">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-180">Prompt</span><span class="sxs-lookup"><span data-stu-id="0d4f1-180">Prompt</span></span>  <br/> |<span data-ttu-id="0d4f1-181">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0d4f1-181">xsd:string</span></span>  <br/> |<span data-ttu-id="0d4f1-182">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-182">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-183">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0d4f1-184">UniqueID</span><span class="sxs-lookup"><span data-stu-id="0d4f1-184">UniqueID</span></span>  <br/> |<span data-ttu-id="0d4f1-185">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0d4f1-185">xsd:string</span></span>  <br/> |<span data-ttu-id="0d4f1-186">необязательный</span><span class="sxs-lookup"><span data-stu-id="0d4f1-186">optional</span></span>  <br/> ||<span data-ttu-id="0d4f1-187">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0d4f1-187">Values of the xsd:string type.</span></span>  <br/> |
   

