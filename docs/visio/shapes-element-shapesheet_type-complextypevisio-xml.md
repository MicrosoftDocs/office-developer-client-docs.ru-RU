---
title: Элемент фигур (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Содержит коллекцию элементов фигуры.
ms.openlocfilehash: d2e725a28873cac8dded49587a98400df1d9bf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814804"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="ad159-103">Элемент фигур (ShapeSheet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="ad159-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ad159-104">Содержит коллекцию элементов фигуры.</span><span class="sxs-lookup"><span data-stu-id="ad159-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad159-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ad159-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad159-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ad159-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad159-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="ad159-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad159-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ad159-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad159-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ad159-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad159-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ad159-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad159-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ad159-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad159-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="ad159-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad159-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ad159-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad159-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ad159-114">Elements and attributes</span></span>

<span data-ttu-id="ad159-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="ad159-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad159-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ad159-116">Parent elements</span></span>

|<span data-ttu-id="ad159-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ad159-117">**Element**</span></span>|<span data-ttu-id="ad159-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ad159-118">**Type**</span></span>|<span data-ttu-id="ad159-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad159-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad159-120">Фигура</span><span class="sxs-lookup"><span data-stu-id="ad159-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad159-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ad159-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad159-122">Задает набор свойств, связанных с фигурой.</span><span class="sxs-lookup"><span data-stu-id="ad159-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad159-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ad159-123">Child elements</span></span>

|<span data-ttu-id="ad159-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ad159-124">**Element**</span></span>|<span data-ttu-id="ad159-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ad159-125">**Type**</span></span>|<span data-ttu-id="ad159-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad159-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad159-127">Фигура</span><span class="sxs-lookup"><span data-stu-id="ad159-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad159-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="ad159-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad159-129">Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.</span><span class="sxs-lookup"><span data-stu-id="ad159-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ad159-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ad159-130">Attributes</span></span>

<span data-ttu-id="ad159-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="ad159-131">None.</span></span>
  

