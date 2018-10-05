---
title: Элемент RefBy (Trigger_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Задает ссылку на страницу в документе.
ms.openlocfilehash: d987825345b64bd6e202970fc786aedaf49c6a94
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383319"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="b425c-103">Элемент RefBy (Trigger_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b425c-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b425c-104">Задает ссылку на страницу в документе.</span><span class="sxs-lookup"><span data-stu-id="b425c-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b425c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b425c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b425c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b425c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b425c-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="b425c-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b425c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b425c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b425c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b425c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b425c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b425c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b425c-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b425c-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="b425c-112">Определение</span><span class="sxs-lookup"><span data-stu-id="b425c-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b425c-113">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b425c-113">Elements and attributes</span></span>

<span data-ttu-id="b425c-114">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b425c-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b425c-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b425c-115">Parent elements</span></span>

|<span data-ttu-id="b425c-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b425c-116">**Element**</span></span>|<span data-ttu-id="b425c-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b425c-117">**Type**</span></span>|<span data-ttu-id="b425c-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b425c-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b425c-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="b425c-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="b425c-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="b425c-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b425c-121">Инструкции для Microsoft Visio для пересчета отношение между частями документа в файл Visio.</span><span class="sxs-lookup"><span data-stu-id="b425c-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="b425c-122">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b425c-122">Child elements</span></span>

<span data-ttu-id="b425c-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="b425c-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b425c-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b425c-124">Attributes</span></span>

|<span data-ttu-id="b425c-125">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b425c-125">**Attribute**</span></span>|<span data-ttu-id="b425c-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b425c-126">**Type**</span></span>|<span data-ttu-id="b425c-127">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b425c-127">**Required**</span></span>|<span data-ttu-id="b425c-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b425c-128">**Description**</span></span>|<span data-ttu-id="b425c-129">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b425c-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b425c-130">ID</span><span class="sxs-lookup"><span data-stu-id="b425c-130">ID</span></span>  <br/> |<span data-ttu-id="b425c-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b425c-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b425c-132">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b425c-132">required</span></span>  <br/> |<span data-ttu-id="b425c-133">Указывает страницу для атрибута ID в документе.</span><span class="sxs-lookup"><span data-stu-id="b425c-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="b425c-134">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b425c-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b425c-135">T</span><span class="sxs-lookup"><span data-stu-id="b425c-135">T</span></span>  <br/> |<span data-ttu-id="b425c-136">XSD:String</span><span class="sxs-lookup"><span data-stu-id="b425c-136">xsd:string</span></span>  <br/> |<span data-ttu-id="b425c-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b425c-137">required</span></span>  <br/> |<span data-ttu-id="b425c-138">Указывает тип ссылки.</span><span class="sxs-lookup"><span data-stu-id="b425c-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="b425c-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="b425c-139">Values of the xsd:string type.</span></span>  <br/> |
   

