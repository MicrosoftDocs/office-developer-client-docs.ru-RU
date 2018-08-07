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
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="67347-102">MasterShortcut_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="67347-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="67347-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="67347-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67347-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="67347-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="67347-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="67347-105">**Schema file**</span></span> <br/> |<span data-ttu-id="67347-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="67347-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="67347-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="67347-107">**Extension base**</span></span> <br/> |<span data-ttu-id="67347-108">Нет</span><span class="sxs-lookup"><span data-stu-id="67347-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67347-109">Определение</span><span class="sxs-lookup"><span data-stu-id="67347-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="67347-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="67347-110">Elements and attributes</span></span>

<span data-ttu-id="67347-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="67347-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="67347-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="67347-112">Child elements</span></span>

|<span data-ttu-id="67347-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="67347-113">**Element**</span></span>|<span data-ttu-id="67347-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="67347-114">**Type**</span></span>|<span data-ttu-id="67347-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="67347-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67347-116">Icon</span><span class="sxs-lookup"><span data-stu-id="67347-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67347-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="67347-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="67347-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="67347-118">Attributes</span></span>

|<span data-ttu-id="67347-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="67347-119">**Attribute**</span></span>|<span data-ttu-id="67347-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="67347-120">**Type**</span></span>|<span data-ttu-id="67347-121">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="67347-121">**Required**</span></span>|<span data-ttu-id="67347-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="67347-122">**Description**</span></span>|<span data-ttu-id="67347-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="67347-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="67347-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="67347-124">AlignName</span></span>  <br/> |<span data-ttu-id="67347-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="67347-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="67347-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-126">optional</span></span>  <br/> ||<span data-ttu-id="67347-127">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="67347-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="67347-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="67347-128">IconSize</span></span>  <br/> |<span data-ttu-id="67347-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="67347-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="67347-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-130">optional</span></span>  <br/> ||<span data-ttu-id="67347-131">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="67347-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="67347-132">ID</span><span class="sxs-lookup"><span data-stu-id="67347-132">ID</span></span>  <br/> |<span data-ttu-id="67347-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="67347-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="67347-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="67347-134">required</span></span>  <br/> ||<span data-ttu-id="67347-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="67347-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="67347-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="67347-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="67347-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="67347-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="67347-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-138">optional</span></span>  <br/> ||<span data-ttu-id="67347-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="67347-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="67347-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="67347-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="67347-141">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="67347-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="67347-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-142">optional</span></span>  <br/> ||<span data-ttu-id="67347-143">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="67347-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="67347-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="67347-144">MasterType</span></span>  <br/> |<span data-ttu-id="67347-145">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="67347-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="67347-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-146">optional</span></span>  <br/> ||<span data-ttu-id="67347-147">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="67347-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="67347-148">Имя</span><span class="sxs-lookup"><span data-stu-id="67347-148">Name</span></span>  <br/> |<span data-ttu-id="67347-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="67347-149">xsd:string</span></span>  <br/> |<span data-ttu-id="67347-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-150">optional</span></span>  <br/> ||<span data-ttu-id="67347-151">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="67347-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67347-152">NameU</span><span class="sxs-lookup"><span data-stu-id="67347-152">NameU</span></span>  <br/> |<span data-ttu-id="67347-153">XSD:String</span><span class="sxs-lookup"><span data-stu-id="67347-153">xsd:string</span></span>  <br/> |<span data-ttu-id="67347-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-154">optional</span></span>  <br/> ||<span data-ttu-id="67347-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="67347-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67347-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="67347-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="67347-157">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="67347-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="67347-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-158">optional</span></span>  <br/> ||<span data-ttu-id="67347-159">Значения типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="67347-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="67347-160">Запрос</span><span class="sxs-lookup"><span data-stu-id="67347-160">Prompt</span></span>  <br/> |<span data-ttu-id="67347-161">XSD:String</span><span class="sxs-lookup"><span data-stu-id="67347-161">xsd:string</span></span>  <br/> |<span data-ttu-id="67347-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-162">optional</span></span>  <br/> ||<span data-ttu-id="67347-163">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="67347-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67347-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="67347-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="67347-165">XSD:String</span><span class="sxs-lookup"><span data-stu-id="67347-165">xsd:string</span></span>  <br/> |<span data-ttu-id="67347-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-166">optional</span></span>  <br/> ||<span data-ttu-id="67347-167">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="67347-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="67347-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="67347-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="67347-169">XSD:String</span><span class="sxs-lookup"><span data-stu-id="67347-169">xsd:string</span></span>  <br/> |<span data-ttu-id="67347-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="67347-170">optional</span></span>  <br/> ||<span data-ttu-id="67347-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="67347-171">Values of the xsd:string type.</span></span>  <br/> |
   

