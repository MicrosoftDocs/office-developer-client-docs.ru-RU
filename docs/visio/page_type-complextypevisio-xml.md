---
title: Page_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401554"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="32750-102">Page_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="32750-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="32750-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="32750-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32750-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="32750-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="32750-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="32750-105">**Schema file**</span></span> <br/> |<span data-ttu-id="32750-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="32750-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="32750-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="32750-107">**Extension base**</span></span> <br/> |<span data-ttu-id="32750-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="32750-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="32750-109">Определение</span><span class="sxs-lookup"><span data-stu-id="32750-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="32750-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="32750-110">Elements and attributes</span></span>

<span data-ttu-id="32750-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="32750-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="32750-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="32750-112">Child elements</span></span>

|<span data-ttu-id="32750-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="32750-113">**Element**</span></span>|<span data-ttu-id="32750-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="32750-114">**Type**</span></span>|<span data-ttu-id="32750-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32750-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32750-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="32750-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="32750-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="32750-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="32750-118">Rel</span><span class="sxs-lookup"><span data-stu-id="32750-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="32750-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="32750-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="32750-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="32750-120">Attributes</span></span>

|<span data-ttu-id="32750-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="32750-121">**Attribute**</span></span>|<span data-ttu-id="32750-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="32750-122">**Type**</span></span>|<span data-ttu-id="32750-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="32750-123">**Required**</span></span>|<span data-ttu-id="32750-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32750-124">**Description**</span></span>|<span data-ttu-id="32750-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="32750-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="32750-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="32750-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="32750-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32750-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32750-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-128">optional</span></span>  <br/> ||<span data-ttu-id="32750-129">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32750-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32750-130">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="32750-130">Background</span></span>  <br/> |<span data-ttu-id="32750-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="32750-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="32750-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-132">optional</span></span>  <br/> ||<span data-ttu-id="32750-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="32750-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="32750-134">Обратная сторона</span><span class="sxs-lookup"><span data-stu-id="32750-134">BackPage</span></span>  <br/> |<span data-ttu-id="32750-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32750-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32750-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-136">optional</span></span>  <br/> ||<span data-ttu-id="32750-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32750-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32750-138">ID</span><span class="sxs-lookup"><span data-stu-id="32750-138">ID</span></span>  <br/> |<span data-ttu-id="32750-139">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32750-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32750-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="32750-140">required</span></span>  <br/> ||<span data-ttu-id="32750-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32750-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32750-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="32750-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="32750-143">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="32750-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="32750-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-144">optional</span></span>  <br/> ||<span data-ttu-id="32750-145">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="32750-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="32750-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="32750-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="32750-147">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="32750-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="32750-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-148">optional</span></span>  <br/> ||<span data-ttu-id="32750-149">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="32750-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="32750-150">Имя</span><span class="sxs-lookup"><span data-stu-id="32750-150">Name</span></span>  <br/> |<span data-ttu-id="32750-151">XSD:String</span><span class="sxs-lookup"><span data-stu-id="32750-151">xsd:string</span></span>  <br/> |<span data-ttu-id="32750-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-152">optional</span></span>  <br/> ||<span data-ttu-id="32750-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="32750-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="32750-154">NameU</span><span class="sxs-lookup"><span data-stu-id="32750-154">NameU</span></span>  <br/> |<span data-ttu-id="32750-155">XSD:String</span><span class="sxs-lookup"><span data-stu-id="32750-155">xsd:string</span></span>  <br/> |<span data-ttu-id="32750-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-156">optional</span></span>  <br/> ||<span data-ttu-id="32750-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="32750-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="32750-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="32750-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="32750-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="32750-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="32750-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-160">optional</span></span>  <br/> ||<span data-ttu-id="32750-161">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="32750-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="32750-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="32750-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="32750-163">XSD: double</span><span class="sxs-lookup"><span data-stu-id="32750-163">xsd:double</span></span>  <br/> |<span data-ttu-id="32750-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-164">optional</span></span>  <br/> ||<span data-ttu-id="32750-165">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="32750-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="32750-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="32750-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="32750-167">XSD: double</span><span class="sxs-lookup"><span data-stu-id="32750-167">xsd:double</span></span>  <br/> |<span data-ttu-id="32750-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-168">optional</span></span>  <br/> ||<span data-ttu-id="32750-169">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="32750-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="32750-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="32750-170">ViewScale</span></span>  <br/> |<span data-ttu-id="32750-171">XSD: double</span><span class="sxs-lookup"><span data-stu-id="32750-171">xsd:double</span></span>  <br/> |<span data-ttu-id="32750-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="32750-172">optional</span></span>  <br/> ||<span data-ttu-id="32750-173">Значения типа XSD: double.</span><span class="sxs-lookup"><span data-stu-id="32750-173">Values of the xsd:double type.</span></span>  <br/> |
   

