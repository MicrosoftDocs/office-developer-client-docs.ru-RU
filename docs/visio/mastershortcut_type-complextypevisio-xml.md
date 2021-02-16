---
title: MasterShortcut_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: ed8dd8ef985c814e41017526144bd7ec8cb63424
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538062"
---
# <a name="mastershortcut_type-complextype-visio-xml"></a><span data-ttu-id="86967-102">MasterShortcut_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="86967-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="86967-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="86967-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86967-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="86967-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="86967-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="86967-105">**Schema file**</span></span> <br/> |<span data-ttu-id="86967-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="86967-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="86967-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="86967-107">**Extension base**</span></span> <br/> |<span data-ttu-id="86967-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="86967-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86967-109">Определение</span><span class="sxs-lookup"><span data-stu-id="86967-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="86967-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="86967-110">Elements and attributes</span></span>

<span data-ttu-id="86967-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="86967-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="86967-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="86967-112">Child elements</span></span>

|<span data-ttu-id="86967-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="86967-113">**Element**</span></span>|<span data-ttu-id="86967-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="86967-114">**Type**</span></span>|<span data-ttu-id="86967-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="86967-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86967-116">Icon</span><span class="sxs-lookup"><span data-stu-id="86967-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86967-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="86967-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="86967-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="86967-118">Attributes</span></span>

|<span data-ttu-id="86967-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="86967-119">**Attribute**</span></span>|<span data-ttu-id="86967-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="86967-120">**Type**</span></span>|<span data-ttu-id="86967-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="86967-121">**Required**</span></span>|<span data-ttu-id="86967-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="86967-122">**Description**</span></span>|<span data-ttu-id="86967-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="86967-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="86967-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="86967-124">AlignName</span></span>  <br/> |<span data-ttu-id="86967-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="86967-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="86967-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-126">optional</span></span>  <br/> ||<span data-ttu-id="86967-127">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="86967-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="86967-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="86967-128">IconSize</span></span>  <br/> |<span data-ttu-id="86967-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="86967-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="86967-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-130">optional</span></span>  <br/> ||<span data-ttu-id="86967-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="86967-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="86967-132">ID</span><span class="sxs-lookup"><span data-stu-id="86967-132">ID</span></span>  <br/> |<span data-ttu-id="86967-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="86967-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="86967-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="86967-134">required</span></span>  <br/> ||<span data-ttu-id="86967-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="86967-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="86967-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="86967-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="86967-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="86967-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="86967-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-138">optional</span></span>  <br/> ||<span data-ttu-id="86967-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="86967-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="86967-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="86967-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="86967-141">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="86967-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="86967-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-142">optional</span></span>  <br/> ||<span data-ttu-id="86967-143">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="86967-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="86967-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="86967-144">MasterType</span></span>  <br/> |<span data-ttu-id="86967-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="86967-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="86967-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-146">optional</span></span>  <br/> ||<span data-ttu-id="86967-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="86967-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="86967-148">Имя</span><span class="sxs-lookup"><span data-stu-id="86967-148">Name</span></span>  <br/> |<span data-ttu-id="86967-149">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86967-149">xsd:string</span></span>  <br/> |<span data-ttu-id="86967-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-150">optional</span></span>  <br/> ||<span data-ttu-id="86967-151">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="86967-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="86967-152">NameU</span><span class="sxs-lookup"><span data-stu-id="86967-152">NameU</span></span>  <br/> |<span data-ttu-id="86967-153">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86967-153">xsd:string</span></span>  <br/> |<span data-ttu-id="86967-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-154">optional</span></span>  <br/> ||<span data-ttu-id="86967-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="86967-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="86967-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="86967-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="86967-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="86967-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="86967-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-158">optional</span></span>  <br/> ||<span data-ttu-id="86967-159">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="86967-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="86967-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="86967-160">Prompt</span></span>  <br/> |<span data-ttu-id="86967-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86967-161">xsd:string</span></span>  <br/> |<span data-ttu-id="86967-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-162">optional</span></span>  <br/> ||<span data-ttu-id="86967-163">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="86967-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="86967-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="86967-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="86967-165">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86967-165">xsd:string</span></span>  <br/> |<span data-ttu-id="86967-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-166">optional</span></span>  <br/> ||<span data-ttu-id="86967-167">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="86967-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="86967-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="86967-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="86967-169">xsd:string</span><span class="sxs-lookup"><span data-stu-id="86967-169">xsd:string</span></span>  <br/> |<span data-ttu-id="86967-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="86967-170">optional</span></span>  <br/> ||<span data-ttu-id="86967-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="86967-171">Values of the xsd:string type.</span></span>  <br/> |
   

