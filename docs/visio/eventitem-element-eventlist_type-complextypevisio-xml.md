---
title: Элемент EventItem (EventList_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Инкапсулирует код события.
ms.openlocfilehash: 0db88a175d3e0330cb648f870559d9d2bd4dc1d8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541843"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a><span data-ttu-id="ca65e-103">Элемент EventItem (EventList_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ca65e-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ca65e-104">Инкапсулирует код события.</span><span class="sxs-lookup"><span data-stu-id="ca65e-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ca65e-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ca65e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ca65e-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ca65e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ca65e-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="ca65e-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ca65e-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ca65e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ca65e-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ca65e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ca65e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ca65e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ca65e-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="ca65e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ca65e-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="ca65e-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ca65e-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ca65e-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ca65e-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca65e-114">Elements and attributes</span></span>

<span data-ttu-id="ca65e-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ca65e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ca65e-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ca65e-116">Parent elements</span></span>

|<span data-ttu-id="ca65e-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ca65e-117">**Element**</span></span>|<span data-ttu-id="ca65e-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca65e-118">**Type**</span></span>|<span data-ttu-id="ca65e-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca65e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ca65e-120">EventList</span><span class="sxs-lookup"><span data-stu-id="ca65e-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ca65e-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="ca65e-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ca65e-122">Содержит элемент **EventItem** для каждого события, на которое должен отвечать объект.</span><span class="sxs-lookup"><span data-stu-id="ca65e-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ca65e-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ca65e-123">Child elements</span></span>

<span data-ttu-id="ca65e-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="ca65e-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ca65e-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ca65e-125">Attributes</span></span>

|<span data-ttu-id="ca65e-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ca65e-126">**Attribute**</span></span>|<span data-ttu-id="ca65e-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ca65e-127">**Type**</span></span>|<span data-ttu-id="ca65e-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ca65e-128">**Required**</span></span>|<span data-ttu-id="ca65e-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ca65e-129">**Description**</span></span>|<span data-ttu-id="ca65e-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ca65e-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ca65e-131">Action</span><span class="sxs-lookup"><span data-stu-id="ca65e-131">Action</span></span>  <br/> |<span data-ttu-id="ca65e-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ca65e-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ca65e-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca65e-133">required</span></span>  <br/> |<span data-ttu-id="ca65e-134">Указывает код действия родительского **элемента EventItem.**</span><span class="sxs-lookup"><span data-stu-id="ca65e-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="ca65e-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ca65e-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ca65e-136">Включено</span><span class="sxs-lookup"><span data-stu-id="ca65e-136">Enabled</span></span>  <br/> |<span data-ttu-id="ca65e-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="ca65e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="ca65e-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="ca65e-138">optional</span></span>  <br/> |<span data-ttu-id="ca65e-139">Представляет флаг, указывающий, включено или отключено событие.</span><span class="sxs-lookup"><span data-stu-id="ca65e-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="ca65e-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="ca65e-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="ca65e-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="ca65e-141">EventCode</span></span>  <br/> |<span data-ttu-id="ca65e-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="ca65e-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="ca65e-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca65e-143">required</span></span>  <br/> |<span data-ttu-id="ca65e-144">Код, указывающий событие, запускающее надстройки.</span><span class="sxs-lookup"><span data-stu-id="ca65e-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="ca65e-145">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="ca65e-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="ca65e-146">ID</span><span class="sxs-lookup"><span data-stu-id="ca65e-146">ID</span></span>  <br/> |<span data-ttu-id="ca65e-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ca65e-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ca65e-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca65e-148">required</span></span>  <br/> |<span data-ttu-id="ca65e-149">ID события.</span><span class="sxs-lookup"><span data-stu-id="ca65e-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="ca65e-150">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ca65e-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ca65e-151">Target</span><span class="sxs-lookup"><span data-stu-id="ca65e-151">Target</span></span>  <br/> |<span data-ttu-id="ca65e-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca65e-152">xsd:string</span></span>  <br/> |<span data-ttu-id="ca65e-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca65e-153">required</span></span>  <br/> |<span data-ttu-id="ca65e-154">Указывает цель события.</span><span class="sxs-lookup"><span data-stu-id="ca65e-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="ca65e-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ca65e-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ca65e-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="ca65e-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="ca65e-157">xsd:string</span><span class="sxs-lookup"><span data-stu-id="ca65e-157">xsd:string</span></span>  <br/> |<span data-ttu-id="ca65e-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ca65e-158">required</span></span>  <br/> |<span data-ttu-id="ca65e-159">Указывает строку, содержащую аргументы, которые будут отправлены в целевой объект события.</span><span class="sxs-lookup"><span data-stu-id="ca65e-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="ca65e-160">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="ca65e-160">Values of the xsd:string type.</span></span>  <br/> |
   

