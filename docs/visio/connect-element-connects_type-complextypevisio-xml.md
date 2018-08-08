---
title: Подключение элемента (Connects_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.
ms.openlocfilehash: 1bd3e1f006afe8d5bbb698e0b3a2179b74728315
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813467"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="6e7cc-103">Подключение элемента (Connects_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="6e7cc-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="6e7cc-104">Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e7cc-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6e7cc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e7cc-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6e7cc-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="6e7cc-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6e7cc-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6e7cc-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6e7cc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="6e7cc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6e7cc-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6e7cc-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="6e7cc-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e7cc-113">Определение</span><span class="sxs-lookup"><span data-stu-id="6e7cc-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6e7cc-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e7cc-114">Elements and attributes</span></span>

<span data-ttu-id="6e7cc-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6e7cc-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6e7cc-116">Parent elements</span></span>

|<span data-ttu-id="6e7cc-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-117">**Element**</span></span>|<span data-ttu-id="6e7cc-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-118">**Type**</span></span>|<span data-ttu-id="6e7cc-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e7cc-120">Осуществляет подключение</span><span class="sxs-lookup"><span data-stu-id="6e7cc-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e7cc-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="6e7cc-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e7cc-122">Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6e7cc-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6e7cc-123">Child elements</span></span>

<span data-ttu-id="6e7cc-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e7cc-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e7cc-125">Attributes</span></span>

|<span data-ttu-id="6e7cc-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-126">**Attribute**</span></span>|<span data-ttu-id="6e7cc-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-127">**Type**</span></span>|<span data-ttu-id="6e7cc-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-128">**Required**</span></span>|<span data-ttu-id="6e7cc-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-129">**Description**</span></span>|<span data-ttu-id="6e7cc-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6e7cc-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6e7cc-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="6e7cc-131">FromCell</span></span>  <br/> |<span data-ttu-id="6e7cc-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="6e7cc-132">xsd:string</span></span>  <br/> |<span data-ttu-id="6e7cc-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="6e7cc-133">optional</span></span>  <br/> |<span data-ttu-id="6e7cc-134">Ячейка, из которого создается подключение.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="6e7cc-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6e7cc-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="6e7cc-136">FromPart</span></span>  <br/> |<span data-ttu-id="6e7cc-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="6e7cc-137">xsd:int</span></span>  <br/> |<span data-ttu-id="6e7cc-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="6e7cc-138">optional</span></span>  <br/> |<span data-ttu-id="6e7cc-139">Часть фигуры, из которого создается подключение.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="6e7cc-140">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="6e7cc-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="6e7cc-141">FromSheet</span></span>  <br/> |<span data-ttu-id="6e7cc-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6e7cc-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6e7cc-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6e7cc-143">required</span></span>  <br/> |<span data-ttu-id="6e7cc-144">Идентификатор фигуры, из которого создаются и подключения.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="6e7cc-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6e7cc-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="6e7cc-146">ToCell</span></span>  <br/> |<span data-ttu-id="6e7cc-147">XSD:String</span><span class="sxs-lookup"><span data-stu-id="6e7cc-147">xsd:string</span></span>  <br/> |<span data-ttu-id="6e7cc-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="6e7cc-148">optional</span></span>  <br/> |<span data-ttu-id="6e7cc-149">Ячейка, к которому выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="6e7cc-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6e7cc-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="6e7cc-151">ToPart</span></span>  <br/> |<span data-ttu-id="6e7cc-152">XSD: int</span><span class="sxs-lookup"><span data-stu-id="6e7cc-152">xsd:int</span></span>  <br/> |<span data-ttu-id="6e7cc-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="6e7cc-153">optional</span></span>  <br/> |<span data-ttu-id="6e7cc-154">Часть фигуры, к которому выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="6e7cc-155">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="6e7cc-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="6e7cc-156">ToSheet</span></span>  <br/> |<span data-ttu-id="6e7cc-157">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6e7cc-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6e7cc-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6e7cc-158">required</span></span>  <br/> |<span data-ttu-id="6e7cc-159">Идентификатор фигуры, к которой один или несколько подключения.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="6e7cc-160">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6e7cc-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

