---
title: Элемент RefBy (Trigger_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Задает ссылку на страницу в документе.
ms.openlocfilehash: 57ac63c4488b68d3af3c6e4a75417e2c7937723c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814537"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="b2038-103">Элемент RefBy (Trigger_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b2038-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b2038-104">Задает ссылку на страницу в документе.</span><span class="sxs-lookup"><span data-stu-id="b2038-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2038-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b2038-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2038-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b2038-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b2038-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="b2038-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b2038-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b2038-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b2038-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b2038-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b2038-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b2038-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b2038-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b2038-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="b2038-112">Определение</span><span class="sxs-lookup"><span data-stu-id="b2038-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b2038-113">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b2038-113">Elements and attributes</span></span>

<span data-ttu-id="b2038-114">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="b2038-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b2038-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b2038-115">Parent elements</span></span>

|<span data-ttu-id="b2038-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b2038-116">**Element**</span></span>|<span data-ttu-id="b2038-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b2038-117">**Type**</span></span>|<span data-ttu-id="b2038-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b2038-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2038-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="b2038-119">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="b2038-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="b2038-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2038-121">Инструкции для Microsoft Visio для пересчета отношение между частями документа в файл Visio.</span><span class="sxs-lookup"><span data-stu-id="b2038-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="b2038-122">Trigger</span><span class="sxs-lookup"><span data-stu-id="b2038-122">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="b2038-123">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="b2038-123">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2038-124">Инструкции для Microsoft Visio для пересчета отношение между частями документа в файл Visio.</span><span class="sxs-lookup"><span data-stu-id="b2038-124">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
|[<span data-ttu-id="b2038-125">Trigger</span><span class="sxs-lookup"><span data-stu-id="b2038-125">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="b2038-126">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="b2038-126">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2038-127">Инструкции для Microsoft Visio для пересчета отношение между частями документа в файл Visio.</span><span class="sxs-lookup"><span data-stu-id="b2038-127">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b2038-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b2038-128">Child elements</span></span>

<span data-ttu-id="b2038-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="b2038-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2038-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b2038-130">Attributes</span></span>

|<span data-ttu-id="b2038-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b2038-131">**Attribute**</span></span>|<span data-ttu-id="b2038-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b2038-132">**Type**</span></span>|<span data-ttu-id="b2038-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="b2038-133">**Required**</span></span>|<span data-ttu-id="b2038-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b2038-134">**Description**</span></span>|<span data-ttu-id="b2038-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b2038-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b2038-136">ID</span><span class="sxs-lookup"><span data-stu-id="b2038-136">ID</span></span>  <br/> |<span data-ttu-id="b2038-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2038-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2038-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b2038-138">required</span></span>  <br/> |<span data-ttu-id="b2038-139">Указывает страницу для атрибута ID в документе.</span><span class="sxs-lookup"><span data-stu-id="b2038-139">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="b2038-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2038-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2038-141">T</span><span class="sxs-lookup"><span data-stu-id="b2038-141">T</span></span>  <br/> |<span data-ttu-id="b2038-142">XSD:String</span><span class="sxs-lookup"><span data-stu-id="b2038-142">xsd:string</span></span>  <br/> |<span data-ttu-id="b2038-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b2038-143">required</span></span>  <br/> |<span data-ttu-id="b2038-144">Указывает тип ссылки.</span><span class="sxs-lookup"><span data-stu-id="b2038-144">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="b2038-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b2038-145">Values of the xsd:string type.</span></span>  <br/> |
   

