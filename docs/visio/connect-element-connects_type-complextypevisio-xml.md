---
title: Элемент Connect (Коннектс_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e1ad47b-ee28-6b9a-f2f9-642e09ca28d4
description: Представляет соединение между двумя фигурами в документе, например линии и поле на организационной диаграмме.
ms.openlocfilehash: 82413f44f05f2ec6140e2b3981b7a1e8435becb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346510"
---
# <a name="connect-element-connectstype-complextype-visio-xml"></a><span data-ttu-id="0dff3-103">Элемент Connect (Коннектс_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="0dff3-103">Connect element (Connects_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="0dff3-104">Представляет соединение между двумя фигурами в документе, например линии и поле на организационной диаграмме.</span><span class="sxs-lookup"><span data-stu-id="0dff3-104">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0dff3-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0dff3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0dff3-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="0dff3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="0dff3-107">Коннект_типе</span><span class="sxs-lookup"><span data-stu-id="0dff3-107">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="0dff3-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0dff3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="0dff3-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0dff3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="0dff3-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="0dff3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="0dff3-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="0dff3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="0dff3-112">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="0dff3-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0dff3-113">Определение</span><span class="sxs-lookup"><span data-stu-id="0dff3-113">Definition</span></span>

```XML
< xs:element name="Connect" type="Connect_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0dff3-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0dff3-114">Elements and attributes</span></span>

<span data-ttu-id="0dff3-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0dff3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="0dff3-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0dff3-116">Parent elements</span></span>

|<span data-ttu-id="0dff3-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0dff3-117">**Element**</span></span>|<span data-ttu-id="0dff3-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0dff3-118">**Type**</span></span>|<span data-ttu-id="0dff3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0dff3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0dff3-120">Connects</span><span class="sxs-lookup"><span data-stu-id="0dff3-120">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0dff3-121">Коннектс_типе</span><span class="sxs-lookup"><span data-stu-id="0dff3-121">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="0dff3-122">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="0dff3-122">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="0dff3-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0dff3-123">Child elements</span></span>

<span data-ttu-id="0dff3-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="0dff3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0dff3-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0dff3-125">Attributes</span></span>

|<span data-ttu-id="0dff3-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="0dff3-126">**Attribute**</span></span>|<span data-ttu-id="0dff3-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0dff3-127">**Type**</span></span>|<span data-ttu-id="0dff3-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="0dff3-128">**Required**</span></span>|<span data-ttu-id="0dff3-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0dff3-129">**Description**</span></span>|<span data-ttu-id="0dff3-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="0dff3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0dff3-131">FromCell</span><span class="sxs-lookup"><span data-stu-id="0dff3-131">FromCell</span></span>  <br/> |<span data-ttu-id="0dff3-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0dff3-132">xsd:string</span></span>  <br/> |<span data-ttu-id="0dff3-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="0dff3-133">optional</span></span>  <br/> |<span data-ttu-id="0dff3-134">Ячейка, из которой исходит подключение.</span><span class="sxs-lookup"><span data-stu-id="0dff3-134">The cell from which a connection originates.</span></span>  <br/> |<span data-ttu-id="0dff3-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0dff3-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0dff3-136">FromPart</span><span class="sxs-lookup"><span data-stu-id="0dff3-136">FromPart</span></span>  <br/> |<span data-ttu-id="0dff3-137">XSD: int</span><span class="sxs-lookup"><span data-stu-id="0dff3-137">xsd:int</span></span>  <br/> |<span data-ttu-id="0dff3-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="0dff3-138">optional</span></span>  <br/> |<span data-ttu-id="0dff3-139">Часть фигуры, из которой происходит подключение.</span><span class="sxs-lookup"><span data-stu-id="0dff3-139">The part of a shape from which a connection originates.</span></span>  <br/> |<span data-ttu-id="0dff3-140">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="0dff3-140">Values of the xsd:int type.</span></span>  <br/> |
|<span data-ttu-id="0dff3-141">FromSheet</span><span class="sxs-lookup"><span data-stu-id="0dff3-141">FromSheet</span></span>  <br/> |<span data-ttu-id="0dff3-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0dff3-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0dff3-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0dff3-143">required</span></span>  <br/> |<span data-ttu-id="0dff3-144">ИДЕНТИФИКАТОР фигуры, из которой происходят подключения.</span><span class="sxs-lookup"><span data-stu-id="0dff3-144">The ID of the shape from which a connection or connections originate.</span></span>  <br/> |<span data-ttu-id="0dff3-145">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0dff3-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="0dff3-146">ToCell</span><span class="sxs-lookup"><span data-stu-id="0dff3-146">ToCell</span></span>  <br/> |<span data-ttu-id="0dff3-147">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="0dff3-147">xsd:string</span></span>  <br/> |<span data-ttu-id="0dff3-148">необязательный</span><span class="sxs-lookup"><span data-stu-id="0dff3-148">optional</span></span>  <br/> |<span data-ttu-id="0dff3-149">Ячейка, к которой выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="0dff3-149">The cell to which a connection is made.</span></span>  <br/> |<span data-ttu-id="0dff3-150">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="0dff3-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0dff3-151">ToPart</span><span class="sxs-lookup"><span data-stu-id="0dff3-151">ToPart</span></span>  <br/> |<span data-ttu-id="0dff3-152">XSD: int</span><span class="sxs-lookup"><span data-stu-id="0dff3-152">xsd:int</span></span>  <br/> |<span data-ttu-id="0dff3-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="0dff3-153">optional</span></span>  <br/> |<span data-ttu-id="0dff3-154">Часть фигуры, к которой выполняется подключение.</span><span class="sxs-lookup"><span data-stu-id="0dff3-154">The part of a shape to which a connection is made.</span></span>  <br/> |<span data-ttu-id="0dff3-155">Значения типа XSD: int.</span><span class="sxs-lookup"><span data-stu-id="0dff3-155">Values of the xsd:Int type.</span></span>  <br/> |
|<span data-ttu-id="0dff3-156">ToSheet</span><span class="sxs-lookup"><span data-stu-id="0dff3-156">ToSheet</span></span>  <br/> |<span data-ttu-id="0dff3-157">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="0dff3-157">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0dff3-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="0dff3-158">required</span></span>  <br/> |<span data-ttu-id="0dff3-159">ИДЕНТИФИКАТОР фигуры, для которой выполняется одно или несколько подключений.</span><span class="sxs-lookup"><span data-stu-id="0dff3-159">The ID of the shape to which one or more connections are made.</span></span>  <br/> |<span data-ttu-id="0dff3-160">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="0dff3-160">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

