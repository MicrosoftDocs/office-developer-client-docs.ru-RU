---
title: Элемент Shapes (Пажеконтентс_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Содержит коллекцию элементов Shape.
ms.openlocfilehash: 7abece2a9fc8d88817f22c654567272becce981e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349170"
---
# <a name="shapes-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="7cb1e-103">Элемент Shapes (Пажеконтентс_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="7cb1e-103">Shapes element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7cb1e-104">Содержит коллекцию элементов Shape.</span><span class="sxs-lookup"><span data-stu-id="7cb1e-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7cb1e-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7cb1e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cb1e-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7cb1e-107">Шапес_типе</span><span class="sxs-lookup"><span data-stu-id="7cb1e-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7cb1e-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7cb1e-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7cb1e-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7cb1e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7cb1e-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7cb1e-112">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="7cb1e-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7cb1e-113">Определение</span><span class="sxs-lookup"><span data-stu-id="7cb1e-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7cb1e-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7cb1e-114">Elements and attributes</span></span>

<span data-ttu-id="7cb1e-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7cb1e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7cb1e-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7cb1e-116">Parent elements</span></span>

|<span data-ttu-id="7cb1e-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-117">**Element**</span></span>|<span data-ttu-id="7cb1e-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-118">**Type**</span></span>|<span data-ttu-id="7cb1e-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7cb1e-120">Мастерконтентс</span><span class="sxs-lookup"><span data-stu-id="7cb1e-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="7cb1e-121">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="7cb1e-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7cb1e-122">Задает сведения о фигурах в образце в веб-документе.</span><span class="sxs-lookup"><span data-stu-id="7cb1e-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="7cb1e-123">Пажеконтентс</span><span class="sxs-lookup"><span data-stu-id="7cb1e-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="7cb1e-124">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="7cb1e-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7cb1e-125">Задает сведения о фигурах в образце в веб-документе.</span><span class="sxs-lookup"><span data-stu-id="7cb1e-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7cb1e-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7cb1e-126">Child elements</span></span>

|<span data-ttu-id="7cb1e-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-127">**Element**</span></span>|<span data-ttu-id="7cb1e-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-128">**Type**</span></span>|<span data-ttu-id="7cb1e-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7cb1e-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7cb1e-130">Shape</span><span class="sxs-lookup"><span data-stu-id="7cb1e-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7cb1e-131">Шапешит_типе</span><span class="sxs-lookup"><span data-stu-id="7cb1e-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7cb1e-132">Содержит элементы, определяющие фигуру в **главной**, **странице**или элементе фигуры группы.</span><span class="sxs-lookup"><span data-stu-id="7cb1e-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7cb1e-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7cb1e-133">Attributes</span></span>

<span data-ttu-id="7cb1e-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="7cb1e-134">None.</span></span>
  

