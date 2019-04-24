---
title: Паже_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: d0c364164d2453c9dc64290db24890224a3c70e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334400"
---
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="ec683-102">Паже_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="ec683-102">Page_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ec683-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="ec683-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ec683-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ec683-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ec683-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ec683-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ec683-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ec683-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ec683-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="ec683-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ec683-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="ec683-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ec683-109">Определение</span><span class="sxs-lookup"><span data-stu-id="ec683-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ec683-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec683-110">Elements and attributes</span></span>

<span data-ttu-id="ec683-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ec683-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ec683-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ec683-112">Child elements</span></span>

|<span data-ttu-id="ec683-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ec683-113">**Element**</span></span>|<span data-ttu-id="ec683-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec683-114">**Type**</span></span>|<span data-ttu-id="ec683-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec683-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ec683-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="ec683-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec683-117">Пажешит_типе</span><span class="sxs-lookup"><span data-stu-id="ec683-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ec683-118">Rel</span><span class="sxs-lookup"><span data-stu-id="ec683-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ec683-119">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="ec683-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ec683-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ec683-120">Attributes</span></span>

|<span data-ttu-id="ec683-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ec683-121">**Attribute**</span></span>|<span data-ttu-id="ec683-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ec683-122">**Type**</span></span>|<span data-ttu-id="ec683-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ec683-123">**Required**</span></span>|<span data-ttu-id="ec683-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ec683-124">**Description**</span></span>|<span data-ttu-id="ec683-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ec683-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ec683-126">АссоЦиатедпаже</span><span class="sxs-lookup"><span data-stu-id="ec683-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="ec683-127">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec683-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec683-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-128">optional</span></span>  <br/> ||<span data-ttu-id="ec683-129">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec683-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec683-130">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="ec683-130">Background</span></span>  <br/> |<span data-ttu-id="ec683-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec683-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec683-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-132">optional</span></span>  <br/> ||<span data-ttu-id="ec683-133">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ec683-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec683-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="ec683-134">BackPage</span></span>  <br/> |<span data-ttu-id="ec683-135">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec683-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec683-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-136">optional</span></span>  <br/> ||<span data-ttu-id="ec683-137">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec683-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec683-138">ИД</span><span class="sxs-lookup"><span data-stu-id="ec683-138">ID</span></span>  <br/> |<span data-ttu-id="ec683-139">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec683-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec683-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-140">required</span></span>  <br/> ||<span data-ttu-id="ec683-141">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec683-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec683-142">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="ec683-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="ec683-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec683-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec683-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-144">optional</span></span>  <br/> ||<span data-ttu-id="ec683-145">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ec683-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec683-146">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="ec683-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="ec683-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="ec683-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ec683-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-148">optional</span></span>  <br/> ||<span data-ttu-id="ec683-149">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="ec683-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ec683-150">Имя</span><span class="sxs-lookup"><span data-stu-id="ec683-150">Name</span></span>  <br/> |<span data-ttu-id="ec683-151">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ec683-151">xsd:string</span></span>  <br/> |<span data-ttu-id="ec683-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-152">optional</span></span>  <br/> ||<span data-ttu-id="ec683-153">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ec683-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ec683-154">NameU</span><span class="sxs-lookup"><span data-stu-id="ec683-154">NameU</span></span>  <br/> |<span data-ttu-id="ec683-155">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="ec683-155">xsd:string</span></span>  <br/> |<span data-ttu-id="ec683-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-156">optional</span></span>  <br/> ||<span data-ttu-id="ec683-157">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="ec683-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ec683-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="ec683-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="ec683-159">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="ec683-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ec683-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-160">optional</span></span>  <br/> ||<span data-ttu-id="ec683-161">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="ec683-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ec683-162">Виевцентеркс</span><span class="sxs-lookup"><span data-stu-id="ec683-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="ec683-163">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="ec683-163">xsd:double</span></span>  <br/> |<span data-ttu-id="ec683-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-164">optional</span></span>  <br/> ||<span data-ttu-id="ec683-165">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="ec683-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ec683-166">Виевцентери</span><span class="sxs-lookup"><span data-stu-id="ec683-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="ec683-167">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="ec683-167">xsd:double</span></span>  <br/> |<span data-ttu-id="ec683-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-168">optional</span></span>  <br/> ||<span data-ttu-id="ec683-169">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="ec683-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="ec683-170">Виевскале</span><span class="sxs-lookup"><span data-stu-id="ec683-170">ViewScale</span></span>  <br/> |<span data-ttu-id="ec683-171">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="ec683-171">xsd:double</span></span>  <br/> |<span data-ttu-id="ec683-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="ec683-172">optional</span></span>  <br/> ||<span data-ttu-id="ec683-173">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="ec683-173">Values of the xsd:double type.</span></span>  <br/> |
   

