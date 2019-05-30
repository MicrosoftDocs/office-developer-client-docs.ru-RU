---
title: Мастершорткут_типе complexType (XML для Visio)
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
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="52bac-102">Мастершорткут_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="52bac-102">MasterShortcut_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="52bac-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="52bac-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52bac-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="52bac-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="52bac-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="52bac-105">**Schema file**</span></span> <br/> |<span data-ttu-id="52bac-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="52bac-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="52bac-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="52bac-107">**Extension base**</span></span> <br/> |<span data-ttu-id="52bac-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="52bac-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52bac-109">Определение</span><span class="sxs-lookup"><span data-stu-id="52bac-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="52bac-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="52bac-110">Elements and attributes</span></span>

<span data-ttu-id="52bac-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="52bac-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="52bac-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="52bac-112">Child elements</span></span>

|<span data-ttu-id="52bac-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="52bac-113">**Element**</span></span>|<span data-ttu-id="52bac-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="52bac-114">**Type**</span></span>|<span data-ttu-id="52bac-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="52bac-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="52bac-116">Icon</span><span class="sxs-lookup"><span data-stu-id="52bac-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="52bac-117">Икон_типе</span><span class="sxs-lookup"><span data-stu-id="52bac-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="52bac-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="52bac-118">Attributes</span></span>

|<span data-ttu-id="52bac-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="52bac-119">**Attribute**</span></span>|<span data-ttu-id="52bac-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="52bac-120">**Type**</span></span>|<span data-ttu-id="52bac-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="52bac-121">**Required**</span></span>|<span data-ttu-id="52bac-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="52bac-122">**Description**</span></span>|<span data-ttu-id="52bac-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="52bac-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="52bac-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="52bac-124">AlignName</span></span>  <br/> |<span data-ttu-id="52bac-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52bac-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52bac-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-126">optional</span></span>  <br/> ||<span data-ttu-id="52bac-127">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="52bac-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52bac-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="52bac-128">IconSize</span></span>  <br/> |<span data-ttu-id="52bac-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52bac-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52bac-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-130">optional</span></span>  <br/> ||<span data-ttu-id="52bac-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="52bac-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52bac-132">ID</span><span class="sxs-lookup"><span data-stu-id="52bac-132">ID</span></span>  <br/> |<span data-ttu-id="52bac-133">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="52bac-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="52bac-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-134">required</span></span>  <br/> ||<span data-ttu-id="52bac-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="52bac-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="52bac-136">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="52bac-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="52bac-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="52bac-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="52bac-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-138">optional</span></span>  <br/> ||<span data-ttu-id="52bac-139">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="52bac-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="52bac-140">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="52bac-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="52bac-141">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="52bac-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="52bac-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-142">optional</span></span>  <br/> ||<span data-ttu-id="52bac-143">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="52bac-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="52bac-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="52bac-144">MasterType</span></span>  <br/> |<span data-ttu-id="52bac-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52bac-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52bac-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-146">optional</span></span>  <br/> ||<span data-ttu-id="52bac-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="52bac-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52bac-148">Имя</span><span class="sxs-lookup"><span data-stu-id="52bac-148">Name</span></span>  <br/> |<span data-ttu-id="52bac-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="52bac-149">xsd:string</span></span>  <br/> |<span data-ttu-id="52bac-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-150">optional</span></span>  <br/> ||<span data-ttu-id="52bac-151">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="52bac-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52bac-152">NameU</span><span class="sxs-lookup"><span data-stu-id="52bac-152">NameU</span></span>  <br/> |<span data-ttu-id="52bac-153">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="52bac-153">xsd:string</span></span>  <br/> |<span data-ttu-id="52bac-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-154">optional</span></span>  <br/> ||<span data-ttu-id="52bac-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="52bac-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52bac-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="52bac-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="52bac-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="52bac-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="52bac-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-158">optional</span></span>  <br/> ||<span data-ttu-id="52bac-159">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="52bac-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="52bac-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="52bac-160">Prompt</span></span>  <br/> |<span data-ttu-id="52bac-161">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="52bac-161">xsd:string</span></span>  <br/> |<span data-ttu-id="52bac-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-162">optional</span></span>  <br/> ||<span data-ttu-id="52bac-163">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="52bac-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52bac-164">Шорткуселп</span><span class="sxs-lookup"><span data-stu-id="52bac-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="52bac-165">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="52bac-165">xsd:string</span></span>  <br/> |<span data-ttu-id="52bac-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-166">optional</span></span>  <br/> ||<span data-ttu-id="52bac-167">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="52bac-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="52bac-168">Шорткутурл</span><span class="sxs-lookup"><span data-stu-id="52bac-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="52bac-169">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="52bac-169">xsd:string</span></span>  <br/> |<span data-ttu-id="52bac-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="52bac-170">optional</span></span>  <br/> ||<span data-ttu-id="52bac-171">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="52bac-171">Values of the xsd:string type.</span></span>  <br/> |
   

