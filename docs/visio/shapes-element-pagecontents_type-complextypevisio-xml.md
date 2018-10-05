---
title: Элемент фигур (PageContents_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Содержит коллекцию элементов фигуры.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397571"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="3d5ba-103">Элемент фигур (PageContents_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="3d5ba-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3d5ba-104">Содержит коллекцию элементов фигуры.</span><span class="sxs-lookup"><span data-stu-id="3d5ba-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3d5ba-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3d5ba-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3d5ba-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3d5ba-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="3d5ba-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3d5ba-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3d5ba-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3d5ba-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3d5ba-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3d5ba-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3d5ba-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="3d5ba-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3d5ba-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3d5ba-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3d5ba-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3d5ba-114">Elements and attributes</span></span>

<span data-ttu-id="3d5ba-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3d5ba-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3d5ba-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3d5ba-116">Parent elements</span></span>

|<span data-ttu-id="3d5ba-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-117">**Element**</span></span>|<span data-ttu-id="3d5ba-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-118">**Type**</span></span>|<span data-ttu-id="3d5ba-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3d5ba-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="3d5ba-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="3d5ba-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="3d5ba-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3d5ba-122">Задает сведения о фигурах в главный в веб-документ.</span><span class="sxs-lookup"><span data-stu-id="3d5ba-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="3d5ba-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="3d5ba-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="3d5ba-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="3d5ba-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3d5ba-125">Задает сведения о фигурах в главный в веб-документ.</span><span class="sxs-lookup"><span data-stu-id="3d5ba-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3d5ba-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3d5ba-126">Child elements</span></span>

|<span data-ttu-id="3d5ba-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-127">**Element**</span></span>|<span data-ttu-id="3d5ba-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-128">**Type**</span></span>|<span data-ttu-id="3d5ba-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3d5ba-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3d5ba-130">Фигура</span><span class="sxs-lookup"><span data-stu-id="3d5ba-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3d5ba-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="3d5ba-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3d5ba-132">Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.</span><span class="sxs-lookup"><span data-stu-id="3d5ba-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3d5ba-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3d5ba-133">Attributes</span></span>

<span data-ttu-id="3d5ba-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="3d5ba-134">None.</span></span>
  

