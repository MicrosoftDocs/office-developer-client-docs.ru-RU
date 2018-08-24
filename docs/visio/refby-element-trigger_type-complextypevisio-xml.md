---
title: Элемент RefBy (Trigger_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Задает ссылку на страницу в документе.
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572433"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="14a38-103">Элемент RefBy (Trigger_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="14a38-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="14a38-104">Задает ссылку на страницу в документе.</span><span class="sxs-lookup"><span data-stu-id="14a38-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="14a38-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="14a38-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="14a38-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="14a38-106">**Element type**</span></span> <br/> |[<span data-ttu-id="14a38-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="14a38-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="14a38-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="14a38-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="14a38-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="14a38-109">**Schema file**</span></span> <br/> |<span data-ttu-id="14a38-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="14a38-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="14a38-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="14a38-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="14a38-112">Определение</span><span class="sxs-lookup"><span data-stu-id="14a38-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="14a38-113">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="14a38-113">Elements and attributes</span></span>

<span data-ttu-id="14a38-114">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="14a38-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="14a38-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="14a38-115">Parent elements</span></span>

|<span data-ttu-id="14a38-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="14a38-116">**Element**</span></span>|<span data-ttu-id="14a38-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="14a38-117">**Type**</span></span>|<span data-ttu-id="14a38-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="14a38-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="14a38-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="14a38-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="14a38-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="14a38-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="14a38-121">Инструкции для Microsoft Visio для пересчета отношение между частями документа в файл Visio.</span><span class="sxs-lookup"><span data-stu-id="14a38-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="14a38-122">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="14a38-122">Child elements</span></span>

<span data-ttu-id="14a38-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="14a38-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="14a38-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="14a38-124">Attributes</span></span>

|<span data-ttu-id="14a38-125">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="14a38-125">**Attribute**</span></span>|<span data-ttu-id="14a38-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="14a38-126">**Type**</span></span>|<span data-ttu-id="14a38-127">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="14a38-127">**Required**</span></span>|<span data-ttu-id="14a38-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="14a38-128">**Description**</span></span>|<span data-ttu-id="14a38-129">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="14a38-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="14a38-130">ID</span><span class="sxs-lookup"><span data-stu-id="14a38-130">ID</span></span>  <br/> |<span data-ttu-id="14a38-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="14a38-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="14a38-132">Обязательный</span><span class="sxs-lookup"><span data-stu-id="14a38-132">required</span></span>  <br/> |<span data-ttu-id="14a38-133">Указывает страницу для атрибута ID в документе.</span><span class="sxs-lookup"><span data-stu-id="14a38-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="14a38-134">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="14a38-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="14a38-135">T</span><span class="sxs-lookup"><span data-stu-id="14a38-135">T</span></span>  <br/> |<span data-ttu-id="14a38-136">XSD:String</span><span class="sxs-lookup"><span data-stu-id="14a38-136">xsd:string</span></span>  <br/> |<span data-ttu-id="14a38-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="14a38-137">required</span></span>  <br/> |<span data-ttu-id="14a38-138">Указывает тип ссылки.</span><span class="sxs-lookup"><span data-stu-id="14a38-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="14a38-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="14a38-139">Values of the xsd:string type.</span></span>  <br/> |
   

