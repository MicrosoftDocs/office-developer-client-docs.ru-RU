---
title: Master_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397714"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="a1684-102">Master_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="a1684-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="a1684-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a1684-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1684-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a1684-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a1684-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a1684-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a1684-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a1684-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a1684-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a1684-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a1684-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a1684-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1684-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a1684-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="a1684-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1684-110">Elements and attributes</span></span>

<span data-ttu-id="a1684-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a1684-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a1684-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a1684-112">Child elements</span></span>

|<span data-ttu-id="a1684-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a1684-113">**Element**</span></span>|<span data-ttu-id="a1684-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a1684-114">**Type**</span></span>|<span data-ttu-id="a1684-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a1684-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1684-116">Icon</span><span class="sxs-lookup"><span data-stu-id="a1684-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1684-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="a1684-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a1684-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="a1684-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1684-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a1684-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="a1684-120">Rel</span><span class="sxs-lookup"><span data-stu-id="a1684-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1684-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="a1684-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a1684-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1684-122">Attributes</span></span>

|<span data-ttu-id="a1684-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a1684-123">**Attribute**</span></span>|<span data-ttu-id="a1684-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a1684-124">**Type**</span></span>|<span data-ttu-id="a1684-125">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a1684-125">**Required**</span></span>|<span data-ttu-id="a1684-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a1684-126">**Description**</span></span>|<span data-ttu-id="a1684-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a1684-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a1684-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="a1684-128">AlignName</span></span>  <br/> |<span data-ttu-id="a1684-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a1684-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a1684-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-130">optional</span></span>  <br/> ||<span data-ttu-id="a1684-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a1684-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a1684-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="a1684-132">BaseID</span></span>  <br/> |<span data-ttu-id="a1684-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a1684-133">xsd:string</span></span>  <br/> |<span data-ttu-id="a1684-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-134">optional</span></span>  <br/> ||<span data-ttu-id="a1684-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a1684-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a1684-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="a1684-136">Hidden</span></span>  <br/> |<span data-ttu-id="a1684-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a1684-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1684-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-138">optional</span></span>  <br/> ||<span data-ttu-id="a1684-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a1684-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a1684-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="a1684-140">IconSize</span></span>  <br/> |<span data-ttu-id="a1684-141">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a1684-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a1684-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-142">optional</span></span>  <br/> ||<span data-ttu-id="a1684-143">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a1684-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a1684-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="a1684-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="a1684-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a1684-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1684-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-146">optional</span></span>  <br/> ||<span data-ttu-id="a1684-147">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a1684-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a1684-148">ID</span><span class="sxs-lookup"><span data-stu-id="a1684-148">ID</span></span>  <br/> |<span data-ttu-id="a1684-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a1684-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a1684-150">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-150">required</span></span>  <br/> ||<span data-ttu-id="a1684-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a1684-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a1684-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="a1684-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="a1684-153">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a1684-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1684-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-154">optional</span></span>  <br/> ||<span data-ttu-id="a1684-155">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a1684-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a1684-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="a1684-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="a1684-157">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a1684-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1684-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-158">optional</span></span>  <br/> ||<span data-ttu-id="a1684-159">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a1684-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a1684-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="a1684-160">MasterType</span></span>  <br/> |<span data-ttu-id="a1684-161">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a1684-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a1684-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-162">optional</span></span>  <br/> ||<span data-ttu-id="a1684-163">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a1684-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a1684-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="a1684-164">MatchByName</span></span>  <br/> |<span data-ttu-id="a1684-165">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="a1684-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="a1684-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-166">optional</span></span>  <br/> ||<span data-ttu-id="a1684-167">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="a1684-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="a1684-168">Имя</span><span class="sxs-lookup"><span data-stu-id="a1684-168">Name</span></span>  <br/> |<span data-ttu-id="a1684-169">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a1684-169">xsd:string</span></span>  <br/> |<span data-ttu-id="a1684-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-170">optional</span></span>  <br/> ||<span data-ttu-id="a1684-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a1684-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a1684-172">NameU</span><span class="sxs-lookup"><span data-stu-id="a1684-172">NameU</span></span>  <br/> |<span data-ttu-id="a1684-173">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a1684-173">xsd:string</span></span>  <br/> |<span data-ttu-id="a1684-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-174">optional</span></span>  <br/> ||<span data-ttu-id="a1684-175">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a1684-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a1684-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="a1684-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="a1684-177">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="a1684-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="a1684-178">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-178">optional</span></span>  <br/> ||<span data-ttu-id="a1684-179">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="a1684-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="a1684-180">Запрос</span><span class="sxs-lookup"><span data-stu-id="a1684-180">Prompt</span></span>  <br/> |<span data-ttu-id="a1684-181">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a1684-181">xsd:string</span></span>  <br/> |<span data-ttu-id="a1684-182">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-182">optional</span></span>  <br/> ||<span data-ttu-id="a1684-183">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a1684-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a1684-184">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="a1684-184">UniqueID</span></span>  <br/> |<span data-ttu-id="a1684-185">XSD:String</span><span class="sxs-lookup"><span data-stu-id="a1684-185">xsd:string</span></span>  <br/> |<span data-ttu-id="a1684-186">необязательный</span><span class="sxs-lookup"><span data-stu-id="a1684-186">optional</span></span>  <br/> ||<span data-ttu-id="a1684-187">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a1684-187">Values of the xsd:string type.</span></span>  <br/> |
   

