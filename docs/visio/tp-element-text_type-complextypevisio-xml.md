---
title: элемент TP (Текст_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Задает начало работы со свойствами вкладок. Выполнение определяется до конца текста или до следующего тега.
ms.openlocfilehash: 3f27ea0babefa0ea69cbbc361031c57602649107
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307702"
---
# <a name="tp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="687c9-104">элемент TP (Текст_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="687c9-104">tp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="687c9-105">Задает начало работы со свойствами вкладок.</span><span class="sxs-lookup"><span data-stu-id="687c9-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="687c9-106">Выполнение определяется до конца текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="687c9-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="687c9-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="687c9-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="687c9-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="687c9-108">**Element type**</span></span> <br/> |[<span data-ttu-id="687c9-109">Тп_типе</span><span class="sxs-lookup"><span data-stu-id="687c9-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="687c9-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="687c9-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="687c9-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="687c9-111">**Schema file**</span></span> <br/> |<span data-ttu-id="687c9-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="687c9-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="687c9-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="687c9-113">**Document parts**</span></span> <br/> |<span data-ttu-id="687c9-114">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="687c9-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="687c9-115">Определение</span><span class="sxs-lookup"><span data-stu-id="687c9-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="687c9-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="687c9-116">Elements and attributes</span></span>

<span data-ttu-id="687c9-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="687c9-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="687c9-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="687c9-118">Parent elements</span></span>

|<span data-ttu-id="687c9-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="687c9-119">**Element**</span></span>|<span data-ttu-id="687c9-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="687c9-120">**Type**</span></span>|<span data-ttu-id="687c9-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="687c9-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="687c9-122">Text</span><span class="sxs-lookup"><span data-stu-id="687c9-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="687c9-123">Текст_типе</span><span class="sxs-lookup"><span data-stu-id="687c9-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="687c9-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="687c9-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="687c9-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="687c9-125">Child elements</span></span>

<span data-ttu-id="687c9-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="687c9-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="687c9-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="687c9-127">Attributes</span></span>

|<span data-ttu-id="687c9-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="687c9-128">**Attribute**</span></span>|<span data-ttu-id="687c9-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="687c9-129">**Type**</span></span>|<span data-ttu-id="687c9-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="687c9-130">**Required**</span></span>|<span data-ttu-id="687c9-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="687c9-131">**Description**</span></span>|<span data-ttu-id="687c9-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="687c9-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="687c9-133">IX</span><span class="sxs-lookup"><span data-stu-id="687c9-133">IX</span></span>  <br/> |<span data-ttu-id="687c9-134">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="687c9-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="687c9-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="687c9-135">required</span></span>  <br/> |<span data-ttu-id="687c9-136">Отсчитываемый от нуля индекс элемента в его родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="687c9-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="687c9-137">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="687c9-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

