---
title: Page_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 3a0153b724539136fe142c2489badcf9895af765
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537985"
---
# <a name="page_type-complextype-visio-xml"></a><span data-ttu-id="19054-102">Page_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="19054-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="19054-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="19054-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19054-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="19054-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="19054-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="19054-105">**Schema file**</span></span> <br/> |<span data-ttu-id="19054-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="19054-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="19054-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="19054-107">**Extension base**</span></span> <br/> |<span data-ttu-id="19054-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="19054-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19054-109">Определение</span><span class="sxs-lookup"><span data-stu-id="19054-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="19054-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="19054-110">Elements and attributes</span></span>

<span data-ttu-id="19054-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="19054-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="19054-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="19054-112">Child elements</span></span>

|<span data-ttu-id="19054-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="19054-113">**Element**</span></span>|<span data-ttu-id="19054-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="19054-114">**Type**</span></span>|<span data-ttu-id="19054-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19054-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19054-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="19054-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19054-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="19054-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="19054-118">Rel</span><span class="sxs-lookup"><span data-stu-id="19054-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19054-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="19054-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="19054-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="19054-120">Attributes</span></span>

|<span data-ttu-id="19054-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="19054-121">**Attribute**</span></span>|<span data-ttu-id="19054-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="19054-122">**Type**</span></span>|<span data-ttu-id="19054-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="19054-123">**Required**</span></span>|<span data-ttu-id="19054-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19054-124">**Description**</span></span>|<span data-ttu-id="19054-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="19054-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="19054-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="19054-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="19054-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19054-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19054-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-128">optional</span></span>  <br/> ||<span data-ttu-id="19054-129">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19054-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19054-130">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="19054-130">Background</span></span>  <br/> |<span data-ttu-id="19054-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="19054-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19054-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-132">optional</span></span>  <br/> ||<span data-ttu-id="19054-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="19054-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19054-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="19054-134">BackPage</span></span>  <br/> |<span data-ttu-id="19054-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19054-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19054-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-136">optional</span></span>  <br/> ||<span data-ttu-id="19054-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19054-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19054-138">ID</span><span class="sxs-lookup"><span data-stu-id="19054-138">ID</span></span>  <br/> |<span data-ttu-id="19054-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19054-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19054-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="19054-140">required</span></span>  <br/> ||<span data-ttu-id="19054-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19054-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19054-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="19054-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="19054-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="19054-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19054-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-144">optional</span></span>  <br/> ||<span data-ttu-id="19054-145">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="19054-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19054-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="19054-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="19054-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="19054-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="19054-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-148">optional</span></span>  <br/> ||<span data-ttu-id="19054-149">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="19054-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="19054-150">Имя</span><span class="sxs-lookup"><span data-stu-id="19054-150">Name</span></span>  <br/> |<span data-ttu-id="19054-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19054-151">xsd:string</span></span>  <br/> |<span data-ttu-id="19054-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-152">optional</span></span>  <br/> ||<span data-ttu-id="19054-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19054-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19054-154">NameU</span><span class="sxs-lookup"><span data-stu-id="19054-154">NameU</span></span>  <br/> |<span data-ttu-id="19054-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="19054-155">xsd:string</span></span>  <br/> |<span data-ttu-id="19054-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-156">optional</span></span>  <br/> ||<span data-ttu-id="19054-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="19054-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="19054-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="19054-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="19054-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="19054-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="19054-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-160">optional</span></span>  <br/> ||<span data-ttu-id="19054-161">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="19054-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="19054-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="19054-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="19054-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="19054-163">xsd:double</span></span>  <br/> |<span data-ttu-id="19054-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-164">optional</span></span>  <br/> ||<span data-ttu-id="19054-165">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="19054-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="19054-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="19054-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="19054-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="19054-167">xsd:double</span></span>  <br/> |<span data-ttu-id="19054-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-168">optional</span></span>  <br/> ||<span data-ttu-id="19054-169">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="19054-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="19054-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="19054-170">ViewScale</span></span>  <br/> |<span data-ttu-id="19054-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="19054-171">xsd:double</span></span>  <br/> |<span data-ttu-id="19054-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="19054-172">optional</span></span>  <br/> ||<span data-ttu-id="19054-173">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="19054-173">Values of the xsd:double type.</span></span>  <br/> |
   

