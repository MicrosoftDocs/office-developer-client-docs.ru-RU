---
title: Элемент Евентитем (Евентлист_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Инкапсулирует код события.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337200"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a><span data-ttu-id="bdb08-103">Элемент Евентитем (Евентлист_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="bdb08-103">EventItem element (EventList_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="bdb08-104">Инкапсулирует код события.</span><span class="sxs-lookup"><span data-stu-id="bdb08-104">Encapsulates an event code.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bdb08-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bdb08-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bdb08-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="bdb08-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bdb08-107">Евентитем_типе</span><span class="sxs-lookup"><span data-stu-id="bdb08-107">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bdb08-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bdb08-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bdb08-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bdb08-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bdb08-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="bdb08-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bdb08-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="bdb08-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bdb08-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="bdb08-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bdb08-113">Определение</span><span class="sxs-lookup"><span data-stu-id="bdb08-113">Definition</span></span>

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bdb08-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bdb08-114">Elements and attributes</span></span>

<span data-ttu-id="bdb08-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="bdb08-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bdb08-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bdb08-116">Parent elements</span></span>

|<span data-ttu-id="bdb08-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bdb08-117">**Element**</span></span>|<span data-ttu-id="bdb08-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bdb08-118">**Type**</span></span>|<span data-ttu-id="bdb08-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bdb08-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bdb08-120">EventList</span><span class="sxs-lookup"><span data-stu-id="bdb08-120">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bdb08-121">Евентлист_типе</span><span class="sxs-lookup"><span data-stu-id="bdb08-121">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bdb08-122">Содержит элемент **евентитем** для каждого события, на которое должен отвечать объект.</span><span class="sxs-lookup"><span data-stu-id="bdb08-122">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bdb08-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bdb08-123">Child elements</span></span>

<span data-ttu-id="bdb08-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="bdb08-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bdb08-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bdb08-125">Attributes</span></span>

|<span data-ttu-id="bdb08-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="bdb08-126">**Attribute**</span></span>|<span data-ttu-id="bdb08-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bdb08-127">**Type**</span></span>|<span data-ttu-id="bdb08-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="bdb08-128">**Required**</span></span>|<span data-ttu-id="bdb08-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bdb08-129">**Description**</span></span>|<span data-ttu-id="bdb08-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="bdb08-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bdb08-131">Действие</span><span class="sxs-lookup"><span data-stu-id="bdb08-131">Action</span></span>  <br/> |<span data-ttu-id="bdb08-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdb08-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdb08-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bdb08-133">required</span></span>  <br/> |<span data-ttu-id="bdb08-134">Задает код действия родительского элемента **евентитем** .</span><span class="sxs-lookup"><span data-stu-id="bdb08-134">Specifies the action code of the parent **EventItem** element.</span></span>  <br/> |<span data-ttu-id="bdb08-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdb08-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdb08-136">Включена</span><span class="sxs-lookup"><span data-stu-id="bdb08-136">Enabled</span></span>  <br/> |<span data-ttu-id="bdb08-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="bdb08-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bdb08-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="bdb08-138">optional</span></span>  <br/> |<span data-ttu-id="bdb08-139">Представляет флаг, указывающий, включено или отключено событие.</span><span class="sxs-lookup"><span data-stu-id="bdb08-139">Represents a flag indicating if the event is enabled or disabled.</span></span>  <br/> |<span data-ttu-id="bdb08-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="bdb08-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="bdb08-141">Евенткоде</span><span class="sxs-lookup"><span data-stu-id="bdb08-141">EventCode</span></span>  <br/> |<span data-ttu-id="bdb08-142">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="bdb08-142">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="bdb08-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bdb08-143">required</span></span>  <br/> |<span data-ttu-id="bdb08-144">Код, указывающий на событие, которое запускает надстройку.</span><span class="sxs-lookup"><span data-stu-id="bdb08-144">A code indicating the event that triggers the add-on.</span></span>  <br/> |<span data-ttu-id="bdb08-145">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="bdb08-145">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="bdb08-146">ИД</span><span class="sxs-lookup"><span data-stu-id="bdb08-146">ID</span></span>  <br/> |<span data-ttu-id="bdb08-147">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="bdb08-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bdb08-148">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bdb08-148">required</span></span>  <br/> |<span data-ttu-id="bdb08-149">Идентификатор события.</span><span class="sxs-lookup"><span data-stu-id="bdb08-149">The ID of the event.</span></span>  <br/> |<span data-ttu-id="bdb08-150">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="bdb08-150">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bdb08-151">Target</span><span class="sxs-lookup"><span data-stu-id="bdb08-151">Target</span></span>  <br/> |<span data-ttu-id="bdb08-152">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="bdb08-152">xsd:string</span></span>  <br/> |<span data-ttu-id="bdb08-153">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bdb08-153">required</span></span>  <br/> |<span data-ttu-id="bdb08-154">Указывает целевой объект события.</span><span class="sxs-lookup"><span data-stu-id="bdb08-154">Specifies the target of an event.</span></span>  <br/> |<span data-ttu-id="bdb08-155">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="bdb08-155">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bdb08-156">TargetArgs</span><span class="sxs-lookup"><span data-stu-id="bdb08-156">TargetArgs</span></span>  <br/> |<span data-ttu-id="bdb08-157">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="bdb08-157">xsd:string</span></span>  <br/> |<span data-ttu-id="bdb08-158">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bdb08-158">required</span></span>  <br/> |<span data-ttu-id="bdb08-159">Указывает строку, содержащую аргументы, которые необходимо отправить в цель события.</span><span class="sxs-lookup"><span data-stu-id="bdb08-159">Specifies a string containing arguments to be sent to the target of an event.</span></span>  <br/> |<span data-ttu-id="bdb08-160">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="bdb08-160">Values of the xsd:string type.</span></span>  <br/> |
   

