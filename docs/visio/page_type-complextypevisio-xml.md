---
title: Page_Type complexType (Visio XML)
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
# <a name="page_type-complextype-visio-xml"></a><span data-ttu-id="58054-102">Page_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="58054-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="58054-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="58054-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="58054-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="58054-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="58054-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="58054-105">**Schema file**</span></span> <br/> |<span data-ttu-id="58054-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="58054-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="58054-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="58054-107">**Extension base**</span></span> <br/> |<span data-ttu-id="58054-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="58054-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="58054-109">Определение</span><span class="sxs-lookup"><span data-stu-id="58054-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="58054-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="58054-110">Elements and attributes</span></span>

<span data-ttu-id="58054-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="58054-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="58054-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="58054-112">Child elements</span></span>

|<span data-ttu-id="58054-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="58054-113">**Element**</span></span>|<span data-ttu-id="58054-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="58054-114">**Type**</span></span>|<span data-ttu-id="58054-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58054-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="58054-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="58054-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58054-117">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="58054-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="58054-118">Rel</span><span class="sxs-lookup"><span data-stu-id="58054-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="58054-119">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="58054-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="58054-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="58054-120">Attributes</span></span>

|<span data-ttu-id="58054-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="58054-121">**Attribute**</span></span>|<span data-ttu-id="58054-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="58054-122">**Type**</span></span>|<span data-ttu-id="58054-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="58054-123">**Required**</span></span>|<span data-ttu-id="58054-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="58054-124">**Description**</span></span>|<span data-ttu-id="58054-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="58054-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="58054-126">AssociatedPage</span><span class="sxs-lookup"><span data-stu-id="58054-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="58054-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58054-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58054-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-128">optional</span></span>  <br/> ||<span data-ttu-id="58054-129">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="58054-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58054-130">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="58054-130">Background</span></span>  <br/> |<span data-ttu-id="58054-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="58054-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="58054-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-132">optional</span></span>  <br/> ||<span data-ttu-id="58054-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="58054-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="58054-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="58054-134">BackPage</span></span>  <br/> |<span data-ttu-id="58054-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58054-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58054-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-136">optional</span></span>  <br/> ||<span data-ttu-id="58054-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="58054-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58054-138">ID</span><span class="sxs-lookup"><span data-stu-id="58054-138">ID</span></span>  <br/> |<span data-ttu-id="58054-139">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58054-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58054-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="58054-140">required</span></span>  <br/> ||<span data-ttu-id="58054-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="58054-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58054-142">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="58054-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="58054-143">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="58054-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="58054-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-144">optional</span></span>  <br/> ||<span data-ttu-id="58054-145">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="58054-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="58054-146">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="58054-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="58054-147">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="58054-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="58054-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-148">optional</span></span>  <br/> ||<span data-ttu-id="58054-149">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="58054-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="58054-150">Имя</span><span class="sxs-lookup"><span data-stu-id="58054-150">Name</span></span>  <br/> |<span data-ttu-id="58054-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="58054-151">xsd:string</span></span>  <br/> |<span data-ttu-id="58054-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-152">optional</span></span>  <br/> ||<span data-ttu-id="58054-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="58054-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58054-154">NameU</span><span class="sxs-lookup"><span data-stu-id="58054-154">NameU</span></span>  <br/> |<span data-ttu-id="58054-155">xsd:string</span><span class="sxs-lookup"><span data-stu-id="58054-155">xsd:string</span></span>  <br/> |<span data-ttu-id="58054-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-156">optional</span></span>  <br/> ||<span data-ttu-id="58054-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="58054-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="58054-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="58054-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="58054-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="58054-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="58054-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-160">optional</span></span>  <br/> ||<span data-ttu-id="58054-161">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="58054-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="58054-162">ViewCenterX</span><span class="sxs-lookup"><span data-stu-id="58054-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="58054-163">xsd:double</span><span class="sxs-lookup"><span data-stu-id="58054-163">xsd:double</span></span>  <br/> |<span data-ttu-id="58054-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-164">optional</span></span>  <br/> ||<span data-ttu-id="58054-165">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="58054-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="58054-166">ViewCenterY</span><span class="sxs-lookup"><span data-stu-id="58054-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="58054-167">xsd:double</span><span class="sxs-lookup"><span data-stu-id="58054-167">xsd:double</span></span>  <br/> |<span data-ttu-id="58054-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-168">optional</span></span>  <br/> ||<span data-ttu-id="58054-169">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="58054-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="58054-170">ViewScale</span><span class="sxs-lookup"><span data-stu-id="58054-170">ViewScale</span></span>  <br/> |<span data-ttu-id="58054-171">xsd:double</span><span class="sxs-lookup"><span data-stu-id="58054-171">xsd:double</span></span>  <br/> |<span data-ttu-id="58054-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="58054-172">optional</span></span>  <br/> ||<span data-ttu-id="58054-173">Значения типа xsd:double.</span><span class="sxs-lookup"><span data-stu-id="58054-173">Values of the xsd:double type.</span></span>  <br/> |
   

