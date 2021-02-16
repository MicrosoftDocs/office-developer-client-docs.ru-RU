---
title: Элемент RefBy (Trigger_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Указывает ссылку на страницу в документе.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538293"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="e8757-103">Элемент RefBy (Trigger_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e8757-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e8757-104">Указывает ссылку на страницу в документе.</span><span class="sxs-lookup"><span data-stu-id="e8757-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8757-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e8757-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8757-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e8757-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e8757-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="e8757-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e8757-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e8757-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e8757-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e8757-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e8757-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e8757-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e8757-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e8757-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="e8757-112">Определение</span><span class="sxs-lookup"><span data-stu-id="e8757-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e8757-113">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e8757-113">Elements and attributes</span></span>

<span data-ttu-id="e8757-114">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e8757-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e8757-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e8757-115">Parent elements</span></span>

|<span data-ttu-id="e8757-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e8757-116">**Element**</span></span>|<span data-ttu-id="e8757-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e8757-117">**Type**</span></span>|<span data-ttu-id="e8757-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8757-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e8757-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="e8757-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="e8757-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="e8757-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e8757-121">Содержит инструкции для Microsoft Visio по пересчету связи между частями документа в файле Visio.</span><span class="sxs-lookup"><span data-stu-id="e8757-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="e8757-122">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e8757-122">Child elements</span></span>

<span data-ttu-id="e8757-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="e8757-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8757-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e8757-124">Attributes</span></span>

|<span data-ttu-id="e8757-125">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e8757-125">**Attribute**</span></span>|<span data-ttu-id="e8757-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e8757-126">**Type**</span></span>|<span data-ttu-id="e8757-127">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e8757-127">**Required**</span></span>|<span data-ttu-id="e8757-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8757-128">**Description**</span></span>|<span data-ttu-id="e8757-129">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e8757-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e8757-130">ID</span><span class="sxs-lookup"><span data-stu-id="e8757-130">ID</span></span>  <br/> |<span data-ttu-id="e8757-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e8757-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e8757-132">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e8757-132">required</span></span>  <br/> |<span data-ttu-id="e8757-133">Указывает атрибут ID страницы в документе.</span><span class="sxs-lookup"><span data-stu-id="e8757-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="e8757-134">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e8757-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e8757-135">T</span><span class="sxs-lookup"><span data-stu-id="e8757-135">T</span></span>  <br/> |<span data-ttu-id="e8757-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e8757-136">xsd:string</span></span>  <br/> |<span data-ttu-id="e8757-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e8757-137">required</span></span>  <br/> |<span data-ttu-id="e8757-138">Указывает тип ссылки.</span><span class="sxs-lookup"><span data-stu-id="e8757-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="e8757-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e8757-139">Values of the xsd:string type.</span></span>  <br/> |
   

