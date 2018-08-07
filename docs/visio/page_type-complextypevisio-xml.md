---
title: Page_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: b3a4916f3de20d9350b6673a6000d56f3030b66e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814327"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="1fb7e-102">Page_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1fb7e-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1fb7e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1fb7e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fb7e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1fb7e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1fb7e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1fb7e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1fb7e-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1fb7e-108">Нет</span><span class="sxs-lookup"><span data-stu-id="1fb7e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1fb7e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1fb7e-109">Definition</span></span>

```XML
          <xs:complexType name="Page_Type">
          
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
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1fb7e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1fb7e-110">Elements and attributes</span></span>

<span data-ttu-id="1fb7e-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1fb7e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1fb7e-112">Child elements</span></span>

|<span data-ttu-id="1fb7e-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-113">**Element**</span></span>|<span data-ttu-id="1fb7e-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-114">**Type**</span></span>|<span data-ttu-id="1fb7e-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1fb7e-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="1fb7e-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1fb7e-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1fb7e-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1fb7e-118">Rel</span><span class="sxs-lookup"><span data-stu-id="1fb7e-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1fb7e-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="1fb7e-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1fb7e-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1fb7e-120">Attributes</span></span>

|<span data-ttu-id="1fb7e-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-121">**Attribute**</span></span>|<span data-ttu-id="1fb7e-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-122">**Type**</span></span>|<span data-ttu-id="1fb7e-123">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-123">**Required**</span></span>|<span data-ttu-id="1fb7e-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-124">**Description**</span></span>|<span data-ttu-id="1fb7e-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1fb7e-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1fb7e-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="1fb7e-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="1fb7e-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1fb7e-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1fb7e-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-128">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-129">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-130">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="1fb7e-130">Background</span></span>  <br/> |<span data-ttu-id="1fb7e-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="1fb7e-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1fb7e-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-132">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-134">Обратная сторона</span><span class="sxs-lookup"><span data-stu-id="1fb7e-134">BackPage</span></span>  <br/> |<span data-ttu-id="1fb7e-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1fb7e-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1fb7e-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-136">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-138">ID</span><span class="sxs-lookup"><span data-stu-id="1fb7e-138">ID</span></span>  <br/> |<span data-ttu-id="1fb7e-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1fb7e-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1fb7e-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-140">required</span></span>  <br/> ||<span data-ttu-id="1fb7e-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="1fb7e-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="1fb7e-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="1fb7e-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1fb7e-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-144">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-145">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="1fb7e-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="1fb7e-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="1fb7e-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1fb7e-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-148">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-149">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-150">Имя</span><span class="sxs-lookup"><span data-stu-id="1fb7e-150">Name</span></span>  <br/> |<span data-ttu-id="1fb7e-151">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1fb7e-151">xsd:string</span></span>  <br/> |<span data-ttu-id="1fb7e-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-152">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-154">NameU</span><span class="sxs-lookup"><span data-stu-id="1fb7e-154">NameU</span></span>  <br/> |<span data-ttu-id="1fb7e-155">XSD:String</span><span class="sxs-lookup"><span data-stu-id="1fb7e-155">xsd:string</span></span>  <br/> |<span data-ttu-id="1fb7e-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-156">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="1fb7e-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="1fb7e-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1fb7e-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1fb7e-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-160">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-161">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="1fb7e-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="1fb7e-163">XSD: double</span><span class="sxs-lookup"><span data-stu-id="1fb7e-163">xsd:double</span></span>  <br/> |<span data-ttu-id="1fb7e-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-164">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-165">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="1fb7e-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="1fb7e-167">XSD: double</span><span class="sxs-lookup"><span data-stu-id="1fb7e-167">xsd:double</span></span>  <br/> |<span data-ttu-id="1fb7e-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-168">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-169">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="1fb7e-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="1fb7e-170">ViewScale</span></span>  <br/> |<span data-ttu-id="1fb7e-171">XSD: double</span><span class="sxs-lookup"><span data-stu-id="1fb7e-171">xsd:double</span></span>  <br/> |<span data-ttu-id="1fb7e-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="1fb7e-172">optional</span></span>  <br/> ||<span data-ttu-id="1fb7e-173">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="1fb7e-173">Values of the xsd:double type.</span></span>  <br/> |
   

