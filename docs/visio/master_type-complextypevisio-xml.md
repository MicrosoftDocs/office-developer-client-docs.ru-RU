---
title: Master_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: b4dde4d00552525a5ec17116f96151f39c6d0957
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814197"
---
# <a name="mastertype-complextype-visio-xml"></a><span data-ttu-id="3c687-102">Master_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="3c687-102">Master_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3c687-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="3c687-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c687-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3c687-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3c687-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3c687-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3c687-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3c687-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3c687-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="3c687-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3c687-108">Нет</span><span class="sxs-lookup"><span data-stu-id="3c687-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c687-109">Определение</span><span class="sxs-lookup"><span data-stu-id="3c687-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3c687-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3c687-110">Elements and attributes</span></span>

<span data-ttu-id="3c687-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="3c687-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3c687-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3c687-112">Child elements</span></span>

|<span data-ttu-id="3c687-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3c687-113">**Element**</span></span>|<span data-ttu-id="3c687-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3c687-114">**Type**</span></span>|<span data-ttu-id="3c687-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c687-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c687-116">Icon</span><span class="sxs-lookup"><span data-stu-id="3c687-116">Icon</span></span>](icon-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c687-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="3c687-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3c687-118">PageSheet</span><span class="sxs-lookup"><span data-stu-id="3c687-118">PageSheet</span></span>](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c687-119">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="3c687-119">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3c687-120">Rel</span><span class="sxs-lookup"><span data-stu-id="3c687-120">Rel</span></span>](rel-element-master_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c687-121">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="3c687-121">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3c687-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3c687-122">Attributes</span></span>

|<span data-ttu-id="3c687-123">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3c687-123">**Attribute**</span></span>|<span data-ttu-id="3c687-124">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3c687-124">**Type**</span></span>|<span data-ttu-id="3c687-125">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="3c687-125">**Required**</span></span>|<span data-ttu-id="3c687-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c687-126">**Description**</span></span>|<span data-ttu-id="3c687-127">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3c687-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3c687-128">AlignName</span><span class="sxs-lookup"><span data-stu-id="3c687-128">AlignName</span></span>  <br/> |<span data-ttu-id="3c687-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3c687-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3c687-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-130">optional</span></span>  <br/> ||<span data-ttu-id="3c687-131">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3c687-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3c687-132">BaseID</span><span class="sxs-lookup"><span data-stu-id="3c687-132">BaseID</span></span>  <br/> |<span data-ttu-id="3c687-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3c687-133">xsd:string</span></span>  <br/> |<span data-ttu-id="3c687-134">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-134">optional</span></span>  <br/> ||<span data-ttu-id="3c687-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c687-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c687-136">Hidden</span><span class="sxs-lookup"><span data-stu-id="3c687-136">Hidden</span></span>  <br/> |<span data-ttu-id="3c687-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="3c687-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3c687-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-138">optional</span></span>  <br/> ||<span data-ttu-id="3c687-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3c687-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3c687-140">IconSize</span><span class="sxs-lookup"><span data-stu-id="3c687-140">IconSize</span></span>  <br/> |<span data-ttu-id="3c687-141">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3c687-141">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3c687-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-142">optional</span></span>  <br/> ||<span data-ttu-id="3c687-143">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3c687-143">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3c687-144">IconUpdate</span><span class="sxs-lookup"><span data-stu-id="3c687-144">IconUpdate</span></span>  <br/> |<span data-ttu-id="3c687-145">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="3c687-145">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3c687-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-146">optional</span></span>  <br/> ||<span data-ttu-id="3c687-147">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3c687-147">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3c687-148">ID</span><span class="sxs-lookup"><span data-stu-id="3c687-148">ID</span></span>  <br/> |<span data-ttu-id="3c687-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3c687-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3c687-150">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-150">required</span></span>  <br/> ||<span data-ttu-id="3c687-151">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3c687-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3c687-152">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="3c687-152">IsCustomName</span></span>  <br/> |<span data-ttu-id="3c687-153">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="3c687-153">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3c687-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-154">optional</span></span>  <br/> ||<span data-ttu-id="3c687-155">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3c687-155">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3c687-156">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="3c687-156">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="3c687-157">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="3c687-157">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3c687-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-158">optional</span></span>  <br/> ||<span data-ttu-id="3c687-159">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3c687-159">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3c687-160">MasterType</span><span class="sxs-lookup"><span data-stu-id="3c687-160">MasterType</span></span>  <br/> |<span data-ttu-id="3c687-161">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3c687-161">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3c687-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-162">optional</span></span>  <br/> ||<span data-ttu-id="3c687-163">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3c687-163">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3c687-164">MatchByName</span><span class="sxs-lookup"><span data-stu-id="3c687-164">MatchByName</span></span>  <br/> |<span data-ttu-id="3c687-165">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="3c687-165">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3c687-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-166">optional</span></span>  <br/> ||<span data-ttu-id="3c687-167">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3c687-167">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3c687-168">Имя</span><span class="sxs-lookup"><span data-stu-id="3c687-168">Name</span></span>  <br/> |<span data-ttu-id="3c687-169">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3c687-169">xsd:string</span></span>  <br/> |<span data-ttu-id="3c687-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-170">optional</span></span>  <br/> ||<span data-ttu-id="3c687-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c687-171">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c687-172">NameU</span><span class="sxs-lookup"><span data-stu-id="3c687-172">NameU</span></span>  <br/> |<span data-ttu-id="3c687-173">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3c687-173">xsd:string</span></span>  <br/> |<span data-ttu-id="3c687-174">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-174">optional</span></span>  <br/> ||<span data-ttu-id="3c687-175">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c687-175">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c687-176">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="3c687-176">PatternFlags</span></span>  <br/> |<span data-ttu-id="3c687-177">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3c687-177">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3c687-178">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-178">optional</span></span>  <br/> ||<span data-ttu-id="3c687-179">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3c687-179">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3c687-180">Запрос</span><span class="sxs-lookup"><span data-stu-id="3c687-180">Prompt</span></span>  <br/> |<span data-ttu-id="3c687-181">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3c687-181">xsd:string</span></span>  <br/> |<span data-ttu-id="3c687-182">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-182">optional</span></span>  <br/> ||<span data-ttu-id="3c687-183">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c687-183">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3c687-184">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="3c687-184">UniqueID</span></span>  <br/> |<span data-ttu-id="3c687-185">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3c687-185">xsd:string</span></span>  <br/> |<span data-ttu-id="3c687-186">необязательный</span><span class="sxs-lookup"><span data-stu-id="3c687-186">optional</span></span>  <br/> ||<span data-ttu-id="3c687-187">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3c687-187">Values of the xsd:string type.</span></span>  <br/> |
   

