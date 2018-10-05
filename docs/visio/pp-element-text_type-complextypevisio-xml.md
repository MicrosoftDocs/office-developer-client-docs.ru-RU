---
title: элемент PP (Text_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Выполнение в начале свойств абзаца. Запустить определен в конец текста или до следующего тега.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400106"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="ad1bd-104">элемент PP (Text_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ad1bd-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ad1bd-105">Выполнение в начале свойств абзаца.</span><span class="sxs-lookup"><span data-stu-id="ad1bd-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="ad1bd-106">Запустить определен в конец текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="ad1bd-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad1bd-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ad1bd-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad1bd-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-108">**Element type**</span></span> <br/> |[<span data-ttu-id="ad1bd-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="ad1bd-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad1bd-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad1bd-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-111">**Schema file**</span></span> <br/> |<span data-ttu-id="ad1bd-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ad1bd-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad1bd-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-113">**Document parts**</span></span> <br/> |<span data-ttu-id="ad1bd-114">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="ad1bd-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad1bd-115">Определение</span><span class="sxs-lookup"><span data-stu-id="ad1bd-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad1bd-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ad1bd-116">Elements and attributes</span></span>

<span data-ttu-id="ad1bd-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ad1bd-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad1bd-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ad1bd-118">Parent elements</span></span>

|<span data-ttu-id="ad1bd-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-119">**Element**</span></span>|<span data-ttu-id="ad1bd-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-120">**Type**</span></span>|<span data-ttu-id="ad1bd-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad1bd-122">Text</span><span class="sxs-lookup"><span data-stu-id="ad1bd-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad1bd-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="ad1bd-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad1bd-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="ad1bd-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad1bd-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ad1bd-125">Child elements</span></span>

<span data-ttu-id="ad1bd-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="ad1bd-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad1bd-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ad1bd-127">Attributes</span></span>

|<span data-ttu-id="ad1bd-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-128">**Attribute**</span></span>|<span data-ttu-id="ad1bd-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-129">**Type**</span></span>|<span data-ttu-id="ad1bd-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-130">**Required**</span></span>|<span data-ttu-id="ad1bd-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-131">**Description**</span></span>|<span data-ttu-id="ad1bd-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="ad1bd-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad1bd-133">IX</span><span class="sxs-lookup"><span data-stu-id="ad1bd-133">IX</span></span>  <br/> |<span data-ttu-id="ad1bd-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ad1bd-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ad1bd-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="ad1bd-135">required</span></span>  <br/> |<span data-ttu-id="ad1bd-136">Индекс элемента **абзаца** , задающее форматирование, применяемое к данного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ad1bd-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="ad1bd-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ad1bd-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

