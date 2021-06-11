---
title: Элемент ColorEntry (Colors_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Содержит запись цветовой таблицы.
ms.openlocfilehash: f2221d8d32823e5eec4a100eaf4e8f62b914df28
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540184"
---
# <a name="colorentry-element-colors_type-complextype-visio-xml"></a><span data-ttu-id="e07e5-103">Элемент ColorEntry (Colors_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e07e5-103">ColorEntry element (Colors_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e07e5-104">Содержит запись цветовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="e07e5-104">Contains a color table entry.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e07e5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e07e5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e07e5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e07e5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e07e5-107">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="e07e5-107">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e07e5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e07e5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e07e5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e07e5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e07e5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e07e5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e07e5-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="e07e5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e07e5-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="e07e5-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e07e5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e07e5-113">Definition</span></span>

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e07e5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e07e5-114">Elements and attributes</span></span>

<span data-ttu-id="e07e5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e07e5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e07e5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e07e5-116">Parent elements</span></span>

|<span data-ttu-id="e07e5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e07e5-117">**Element**</span></span>|<span data-ttu-id="e07e5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e07e5-118">**Type**</span></span>|<span data-ttu-id="e07e5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e07e5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e07e5-120">Colors</span><span class="sxs-lookup"><span data-stu-id="e07e5-120">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e07e5-121">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="e07e5-121">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e07e5-122">Содержит цветовую таблицу документа.</span><span class="sxs-lookup"><span data-stu-id="e07e5-122">Contains the document's color table.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e07e5-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e07e5-123">Child elements</span></span>

<span data-ttu-id="e07e5-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="e07e5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e07e5-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e07e5-125">Attributes</span></span>

|<span data-ttu-id="e07e5-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e07e5-126">**Attribute**</span></span>|<span data-ttu-id="e07e5-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e07e5-127">**Type**</span></span>|<span data-ttu-id="e07e5-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e07e5-128">**Required**</span></span>|<span data-ttu-id="e07e5-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e07e5-129">**Description**</span></span>|<span data-ttu-id="e07e5-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e07e5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e07e5-131">IX</span><span class="sxs-lookup"><span data-stu-id="e07e5-131">IX</span></span>  <br/> |<span data-ttu-id="e07e5-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e07e5-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e07e5-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e07e5-133">required</span></span>  <br/> |<span data-ttu-id="e07e5-134">Нулевой индекс элемента в родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="e07e5-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="e07e5-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e07e5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e07e5-136">RGB</span><span class="sxs-lookup"><span data-stu-id="e07e5-136">RGB</span></span>  <br/> |<span data-ttu-id="e07e5-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e07e5-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e07e5-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e07e5-138">required</span></span>  <br/> |<span data-ttu-id="e07e5-139">Hexadecimal value of the color table entry.</span><span class="sxs-lookup"><span data-stu-id="e07e5-139">The hexadecimal value of the color table entry.</span></span>  <br/> |<span data-ttu-id="e07e5-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e07e5-140">Values of the xsd:string type.</span></span>  <br/> |
   

