---
title: Паже_типе complexType (XML для Visio)
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
# <a name="pagetype-complextype-visio-xml"></a><span data-ttu-id="3a422-102">Паже_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="3a422-102">Page_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3a422-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="3a422-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a422-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3a422-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3a422-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3a422-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3a422-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3a422-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3a422-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="3a422-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3a422-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="3a422-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3a422-109">Определение</span><span class="sxs-lookup"><span data-stu-id="3a422-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3a422-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3a422-110">Elements and attributes</span></span>

<span data-ttu-id="3a422-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3a422-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3a422-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3a422-112">Child elements</span></span>

|<span data-ttu-id="3a422-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3a422-113">**Element**</span></span>|<span data-ttu-id="3a422-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3a422-114">**Type**</span></span>|<span data-ttu-id="3a422-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a422-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3a422-116">PageSheet</span><span class="sxs-lookup"><span data-stu-id="3a422-116">PageSheet</span></span>](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3a422-117">Пажешит_типе</span><span class="sxs-lookup"><span data-stu-id="3a422-117">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3a422-118">Rel</span><span class="sxs-lookup"><span data-stu-id="3a422-118">Rel</span></span>](rel-element-page_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3a422-119">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="3a422-119">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3a422-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3a422-120">Attributes</span></span>

|<span data-ttu-id="3a422-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3a422-121">**Attribute**</span></span>|<span data-ttu-id="3a422-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3a422-122">**Type**</span></span>|<span data-ttu-id="3a422-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="3a422-123">**Required**</span></span>|<span data-ttu-id="3a422-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a422-124">**Description**</span></span>|<span data-ttu-id="3a422-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3a422-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3a422-126">АссоЦиатедпаже</span><span class="sxs-lookup"><span data-stu-id="3a422-126">AssociatedPage</span></span>  <br/> |<span data-ttu-id="3a422-127">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="3a422-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3a422-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-128">optional</span></span>  <br/> ||<span data-ttu-id="3a422-129">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="3a422-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3a422-130">Фон</span><span class="sxs-lookup"><span data-stu-id="3a422-130">Background</span></span>  <br/> |<span data-ttu-id="3a422-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3a422-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3a422-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-132">optional</span></span>  <br/> ||<span data-ttu-id="3a422-133">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3a422-133">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3a422-134">BackPage</span><span class="sxs-lookup"><span data-stu-id="3a422-134">BackPage</span></span>  <br/> |<span data-ttu-id="3a422-135">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="3a422-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3a422-136">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-136">optional</span></span>  <br/> ||<span data-ttu-id="3a422-137">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="3a422-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3a422-138">ID</span><span class="sxs-lookup"><span data-stu-id="3a422-138">ID</span></span>  <br/> |<span data-ttu-id="3a422-139">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="3a422-139">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3a422-140">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-140">required</span></span>  <br/> ||<span data-ttu-id="3a422-141">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="3a422-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3a422-142">Искустомнаме</span><span class="sxs-lookup"><span data-stu-id="3a422-142">IsCustomName</span></span>  <br/> |<span data-ttu-id="3a422-143">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3a422-143">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3a422-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-144">optional</span></span>  <br/> ||<span data-ttu-id="3a422-145">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3a422-145">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3a422-146">Искустомнамеу</span><span class="sxs-lookup"><span data-stu-id="3a422-146">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="3a422-147">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="3a422-147">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3a422-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-148">optional</span></span>  <br/> ||<span data-ttu-id="3a422-149">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="3a422-149">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3a422-150">Имя</span><span class="sxs-lookup"><span data-stu-id="3a422-150">Name</span></span>  <br/> |<span data-ttu-id="3a422-151">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="3a422-151">xsd:string</span></span>  <br/> |<span data-ttu-id="3a422-152">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-152">optional</span></span>  <br/> ||<span data-ttu-id="3a422-153">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="3a422-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3a422-154">NameU</span><span class="sxs-lookup"><span data-stu-id="3a422-154">NameU</span></span>  <br/> |<span data-ttu-id="3a422-155">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="3a422-155">xsd:string</span></span>  <br/> |<span data-ttu-id="3a422-156">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-156">optional</span></span>  <br/> ||<span data-ttu-id="3a422-157">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="3a422-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3a422-158">ReviewerID</span><span class="sxs-lookup"><span data-stu-id="3a422-158">ReviewerID</span></span>  <br/> |<span data-ttu-id="3a422-159">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="3a422-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3a422-160">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-160">optional</span></span>  <br/> ||<span data-ttu-id="3a422-161">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="3a422-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3a422-162">Виевцентеркс</span><span class="sxs-lookup"><span data-stu-id="3a422-162">ViewCenterX</span></span>  <br/> |<span data-ttu-id="3a422-163">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="3a422-163">xsd:double</span></span>  <br/> |<span data-ttu-id="3a422-164">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-164">optional</span></span>  <br/> ||<span data-ttu-id="3a422-165">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3a422-165">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3a422-166">Виевцентери</span><span class="sxs-lookup"><span data-stu-id="3a422-166">ViewCenterY</span></span>  <br/> |<span data-ttu-id="3a422-167">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="3a422-167">xsd:double</span></span>  <br/> |<span data-ttu-id="3a422-168">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-168">optional</span></span>  <br/> ||<span data-ttu-id="3a422-169">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3a422-169">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="3a422-170">Виевскале</span><span class="sxs-lookup"><span data-stu-id="3a422-170">ViewScale</span></span>  <br/> |<span data-ttu-id="3a422-171">XSD: Double</span><span class="sxs-lookup"><span data-stu-id="3a422-171">xsd:double</span></span>  <br/> |<span data-ttu-id="3a422-172">необязательный</span><span class="sxs-lookup"><span data-stu-id="3a422-172">optional</span></span>  <br/> ||<span data-ttu-id="3a422-173">Значения типа XSD: Double.</span><span class="sxs-lookup"><span data-stu-id="3a422-173">Values of the xsd:double type.</span></span>  <br/> |
   

