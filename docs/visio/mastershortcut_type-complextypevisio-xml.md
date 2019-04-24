---
title: Мастершорткут_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341694"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="7c337-102">Мастершорткут_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7c337-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7c337-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7c337-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c337-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7c337-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7c337-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7c337-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7c337-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7c337-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7c337-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7c337-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7c337-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="7c337-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c337-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7c337-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7c337-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7c337-110">Elements and attributes</span></span>

<span data-ttu-id="7c337-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7c337-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7c337-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7c337-112">Child elements</span></span>

|<span data-ttu-id="7c337-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7c337-113">**Element**</span></span>|<span data-ttu-id="7c337-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7c337-114">**Type**</span></span>|<span data-ttu-id="7c337-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7c337-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c337-116">Icon</span><span class="sxs-lookup"><span data-stu-id="7c337-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c337-117">Икон_типе</span><span class="sxs-lookup"><span data-stu-id="7c337-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7c337-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7c337-118">Attributes</span></span>

|<span data-ttu-id="7c337-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7c337-119">**Attribute**</span></span>|<span data-ttu-id="7c337-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7c337-120">**Type**</span></span>|<span data-ttu-id="7c337-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7c337-121">**Required**</span></span>|<span data-ttu-id="7c337-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7c337-122">**Description**</span></span>|<span data-ttu-id="7c337-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7c337-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7c337-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="7c337-124">AlignName</span></span>  <br/> |<span data-ttu-id="7c337-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7c337-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7c337-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-126">optional</span></span>  <br/> ||<span data-ttu-id="7c337-127">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="7c337-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7c337-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="7c337-128">IconSize</span></span>  <br/> |<span data-ttu-id="7c337-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7c337-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7c337-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-130">optional</span></span>  <br/> ||<span data-ttu-id="7c337-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="7c337-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7c337-132">ИД</span><span class="sxs-lookup"><span data-stu-id="7c337-132">ID</span></span>  <br/> |<span data-ttu-id="7c337-133">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="7c337-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c337-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-134">required</span></span>  <br/> ||<span data-ttu-id="7c337-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="7c337-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c337-136">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="7c337-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="7c337-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="7c337-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7c337-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-138">optional</span></span>  <br/> ||<span data-ttu-id="7c337-139">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7c337-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7c337-140">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="7c337-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="7c337-141">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="7c337-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7c337-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-142">optional</span></span>  <br/> ||<span data-ttu-id="7c337-143">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7c337-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7c337-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="7c337-144">MasterType</span></span>  <br/> |<span data-ttu-id="7c337-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7c337-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7c337-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-146">optional</span></span>  <br/> ||<span data-ttu-id="7c337-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="7c337-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7c337-148">Имя</span><span class="sxs-lookup"><span data-stu-id="7c337-148">Name</span></span>  <br/> |<span data-ttu-id="7c337-149">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7c337-149">xsd:string</span></span>  <br/> |<span data-ttu-id="7c337-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-150">optional</span></span>  <br/> ||<span data-ttu-id="7c337-151">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7c337-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c337-152">NameU</span><span class="sxs-lookup"><span data-stu-id="7c337-152">NameU</span></span>  <br/> |<span data-ttu-id="7c337-153">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7c337-153">xsd:string</span></span>  <br/> |<span data-ttu-id="7c337-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-154">optional</span></span>  <br/> ||<span data-ttu-id="7c337-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7c337-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c337-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="7c337-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="7c337-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="7c337-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="7c337-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-158">optional</span></span>  <br/> ||<span data-ttu-id="7c337-159">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="7c337-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="7c337-160">Prompt</span><span class="sxs-lookup"><span data-stu-id="7c337-160">Prompt</span></span>  <br/> |<span data-ttu-id="7c337-161">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7c337-161">xsd:string</span></span>  <br/> |<span data-ttu-id="7c337-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-162">optional</span></span>  <br/> ||<span data-ttu-id="7c337-163">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7c337-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c337-164">Шорткуселп</span><span class="sxs-lookup"><span data-stu-id="7c337-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="7c337-165">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7c337-165">xsd:string</span></span>  <br/> |<span data-ttu-id="7c337-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-166">optional</span></span>  <br/> ||<span data-ttu-id="7c337-167">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7c337-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c337-168">Шорткутурл</span><span class="sxs-lookup"><span data-stu-id="7c337-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="7c337-169">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="7c337-169">xsd:string</span></span>  <br/> |<span data-ttu-id="7c337-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="7c337-170">optional</span></span>  <br/> ||<span data-ttu-id="7c337-171">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="7c337-171">Values of the xsd:string type.</span></span>  <br/> |
   

