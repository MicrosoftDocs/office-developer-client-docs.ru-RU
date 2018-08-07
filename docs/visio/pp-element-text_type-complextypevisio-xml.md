---
title: элемент PP (Text_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Выполнение в начале свойств абзаца. Запустить определен в конец текста или до следующего тега.
ms.openlocfilehash: ce1bdd89ca9a5eb5b7ce9b73cc2354ccfde1c125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814465"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="fbf6e-104">элемент PP (Text_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="fbf6e-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fbf6e-105">Выполнение в начале свойств абзаца.</span><span class="sxs-lookup"><span data-stu-id="fbf6e-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="fbf6e-106">Запустить определен в конец текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="fbf6e-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbf6e-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fbf6e-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbf6e-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-108">**Element type**</span></span> <br/> |[<span data-ttu-id="fbf6e-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="fbf6e-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fbf6e-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fbf6e-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-111">**Schema file**</span></span> <br/> |<span data-ttu-id="fbf6e-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fbf6e-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fbf6e-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-113">**Document parts**</span></span> <br/> |<span data-ttu-id="fbf6e-114">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="fbf6e-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fbf6e-115">Определение</span><span class="sxs-lookup"><span data-stu-id="fbf6e-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fbf6e-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fbf6e-116">Elements and attributes</span></span>

<span data-ttu-id="fbf6e-117">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="fbf6e-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fbf6e-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fbf6e-118">Parent elements</span></span>

|<span data-ttu-id="fbf6e-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-119">**Element**</span></span>|<span data-ttu-id="fbf6e-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-120">**Type**</span></span>|<span data-ttu-id="fbf6e-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fbf6e-122">Text</span><span class="sxs-lookup"><span data-stu-id="fbf6e-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fbf6e-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="fbf6e-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fbf6e-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="fbf6e-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fbf6e-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fbf6e-125">Child elements</span></span>

<span data-ttu-id="fbf6e-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="fbf6e-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbf6e-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fbf6e-127">Attributes</span></span>

|<span data-ttu-id="fbf6e-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-128">**Attribute**</span></span>|<span data-ttu-id="fbf6e-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-129">**Type**</span></span>|<span data-ttu-id="fbf6e-130">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-130">**Required**</span></span>|<span data-ttu-id="fbf6e-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-131">**Description**</span></span>|<span data-ttu-id="fbf6e-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fbf6e-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fbf6e-133">IX</span><span class="sxs-lookup"><span data-stu-id="fbf6e-133">IX</span></span>  <br/> |<span data-ttu-id="fbf6e-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fbf6e-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fbf6e-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="fbf6e-135">required</span></span>  <br/> |<span data-ttu-id="fbf6e-136">Индекс элемента **абзаца** , задающее форматирование, применяемое к данного выполнения.</span><span class="sxs-lookup"><span data-stu-id="fbf6e-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="fbf6e-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fbf6e-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

