---
title: Элемент Евентитем (Евентлист_типе complexType) (XML для Visio)
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
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="fc1db-103">Элемент Евентитем (Евентлист_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="fc1db-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fc1db-104">Инкапсулирует код события.</span><span class="sxs-lookup"><span data-stu-id="fc1db-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc1db-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fc1db-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc1db-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="fc1db-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fc1db-107">Евентитем_типе</span><span class="sxs-lookup"><span data-stu-id="fc1db-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fc1db-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fc1db-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fc1db-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fc1db-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fc1db-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fc1db-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fc1db-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="fc1db-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fc1db-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="fc1db-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fc1db-113">Определение</span><span class="sxs-lookup"><span data-stu-id="fc1db-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fc1db-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fc1db-114">Elements and attributes</span></span>

<span data-ttu-id="fc1db-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="fc1db-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fc1db-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fc1db-116">Parent elements</span></span>

|<span data-ttu-id="fc1db-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fc1db-117">**Element**</span></span>|<span data-ttu-id="fc1db-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fc1db-118">**Type**</span></span>|<span data-ttu-id="fc1db-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc1db-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fc1db-120">EventList</span><span class="sxs-lookup"><span data-stu-id="fc1db-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fc1db-121">Евентлист_типе</span><span class="sxs-lookup"><span data-stu-id="fc1db-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fc1db-122">Содержит элемент **евентитем** для каждого события, на которое должен отвечать объект.</span><span class="sxs-lookup"><span data-stu-id="fc1db-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fc1db-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fc1db-123">Child elements</span></span>

<span data-ttu-id="fc1db-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="fc1db-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc1db-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fc1db-125">Attributes</span></span>

|<span data-ttu-id="fc1db-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fc1db-126">**Attribute**</span></span>|<span data-ttu-id="fc1db-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fc1db-127">**Type**</span></span>|<span data-ttu-id="fc1db-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="fc1db-128">**Required**</span></span>|<span data-ttu-id="fc1db-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc1db-129">**Description**</span></span>|<span data-ttu-id="fc1db-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fc1db-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fc1db-131">Action</span><span class="sxs-lookup"><span data-stu-id="fc1db-131">Action</span></span>  <br/> |<span data-ttu-id="fc1db-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fc1db-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fc1db-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fc1db-133">required</span></span>  <br/> |<span data-ttu-id="fc1db-134">Задает код действия родительского элемента **евентитем** .</span><span class="sxs-lookup"><span data-stu-id="fc1db-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="fc1db-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fc1db-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fc1db-136">Включен</span><span class="sxs-lookup"><span data-stu-id="fc1db-136">Enabled</span></span>  <br/> |<span data-ttu-id="fc1db-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="fc1db-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fc1db-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="fc1db-138">optional</span></span>  <br/> |<span data-ttu-id="fc1db-139">Представляет флаг, указывающий, включено или отключено событие.</span><span class="sxs-lookup"><span data-stu-id="fc1db-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="fc1db-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="fc1db-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="fc1db-141">Евенткоде</span><span class="sxs-lookup"><span data-stu-id="fc1db-141">EventCode</span></span>  <br/> |<span data-ttu-id="fc1db-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fc1db-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fc1db-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fc1db-143">required</span></span>  <br/> |<span data-ttu-id="fc1db-144">Код, указывающий на событие, которое запускает надстройку.</span><span class="sxs-lookup"><span data-stu-id="fc1db-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="fc1db-145">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fc1db-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fc1db-146">ID</span><span class="sxs-lookup"><span data-stu-id="fc1db-146">ID</span></span>  <br/> |<span data-ttu-id="fc1db-147">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="fc1db-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fc1db-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fc1db-148">required</span></span>  <br/> |<span data-ttu-id="fc1db-149">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="fc1db-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="fc1db-150">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="fc1db-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fc1db-151">Target</span><span class="sxs-lookup"><span data-stu-id="fc1db-151">Target</span></span>  <br/> |<span data-ttu-id="fc1db-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="fc1db-152">xsd:string</span></span>  <br/> |<span data-ttu-id="fc1db-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fc1db-153">required</span></span>  <br/> |<span data-ttu-id="fc1db-154">Указывает целевой объект события.</span><span class="sxs-lookup"><span data-stu-id="fc1db-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="fc1db-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="fc1db-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="fc1db-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="fc1db-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="fc1db-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="fc1db-157">xsd:string</span></span>  <br/> |<span data-ttu-id="fc1db-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fc1db-158">required</span></span>  <br/> |<span data-ttu-id="fc1db-159">Указывает строку, содержащую аргументы, которые необходимо отправить в цель события.</span><span class="sxs-lookup"><span data-stu-id="fc1db-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="fc1db-160">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="fc1db-160">Values of the xsd:string type.</span></span>  <br/> |
   

