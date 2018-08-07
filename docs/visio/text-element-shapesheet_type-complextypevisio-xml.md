---
title: Элемент Text (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Содержит текст фигуры.
ms.openlocfilehash: 636f349b0a93719cd157db563b238147af5584cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814990"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="2f86d-103">Элемент Text (ShapeSheet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="2f86d-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2f86d-104">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="2f86d-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f86d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2f86d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f86d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="2f86d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2f86d-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="2f86d-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2f86d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2f86d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2f86d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2f86d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2f86d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2f86d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2f86d-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="2f86d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2f86d-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="2f86d-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f86d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="2f86d-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2f86d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2f86d-114">Elements and attributes</span></span>

<span data-ttu-id="2f86d-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="2f86d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2f86d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2f86d-116">Parent elements</span></span>

|<span data-ttu-id="2f86d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2f86d-117">**Element**</span></span>|<span data-ttu-id="2f86d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2f86d-118">**Type**</span></span>|<span data-ttu-id="2f86d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2f86d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f86d-120">Фигура</span><span class="sxs-lookup"><span data-stu-id="2f86d-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2f86d-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="2f86d-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2f86d-122">Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.</span><span class="sxs-lookup"><span data-stu-id="2f86d-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2f86d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2f86d-123">Child elements</span></span>

|<span data-ttu-id="2f86d-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2f86d-124">**Element**</span></span>|<span data-ttu-id="2f86d-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2f86d-125">**Type**</span></span>|<span data-ttu-id="2f86d-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2f86d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f86d-127">позиции символа</span><span class="sxs-lookup"><span data-stu-id="2f86d-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2f86d-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="2f86d-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2f86d-129">Метки в начале символ свойства запустите то есть отформатированное в соответствии с соответствующих элементов (знак).</span><span class="sxs-lookup"><span data-stu-id="2f86d-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="2f86d-130">Fld</span><span class="sxs-lookup"><span data-stu-id="2f86d-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2f86d-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="2f86d-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2f86d-132">Указывает точку вставки текстового поля для соответствующего элемента Field.</span><span class="sxs-lookup"><span data-stu-id="2f86d-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="2f86d-133">PP</span><span class="sxs-lookup"><span data-stu-id="2f86d-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2f86d-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="2f86d-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2f86d-135">Выполнение в начале свойств абзаца.</span><span class="sxs-lookup"><span data-stu-id="2f86d-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="2f86d-136">TP</span><span class="sxs-lookup"><span data-stu-id="2f86d-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2f86d-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="2f86d-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2f86d-138">Задает начало вкладок свойств, запустите.</span><span class="sxs-lookup"><span data-stu-id="2f86d-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2f86d-139">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2f86d-139">Attributes</span></span>

<span data-ttu-id="2f86d-140">Нет.</span><span class="sxs-lookup"><span data-stu-id="2f86d-140">None.</span></span>
  

