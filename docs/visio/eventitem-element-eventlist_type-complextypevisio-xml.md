---
title: Элемент EventItem (EventList_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Инкапсулирует код события.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394400"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="f987f-103">Элемент EventItem (EventList_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f987f-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f987f-104">Инкапсулирует код события.</span><span class="sxs-lookup"><span data-stu-id="f987f-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f987f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f987f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f987f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f987f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f987f-107">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="f987f-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f987f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f987f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f987f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f987f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f987f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f987f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f987f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f987f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f987f-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="f987f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f987f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f987f-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f987f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f987f-114">Elements and attributes</span></span>

<span data-ttu-id="f987f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f987f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f987f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f987f-116">Parent elements</span></span>

|<span data-ttu-id="f987f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f987f-117">**Element**</span></span>|<span data-ttu-id="f987f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f987f-118">**Type**</span></span>|<span data-ttu-id="f987f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f987f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f987f-120">EventList</span><span class="sxs-lookup"><span data-stu-id="f987f-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f987f-121">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="f987f-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f987f-122">Содержит элемент **EventItem** для каждого события, к которому должны отвечать объекта.</span><span class="sxs-lookup"><span data-stu-id="f987f-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f987f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f987f-123">Child elements</span></span>

<span data-ttu-id="f987f-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="f987f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f987f-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f987f-125">Attributes</span></span>

|<span data-ttu-id="f987f-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f987f-126">**Attribute**</span></span>|<span data-ttu-id="f987f-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f987f-127">**Type**</span></span>|<span data-ttu-id="f987f-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f987f-128">**Required**</span></span>|<span data-ttu-id="f987f-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f987f-129">**Description**</span></span>|<span data-ttu-id="f987f-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f987f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f987f-131">Действие</span><span class="sxs-lookup"><span data-stu-id="f987f-131">Action</span></span>  <br/> |<span data-ttu-id="f987f-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f987f-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f987f-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f987f-133">required</span></span>  <br/> |<span data-ttu-id="f987f-134">Указывает код действия **EventItem** родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="f987f-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="f987f-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f987f-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f987f-136">Включена</span><span class="sxs-lookup"><span data-stu-id="f987f-136">Enabled</span></span>  <br/> |<span data-ttu-id="f987f-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="f987f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f987f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="f987f-138">optional</span></span>  <br/> |<span data-ttu-id="f987f-139">Представляет флаг, указывающий, включен ли событие.</span><span class="sxs-lookup"><span data-stu-id="f987f-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="f987f-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="f987f-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f987f-141">EventCode</span><span class="sxs-lookup"><span data-stu-id="f987f-141">EventCode</span></span>  <br/> |<span data-ttu-id="f987f-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f987f-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f987f-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f987f-143">required</span></span>  <br/> |<span data-ttu-id="f987f-144">Код, указывающий событие, которое запускает надстройки.</span><span class="sxs-lookup"><span data-stu-id="f987f-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="f987f-145">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f987f-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f987f-146">ID</span><span class="sxs-lookup"><span data-stu-id="f987f-146">ID</span></span>  <br/> |<span data-ttu-id="f987f-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f987f-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f987f-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f987f-148">required</span></span>  <br/> |<span data-ttu-id="f987f-149">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="f987f-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="f987f-150">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f987f-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f987f-151">Целевой объект</span><span class="sxs-lookup"><span data-stu-id="f987f-151">Target</span></span>  <br/> |<span data-ttu-id="f987f-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f987f-152">xsd:string</span></span>  <br/> |<span data-ttu-id="f987f-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f987f-153">required</span></span>  <br/> |<span data-ttu-id="f987f-154">Указывает целевую события.</span><span class="sxs-lookup"><span data-stu-id="f987f-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="f987f-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f987f-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f987f-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="f987f-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="f987f-157">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f987f-157">xsd:string</span></span>  <br/> |<span data-ttu-id="f987f-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f987f-158">required</span></span>  <br/> |<span data-ttu-id="f987f-159">Задает строку, содержащую аргументы для отправки конечного события.</span><span class="sxs-lookup"><span data-stu-id="f987f-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="f987f-160">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f987f-160">Values of the xsd:string type.</span></span>  <br/> |
   

