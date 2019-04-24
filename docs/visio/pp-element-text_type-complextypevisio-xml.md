---
title: элемент PP (Текст_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Задает начало работы со свойствами абзаца. Выполнение определяется до конца текста или до следующего тега.
ms.openlocfilehash: bb2b0ab7a76c142b810ecd02dbc1b5ba7463520a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356079"
---
# <a name="pp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="18f17-104">элемент PP (Текст_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="18f17-104">pp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="18f17-105">Задает начало работы со свойствами абзаца.</span><span class="sxs-lookup"><span data-stu-id="18f17-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="18f17-106">Выполнение определяется до конца текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="18f17-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="18f17-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="18f17-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18f17-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="18f17-108">**Element type**</span></span> <br/> |[<span data-ttu-id="18f17-109">Пп_типе</span><span class="sxs-lookup"><span data-stu-id="18f17-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="18f17-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="18f17-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="18f17-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="18f17-111">**Schema file**</span></span> <br/> |<span data-ttu-id="18f17-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="18f17-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="18f17-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="18f17-113">**Document parts**</span></span> <br/> |<span data-ttu-id="18f17-114">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="18f17-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18f17-115">Определение</span><span class="sxs-lookup"><span data-stu-id="18f17-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="18f17-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="18f17-116">Elements and attributes</span></span>

<span data-ttu-id="18f17-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="18f17-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="18f17-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="18f17-118">Parent elements</span></span>

|<span data-ttu-id="18f17-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="18f17-119">**Element**</span></span>|<span data-ttu-id="18f17-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="18f17-120">**Type**</span></span>|<span data-ttu-id="18f17-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="18f17-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18f17-122">Text</span><span class="sxs-lookup"><span data-stu-id="18f17-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="18f17-123">Текст_типе</span><span class="sxs-lookup"><span data-stu-id="18f17-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="18f17-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="18f17-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="18f17-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="18f17-125">Child elements</span></span>

<span data-ttu-id="18f17-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="18f17-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="18f17-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="18f17-127">Attributes</span></span>

|<span data-ttu-id="18f17-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="18f17-128">**Attribute**</span></span>|<span data-ttu-id="18f17-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="18f17-129">**Type**</span></span>|<span data-ttu-id="18f17-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="18f17-130">**Required**</span></span>|<span data-ttu-id="18f17-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="18f17-131">**Description**</span></span>|<span data-ttu-id="18f17-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="18f17-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="18f17-133">IX</span><span class="sxs-lookup"><span data-stu-id="18f17-133">IX</span></span>  <br/> |<span data-ttu-id="18f17-134">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="18f17-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="18f17-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="18f17-135">required</span></span>  <br/> |<span data-ttu-id="18f17-136">Индекс элемента абзаца \*\*\*\* , который определяет форматирование, применяемое к данному запуску.</span><span class="sxs-lookup"><span data-stu-id="18f17-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="18f17-137">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="18f17-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

