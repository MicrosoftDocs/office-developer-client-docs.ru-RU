---
title: элемент TP (Text_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Задает начало вкладок свойств, запустите. Запустить определен в конец текста или до следующего тега.
ms.openlocfilehash: 9b98374af4ffbf2eaeaea61dcb1dbb49214f01b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815050"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="97c66-104">элемент TP (Text_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="97c66-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="97c66-105">Задает начало вкладок свойств, запустите.</span><span class="sxs-lookup"><span data-stu-id="97c66-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="97c66-106">Запустить определен в конец текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="97c66-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97c66-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="97c66-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97c66-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="97c66-108">**Element type**</span></span> <br/> |[<span data-ttu-id="97c66-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="97c66-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="97c66-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="97c66-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="97c66-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="97c66-111">**Schema file**</span></span> <br/> |<span data-ttu-id="97c66-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="97c66-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="97c66-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="97c66-113">**Document parts**</span></span> <br/> |<span data-ttu-id="97c66-114">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="97c66-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="97c66-115">Определение</span><span class="sxs-lookup"><span data-stu-id="97c66-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="97c66-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="97c66-116">Elements and attributes</span></span>

<span data-ttu-id="97c66-117">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="97c66-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="97c66-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="97c66-118">Parent elements</span></span>

|<span data-ttu-id="97c66-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="97c66-119">**Element**</span></span>|<span data-ttu-id="97c66-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="97c66-120">**Type**</span></span>|<span data-ttu-id="97c66-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="97c66-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="97c66-122">Text</span><span class="sxs-lookup"><span data-stu-id="97c66-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="97c66-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="97c66-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="97c66-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="97c66-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="97c66-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="97c66-125">Child elements</span></span>

<span data-ttu-id="97c66-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="97c66-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97c66-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="97c66-127">Attributes</span></span>

|<span data-ttu-id="97c66-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="97c66-128">**Attribute**</span></span>|<span data-ttu-id="97c66-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="97c66-129">**Type**</span></span>|<span data-ttu-id="97c66-130">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="97c66-130">**Required**</span></span>|<span data-ttu-id="97c66-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="97c66-131">**Description**</span></span>|<span data-ttu-id="97c66-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="97c66-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="97c66-133">IX</span><span class="sxs-lookup"><span data-stu-id="97c66-133">IX</span></span>  <br/> |<span data-ttu-id="97c66-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="97c66-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="97c66-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="97c66-135">required</span></span>  <br/> |<span data-ttu-id="97c66-136">Отсчитываемый от нуля индекс элемента в рамках родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="97c66-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="97c66-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="97c66-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

