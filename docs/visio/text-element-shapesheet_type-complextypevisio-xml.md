---
title: Элемент Text (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46211968-9ad8-07da-f725-3ad136b7a8a1
description: Содержит текст фигуры.
ms.openlocfilehash: f2c809d7db895a3635a5898d83d4583cd38f1249
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385916"
---
# <a name="text-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="b7820-103">Элемент Text (ShapeSheet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b7820-103">Text element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b7820-104">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="b7820-104">Contains the text of a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b7820-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7820-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7820-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b7820-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b7820-107">Text_Type</span><span class="sxs-lookup"><span data-stu-id="b7820-107">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b7820-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b7820-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b7820-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b7820-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b7820-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b7820-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b7820-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b7820-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b7820-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="b7820-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7820-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b7820-113">Definition</span></span>

```XML
< xs:element name="Text" type="Text_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b7820-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7820-114">Elements and attributes</span></span>

<span data-ttu-id="b7820-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b7820-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b7820-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b7820-116">Parent elements</span></span>

|<span data-ttu-id="b7820-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b7820-117">**Element**</span></span>|<span data-ttu-id="b7820-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7820-118">**Type**</span></span>|<span data-ttu-id="b7820-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7820-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7820-120">Фигура</span><span class="sxs-lookup"><span data-stu-id="b7820-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7820-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="b7820-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7820-122">Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.</span><span class="sxs-lookup"><span data-stu-id="b7820-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7820-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7820-123">Child elements</span></span>

|<span data-ttu-id="b7820-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b7820-124">**Element**</span></span>|<span data-ttu-id="b7820-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7820-125">**Type**</span></span>|<span data-ttu-id="b7820-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7820-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7820-127">позиции символа</span><span class="sxs-lookup"><span data-stu-id="b7820-127">cp</span></span>](cp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7820-128">cp_Type</span><span class="sxs-lookup"><span data-stu-id="b7820-128">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7820-129">Метки в начале символ свойства запустите то есть отформатированное в соответствии с соответствующих элементов (знак).</span><span class="sxs-lookup"><span data-stu-id="b7820-129">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span>  <br/> |
|[<span data-ttu-id="b7820-130">Fld</span><span class="sxs-lookup"><span data-stu-id="b7820-130">fld</span></span>](fld-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7820-131">fld_Type</span><span class="sxs-lookup"><span data-stu-id="b7820-131">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7820-132">Указывает точку вставки текстового поля для соответствующего элемента Field.</span><span class="sxs-lookup"><span data-stu-id="b7820-132">Indicates a text-field insertion point for the corresponding Field element.</span></span>  <br/> |
|[<span data-ttu-id="b7820-133">PP</span><span class="sxs-lookup"><span data-stu-id="b7820-133">pp</span></span>](pp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7820-134">pp_Type</span><span class="sxs-lookup"><span data-stu-id="b7820-134">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7820-135">Выполнение в начале свойств абзаца.</span><span class="sxs-lookup"><span data-stu-id="b7820-135">Specifies the beginning of a paragraph properties run.</span></span>  <br/> |
|[<span data-ttu-id="b7820-136">TP</span><span class="sxs-lookup"><span data-stu-id="b7820-136">tp</span></span>](tp-element-text_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7820-137">tp_Type</span><span class="sxs-lookup"><span data-stu-id="b7820-137">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7820-138">Задает начало вкладок свойств, запустите.</span><span class="sxs-lookup"><span data-stu-id="b7820-138">Specifies the beginning of a tabs properties run.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b7820-139">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7820-139">Attributes</span></span>

<span data-ttu-id="b7820-140">Нет.</span><span class="sxs-lookup"><span data-stu-id="b7820-140">None.</span></span>
  

