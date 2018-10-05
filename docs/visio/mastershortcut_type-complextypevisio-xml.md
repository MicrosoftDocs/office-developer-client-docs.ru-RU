---
title: MasterShortcut_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0192c733-09b8-d9ce-1d88-b4d97e2e1a36
ms.openlocfilehash: 23d5de92be151b9ab6819296456746087573e7c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396486"
---
# <a name="mastershortcuttype-complextype-visio-xml"></a><span data-ttu-id="1505f-102">MasterShortcut_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1505f-102">MasterShortcut_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1505f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1505f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1505f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1505f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1505f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1505f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1505f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1505f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1505f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1505f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1505f-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1505f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1505f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1505f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1505f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1505f-110">Elements and attributes</span></span>

<span data-ttu-id="1505f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1505f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1505f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1505f-112">Child elements</span></span>

|<span data-ttu-id="1505f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1505f-113">**Element**</span></span>|<span data-ttu-id="1505f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1505f-114">**Type**</span></span>|<span data-ttu-id="1505f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1505f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1505f-116">Icon</span><span class="sxs-lookup"><span data-stu-id="1505f-116">Icon</span></span>](icon-element-mastershortcut_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1505f-117">Icon_Type</span><span class="sxs-lookup"><span data-stu-id="1505f-117">Icon_Type</span></span>](icon_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1505f-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1505f-118">Attributes</span></span>

|<span data-ttu-id="1505f-119">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1505f-119">**Attribute**</span></span>|<span data-ttu-id="1505f-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1505f-120">**Type**</span></span>|<span data-ttu-id="1505f-121">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1505f-121">**Required**</span></span>|<span data-ttu-id="1505f-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1505f-122">**Description**</span></span>|<span data-ttu-id="1505f-123">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1505f-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1505f-124">AlignName</span><span class="sxs-lookup"><span data-stu-id="1505f-124">AlignName</span></span>  <br/> |<span data-ttu-id="1505f-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1505f-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1505f-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-126">optional</span></span>  <br/> ||<span data-ttu-id="1505f-127">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1505f-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1505f-128">IconSize</span><span class="sxs-lookup"><span data-stu-id="1505f-128">IconSize</span></span>  <br/> |<span data-ttu-id="1505f-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1505f-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1505f-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-130">optional</span></span>  <br/> ||<span data-ttu-id="1505f-131">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1505f-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1505f-132">ID</span><span class="sxs-lookup"><span data-stu-id="1505f-132">ID</span></span>  <br/> |<span data-ttu-id="1505f-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1505f-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1505f-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-134">required</span></span>  <br/> ||<span data-ttu-id="1505f-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1505f-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1505f-136">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="1505f-136">IsCustomName</span></span>  <br/> |<span data-ttu-id="1505f-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="1505f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1505f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-138">optional</span></span>  <br/> ||<span data-ttu-id="1505f-139">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1505f-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1505f-140">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="1505f-140">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="1505f-141">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="1505f-141">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1505f-142">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-142">optional</span></span>  <br/> ||<span data-ttu-id="1505f-143">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1505f-143">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1505f-144">MasterType</span><span class="sxs-lookup"><span data-stu-id="1505f-144">MasterType</span></span>  <br/> |<span data-ttu-id="1505f-145">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1505f-145">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1505f-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-146">optional</span></span>  <br/> ||<span data-ttu-id="1505f-147">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1505f-147">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1505f-148">Имя</span><span class="sxs-lookup"><span data-stu-id="1505f-148">Name</span></span>  <br/> |<span data-ttu-id="1505f-149">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1505f-149">xsd:string</span></span>  <br/> |<span data-ttu-id="1505f-150">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-150">optional</span></span>  <br/> ||<span data-ttu-id="1505f-151">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1505f-151">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1505f-152">NameU</span><span class="sxs-lookup"><span data-stu-id="1505f-152">NameU</span></span>  <br/> |<span data-ttu-id="1505f-153">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1505f-153">xsd:string</span></span>  <br/> |<span data-ttu-id="1505f-154">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-154">optional</span></span>  <br/> ||<span data-ttu-id="1505f-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1505f-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1505f-156">PatternFlags</span><span class="sxs-lookup"><span data-stu-id="1505f-156">PatternFlags</span></span>  <br/> |<span data-ttu-id="1505f-157">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="1505f-157">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="1505f-158">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-158">optional</span></span>  <br/> ||<span data-ttu-id="1505f-159">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="1505f-159">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="1505f-160">Запрос</span><span class="sxs-lookup"><span data-stu-id="1505f-160">Prompt</span></span>  <br/> |<span data-ttu-id="1505f-161">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1505f-161">xsd:string</span></span>  <br/> |<span data-ttu-id="1505f-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-162">optional</span></span>  <br/> ||<span data-ttu-id="1505f-163">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1505f-163">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1505f-164">ShortcutHelp</span><span class="sxs-lookup"><span data-stu-id="1505f-164">ShortcutHelp</span></span>  <br/> |<span data-ttu-id="1505f-165">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1505f-165">xsd:string</span></span>  <br/> |<span data-ttu-id="1505f-166">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-166">optional</span></span>  <br/> ||<span data-ttu-id="1505f-167">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1505f-167">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1505f-168">ShortcutURL</span><span class="sxs-lookup"><span data-stu-id="1505f-168">ShortcutURL</span></span>  <br/> |<span data-ttu-id="1505f-169">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1505f-169">xsd:string</span></span>  <br/> |<span data-ttu-id="1505f-170">необязательный</span><span class="sxs-lookup"><span data-stu-id="1505f-170">optional</span></span>  <br/> ||<span data-ttu-id="1505f-171">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1505f-171">Values of the xsd:string type.</span></span>  <br/> |
   

