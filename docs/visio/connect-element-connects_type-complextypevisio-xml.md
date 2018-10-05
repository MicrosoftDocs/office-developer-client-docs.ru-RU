---
title: Подключение элемента (Connects_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399321"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="ccadd-103">Подключение элемента (Connects_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ccadd-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ccadd-104">Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.</span><span class="sxs-lookup"><span data-stu-id="ccadd-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccadd-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ccadd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccadd-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ccadd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ccadd-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="ccadd-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ccadd-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ccadd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ccadd-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ccadd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ccadd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ccadd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ccadd-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ccadd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ccadd-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="ccadd-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ccadd-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ccadd-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ccadd-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ccadd-114">Elements and attributes</span></span>

<span data-ttu-id="ccadd-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ccadd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ccadd-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ccadd-116">Parent elements</span></span>

|<span data-ttu-id="ccadd-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ccadd-117">**Element**</span></span>|<span data-ttu-id="ccadd-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ccadd-118">**Type**</span></span>|<span data-ttu-id="ccadd-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ccadd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ccadd-120">Осуществляет подключение</span><span class="sxs-lookup"><span data-stu-id="ccadd-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ccadd-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="ccadd-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ccadd-122">Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="ccadd-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ccadd-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ccadd-123">Child elements</span></span>

<span data-ttu-id="ccadd-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="ccadd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccadd-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ccadd-125">Attributes</span></span>

|<span data-ttu-id="ccadd-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ccadd-126">**Attribute**</span></span>|<span data-ttu-id="ccadd-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ccadd-127">**Type**</span></span>|<span data-ttu-id="ccadd-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ccadd-128">**Required**</span></span>|<span data-ttu-id="ccadd-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ccadd-129">**Description**</span></span>|<span data-ttu-id="ccadd-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ccadd-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ccadd-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="ccadd-131">FromCell</span></span>  <br/> |<span data-ttu-id="ccadd-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ccadd-132">xsd:string</span></span>  <br/> |<span data-ttu-id="ccadd-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="ccadd-133">optional</span></span>  <br/> |<span data-ttu-id="ccadd-134">Ячейка, из которого создается подключение.</span><span class="sxs-lookup"><span data-stu-id="ccadd-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="ccadd-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ccadd-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ccadd-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="ccadd-136">FromPart</span></span>  <br/> |<span data-ttu-id="ccadd-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ccadd-137">xsd:int</span></span>  <br/> |<span data-ttu-id="ccadd-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ccadd-138">optional</span></span>  <br/> |<span data-ttu-id="ccadd-139">Часть фигуры, из которого создается подключение.</span><span class="sxs-lookup"><span data-stu-id="ccadd-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="ccadd-140">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="ccadd-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="ccadd-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="ccadd-141">FromSheet</span></span>  <br/> |<span data-ttu-id="ccadd-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ccadd-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ccadd-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ccadd-143">required</span></span>  <br/> |<span data-ttu-id="ccadd-144">Идентификатор фигуры, из которого создаются и подключения.</span><span class="sxs-lookup"><span data-stu-id="ccadd-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="ccadd-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ccadd-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ccadd-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="ccadd-146">ToCell</span></span>  <br/> |<span data-ttu-id="ccadd-147">XSD:String</span><span class="sxs-lookup"><span data-stu-id="ccadd-147">xsd:string</span></span>  <br/> |<span data-ttu-id="ccadd-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="ccadd-148">optional</span></span>  <br/> |<span data-ttu-id="ccadd-149">Ячейка, к которому выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="ccadd-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="ccadd-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ccadd-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ccadd-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="ccadd-151">ToPart</span></span>  <br/> |<span data-ttu-id="ccadd-152">XSD: int</span><span class="sxs-lookup"><span data-stu-id="ccadd-152">xsd:int</span></span>  <br/> |<span data-ttu-id="ccadd-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="ccadd-153">optional</span></span>  <br/> |<span data-ttu-id="ccadd-154">Часть фигуры, к которому выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="ccadd-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="ccadd-155">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="ccadd-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="ccadd-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="ccadd-156">ToSheet</span></span>  <br/> |<span data-ttu-id="ccadd-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ccadd-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ccadd-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ccadd-158">required</span></span>  <br/> |<span data-ttu-id="ccadd-159">Идентификатор фигуры, к которой один или несколько подключения.</span><span class="sxs-lookup"><span data-stu-id="ccadd-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="ccadd-160">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ccadd-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

