---
title: Элемент text (Шапешит_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Содержит текст фигуры.
ms.openlocfilehash: 4b03bc2539b80e49daae9d14f3e2ad07a51de9f1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541927"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="b56af-103">Элемент text (Шапешит_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="b56af-103">Text element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b56af-104">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="b56af-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b56af-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b56af-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b56af-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b56af-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b56af-107">Текст_типе</span><span class="sxs-lookup"><span data-stu-id="b56af-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b56af-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b56af-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b56af-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b56af-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b56af-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b56af-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b56af-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b56af-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b56af-112">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="b56af-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b56af-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b56af-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b56af-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b56af-114">Elements and attributes</span></span>

<span data-ttu-id="b56af-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b56af-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b56af-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b56af-116">Parent elements</span></span>

|<span data-ttu-id="b56af-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b56af-117">**Element**</span></span>|<span data-ttu-id="b56af-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b56af-118">**Type**</span></span>|<span data-ttu-id="b56af-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b56af-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b56af-120">Shape</span><span class="sxs-lookup"><span data-stu-id="b56af-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b56af-121">Шапешит_типе</span><span class="sxs-lookup"><span data-stu-id="b56af-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b56af-122">Содержит элементы, определяющие фигуру в **главной**, **странице**или элементе фигуры группы.</span><span class="sxs-lookup"><span data-stu-id="b56af-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b56af-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b56af-123">Child elements</span></span>

|<span data-ttu-id="b56af-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b56af-124">**Element**</span></span>|<span data-ttu-id="b56af-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b56af-125">**Type**</span></span>|<span data-ttu-id="b56af-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b56af-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b56af-127">CP</span><span class="sxs-lookup"><span data-stu-id="b56af-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b56af-128">Кп_типе</span><span class="sxs-lookup"><span data-stu-id="b56af-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b56af-129">Помечает начало свойства знака, которое отформатировано в соответствии с соответствующим элементом char.</span><span class="sxs-lookup"><span data-stu-id="b56af-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="b56af-130">FLD</span><span class="sxs-lookup"><span data-stu-id="b56af-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b56af-131">Флд_типе</span><span class="sxs-lookup"><span data-stu-id="b56af-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b56af-132">Указывает точку вставки текстового поля для соответствующего элемента Field.</span><span class="sxs-lookup"><span data-stu-id="b56af-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="b56af-133">PP</span><span class="sxs-lookup"><span data-stu-id="b56af-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b56af-134">Пп_типе</span><span class="sxs-lookup"><span data-stu-id="b56af-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b56af-135">Задает начало работы со свойствами абзаца.</span><span class="sxs-lookup"><span data-stu-id="b56af-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="b56af-136">Пи</span><span class="sxs-lookup"><span data-stu-id="b56af-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b56af-137">Тп_типе</span><span class="sxs-lookup"><span data-stu-id="b56af-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b56af-138">Задает начало работы со свойствами вкладок.</span><span class="sxs-lookup"><span data-stu-id="b56af-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b56af-139">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b56af-139">Attributes</span></span>

<span data-ttu-id="b56af-140">Нет.</span><span class="sxs-lookup"><span data-stu-id="b56af-140">None.</span></span>
  

