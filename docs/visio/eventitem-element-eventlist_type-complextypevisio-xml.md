---
title: Элемент Евентитем (EventList_Type complexType) (XML для Visio)
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
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a><span data-ttu-id="96916-103">Элемент Евентитем (EventList_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="96916-103">EventItem element (EventList_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="96916-104">Инкапсулирует код события.</span><span class="sxs-lookup"><span data-stu-id="96916-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="96916-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="96916-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96916-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="96916-106">**Element type**</span></span> <br/> |[<span data-ttu-id="96916-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="96916-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="96916-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="96916-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="96916-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="96916-109">**Schema file**</span></span> <br/> |<span data-ttu-id="96916-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="96916-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="96916-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="96916-111">**Document parts**</span></span> <br/> |<span data-ttu-id="96916-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="96916-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="96916-113">Определение</span><span class="sxs-lookup"><span data-stu-id="96916-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="96916-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="96916-114">Elements and attributes</span></span>

<span data-ttu-id="96916-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="96916-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="96916-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="96916-116">Parent elements</span></span>

|<span data-ttu-id="96916-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="96916-117">**Element**</span></span>|<span data-ttu-id="96916-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="96916-118">**Type**</span></span>|<span data-ttu-id="96916-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96916-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="96916-120">EventList</span><span class="sxs-lookup"><span data-stu-id="96916-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="96916-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="96916-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="96916-122">Содержит элемент **евентитем** для каждого события, на которое должен отвечать объект.</span><span class="sxs-lookup"><span data-stu-id="96916-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="96916-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="96916-123">Child elements</span></span>

<span data-ttu-id="96916-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="96916-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="96916-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="96916-125">Attributes</span></span>

|<span data-ttu-id="96916-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="96916-126">**Attribute**</span></span>|<span data-ttu-id="96916-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="96916-127">**Type**</span></span>|<span data-ttu-id="96916-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="96916-128">**Required**</span></span>|<span data-ttu-id="96916-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="96916-129">**Description**</span></span>|<span data-ttu-id="96916-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="96916-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="96916-131">Action</span><span class="sxs-lookup"><span data-stu-id="96916-131">Action</span></span>  <br/> |<span data-ttu-id="96916-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="96916-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="96916-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96916-133">required</span></span>  <br/> |<span data-ttu-id="96916-134">Задает код действия родительского элемента **евентитем** .</span><span class="sxs-lookup"><span data-stu-id="96916-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="96916-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="96916-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="96916-136">Включен</span><span class="sxs-lookup"><span data-stu-id="96916-136">Enabled</span></span>  <br/> |<span data-ttu-id="96916-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="96916-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="96916-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="96916-138">optional</span></span>  <br/> |<span data-ttu-id="96916-139">Представляет флаг, указывающий, включено или отключено событие.</span><span class="sxs-lookup"><span data-stu-id="96916-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="96916-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="96916-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="96916-141">евенткоде</span><span class="sxs-lookup"><span data-stu-id="96916-141">EventCode</span></span>  <br/> |<span data-ttu-id="96916-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="96916-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="96916-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96916-143">required</span></span>  <br/> |<span data-ttu-id="96916-144">Код, указывающий на событие, которое запускает надстройку.</span><span class="sxs-lookup"><span data-stu-id="96916-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="96916-145">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="96916-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="96916-146">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="96916-146">ID</span></span>  <br/> |<span data-ttu-id="96916-147">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="96916-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="96916-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96916-148">required</span></span>  <br/> |<span data-ttu-id="96916-149">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="96916-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="96916-150">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="96916-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="96916-151">Target</span><span class="sxs-lookup"><span data-stu-id="96916-151">Target</span></span>  <br/> |<span data-ttu-id="96916-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="96916-152">xsd:string</span></span>  <br/> |<span data-ttu-id="96916-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96916-153">required</span></span>  <br/> |<span data-ttu-id="96916-154">Указывает целевой объект события.</span><span class="sxs-lookup"><span data-stu-id="96916-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="96916-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="96916-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="96916-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="96916-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="96916-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="96916-157">xsd:string</span></span>  <br/> |<span data-ttu-id="96916-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="96916-158">required</span></span>  <br/> |<span data-ttu-id="96916-159">Указывает строку, содержащую аргументы, которые необходимо отправить в цель события.</span><span class="sxs-lookup"><span data-stu-id="96916-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="96916-160">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="96916-160">Values of the xsd:string type.</span></span>  <br/> |
   

