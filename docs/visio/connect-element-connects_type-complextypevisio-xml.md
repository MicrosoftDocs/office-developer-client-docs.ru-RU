---
title: Элемент Connect (Connects_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Представляет соединение между двумя фигурами в рисунке, например строкой и полем в диаграмме организации.
ms.openlocfilehash: 3450a07e042fc633b9cd4952d9b3ad6b8190ed1e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541997"
---
# <a name="connect-element-connects_type-complextype-visio-xml"></a><span data-ttu-id="4b822-103">Элемент Connect (Connects_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4b822-103">Connect element (Connects_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4b822-104">Представляет соединение между двумя фигурами в рисунке, например строкой и полем в диаграмме организации.</span><span class="sxs-lookup"><span data-stu-id="4b822-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4b822-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4b822-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b822-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4b822-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4b822-107">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="4b822-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4b822-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4b822-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4b822-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4b822-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4b822-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4b822-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4b822-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4b822-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4b822-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="4b822-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b822-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4b822-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4b822-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4b822-114">Elements and attributes</span></span>

<span data-ttu-id="4b822-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4b822-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4b822-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4b822-116">Parent elements</span></span>

|<span data-ttu-id="4b822-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4b822-117">**Element**</span></span>|<span data-ttu-id="4b822-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4b822-118">**Type**</span></span>|<span data-ttu-id="4b822-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b822-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b822-120">Connects</span><span class="sxs-lookup"><span data-stu-id="4b822-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b822-121">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="4b822-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b822-122">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="4b822-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4b822-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4b822-123">Child elements</span></span>

<span data-ttu-id="4b822-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="4b822-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4b822-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4b822-125">Attributes</span></span>

|<span data-ttu-id="4b822-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4b822-126">**Attribute**</span></span>|<span data-ttu-id="4b822-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4b822-127">**Type**</span></span>|<span data-ttu-id="4b822-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4b822-128">**Required**</span></span>|<span data-ttu-id="4b822-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b822-129">**Description**</span></span>|<span data-ttu-id="4b822-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4b822-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b822-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="4b822-131">FromCell</span></span>  <br/> |<span data-ttu-id="4b822-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4b822-132">xsd:string</span></span>  <br/> |<span data-ttu-id="4b822-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b822-133">optional</span></span>  <br/> |<span data-ttu-id="4b822-134">Ячейка, из которой происходит подключение.</span><span class="sxs-lookup"><span data-stu-id="4b822-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="4b822-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4b822-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b822-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="4b822-136">FromPart</span></span>  <br/> |<span data-ttu-id="4b822-137">xsd:int</span><span class="sxs-lookup"><span data-stu-id="4b822-137">xsd:int</span></span>  <br/> |<span data-ttu-id="4b822-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b822-138">optional</span></span>  <br/> |<span data-ttu-id="4b822-139">Часть фигуры, из которой происходит подключение.</span><span class="sxs-lookup"><span data-stu-id="4b822-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="4b822-140">Значения типа xsd:int.</span><span class="sxs-lookup"><span data-stu-id="4b822-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="4b822-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="4b822-141">FromSheet</span></span>  <br/> |<span data-ttu-id="4b822-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b822-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b822-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4b822-143">required</span></span>  <br/> |<span data-ttu-id="4b822-144">ИД фигуры, из которой происходит подключение или подключение.</span><span class="sxs-lookup"><span data-stu-id="4b822-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="4b822-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b822-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="4b822-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="4b822-146">ToCell</span></span>  <br/> |<span data-ttu-id="4b822-147">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4b822-147">xsd:string</span></span>  <br/> |<span data-ttu-id="4b822-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b822-148">optional</span></span>  <br/> |<span data-ttu-id="4b822-149">Ячейка, к которой выполнено подключение.</span><span class="sxs-lookup"><span data-stu-id="4b822-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="4b822-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4b822-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4b822-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="4b822-151">ToPart</span></span>  <br/> |<span data-ttu-id="4b822-152">xsd:int</span><span class="sxs-lookup"><span data-stu-id="4b822-152">xsd:int</span></span>  <br/> |<span data-ttu-id="4b822-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="4b822-153">optional</span></span>  <br/> |<span data-ttu-id="4b822-154">Часть фигуры, к которой выполнено подключение.</span><span class="sxs-lookup"><span data-stu-id="4b822-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="4b822-155">Значения типа xsd:Int.</span><span class="sxs-lookup"><span data-stu-id="4b822-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="4b822-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="4b822-156">ToSheet</span></span>  <br/> |<span data-ttu-id="4b822-157">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4b822-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4b822-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4b822-158">required</span></span>  <br/> |<span data-ttu-id="4b822-159">ИД фигуры, к которой выполнено одно или несколько подключений.</span><span class="sxs-lookup"><span data-stu-id="4b822-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="4b822-160">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4b822-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

