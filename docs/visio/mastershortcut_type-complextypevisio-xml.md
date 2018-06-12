---
title: MasterShortcut_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: df1e10ff11470cd87fc16efbaba6ad968df6d1b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814213"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="d5f95-102">MasterShortcut_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d5f95-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d5f95-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d5f95-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5f95-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d5f95-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d5f95-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d5f95-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d5f95-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d5f95-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d5f95-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="d5f95-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d5f95-108">Нет</span><span class="sxs-lookup"><span data-stu-id="d5f95-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5f95-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d5f95-109">Definition</span></span>

```XML
          <xs:complexType name="MasterShortcut_Type">
          
          <xs:all>
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
    <xs:attribute name="ShortcutURL"
  type="xsd:string"
    />
    <xs:attribute name="ShortcutHelp"
  type="xsd:string"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d5f95-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d5f95-110">Elements and attributes</span></span>

<span data-ttu-id="d5f95-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="d5f95-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d5f95-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d5f95-112">Child elements</span></span>

|<span data-ttu-id="d5f95-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d5f95-113">**Element**</span></span>|<span data-ttu-id="d5f95-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d5f95-114">**Type**</span></span>|<span data-ttu-id="d5f95-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5f95-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5f95-116">Icon</span><span class="sxs-lookup"><span data-stu-id="d5f95-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5f95-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="d5f95-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d5f95-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d5f95-118">Attributes</span></span>

|<span data-ttu-id="d5f95-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d5f95-119">**Attribute**</span></span>|<span data-ttu-id="d5f95-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d5f95-120">**Type**</span></span>|<span data-ttu-id="d5f95-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="d5f95-121">**Required**</span></span>|<span data-ttu-id="d5f95-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5f95-122">**Description**</span></span>|<span data-ttu-id="d5f95-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d5f95-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5f95-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="d5f95-124">AlignName</span></span>  <br/> |<span data-ttu-id="d5f95-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d5f95-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d5f95-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-126">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-127">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d5f95-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="d5f95-128">IconSize</span></span>  <br/> |<span data-ttu-id="d5f95-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d5f95-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d5f95-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-130">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-131">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d5f95-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-132">ID</span><span class="sxs-lookup"><span data-stu-id="d5f95-132">ID</span></span>  <br/> |<span data-ttu-id="d5f95-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d5f95-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d5f95-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-134">required</span></span>  <br/> ||<span data-ttu-id="d5f95-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d5f95-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="d5f95-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="d5f95-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d5f95-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d5f95-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-138">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d5f95-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="d5f95-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="d5f95-141">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d5f95-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d5f95-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-142">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-143">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d5f95-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="d5f95-144">MasterType</span></span>  <br/> |<span data-ttu-id="d5f95-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d5f95-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d5f95-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-146">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-147">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d5f95-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-148">Имя</span><span class="sxs-lookup"><span data-stu-id="d5f95-148">Name</span></span>  <br/> |<span data-ttu-id="d5f95-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d5f95-149">xsd:string</span></span>  <br/> |<span data-ttu-id="d5f95-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-150">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-151">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d5f95-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-152">NameU</span><span class="sxs-lookup"><span data-stu-id="d5f95-152">NameU</span></span>  <br/> |<span data-ttu-id="d5f95-153">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d5f95-153">xsd:string</span></span>  <br/> |<span data-ttu-id="d5f95-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-154">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d5f95-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="d5f95-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="d5f95-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="d5f95-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="d5f95-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-158">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-159">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="d5f95-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-160">Запрос</span><span class="sxs-lookup"><span data-stu-id="d5f95-160">Prompt</span></span>  <br/> |<span data-ttu-id="d5f95-161">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d5f95-161">xsd:string</span></span>  <br/> |<span data-ttu-id="d5f95-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-162">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-163">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d5f95-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="d5f95-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="d5f95-165">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d5f95-165">xsd:string</span></span>  <br/> |<span data-ttu-id="d5f95-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-166">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-167">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d5f95-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="d5f95-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="d5f95-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="d5f95-169">XSD:String</span><span class="sxs-lookup"><span data-stu-id="d5f95-169">xsd:string</span></span>  <br/> |<span data-ttu-id="d5f95-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="d5f95-170">optional</span></span>  <br/> ||<span data-ttu-id="d5f95-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d5f95-171">Values of the xsd:string type.</span></span>  <br/> |
   

