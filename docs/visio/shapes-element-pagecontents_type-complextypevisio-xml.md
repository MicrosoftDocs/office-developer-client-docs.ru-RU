---
title: Элемент Shapes (PageContents_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f9d51d7-e2b7-bc68-dede-c79fb9dbcf60
description: Содержит коллекцию элементов Shape.
ms.openlocfilehash: 5d248dd2683a1ccc153d15477c888e1b13d24d0f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542123"
---
# <a name="shapes-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="4f896-103">Элемент Shapes (PageContents_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4f896-103">Shapes element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4f896-104">Содержит коллекцию элементов Shape.</span><span class="sxs-lookup"><span data-stu-id="4f896-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4f896-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4f896-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4f896-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4f896-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4f896-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="4f896-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4f896-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4f896-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4f896-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4f896-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4f896-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4f896-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4f896-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="4f896-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4f896-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="4f896-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4f896-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4f896-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4f896-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4f896-114">Elements and attributes</span></span>

<span data-ttu-id="4f896-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4f896-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4f896-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4f896-116">Parent elements</span></span>

|<span data-ttu-id="4f896-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4f896-117">**Element**</span></span>|<span data-ttu-id="4f896-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4f896-118">**Type**</span></span>|<span data-ttu-id="4f896-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f896-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f896-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="4f896-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f896-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="4f896-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f896-122">Указывает сведения о фигурах мастера в веб-рисунке.</span><span class="sxs-lookup"><span data-stu-id="4f896-122">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
|[<span data-ttu-id="4f896-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="4f896-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="4f896-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="4f896-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f896-125">Указывает сведения о фигурах мастера в веб-рисунке.</span><span class="sxs-lookup"><span data-stu-id="4f896-125">Specifies information about the shapes in a master in a Web drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4f896-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4f896-126">Child elements</span></span>

|<span data-ttu-id="4f896-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4f896-127">**Element**</span></span>|<span data-ttu-id="4f896-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4f896-128">**Type**</span></span>|<span data-ttu-id="4f896-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f896-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4f896-130">Shape</span><span class="sxs-lookup"><span data-stu-id="4f896-130">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4f896-131">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4f896-131">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4f896-132">Содержит элементы, определяющие фигуру в **элементе Master,** **Page** или group shape.</span><span class="sxs-lookup"><span data-stu-id="4f896-132">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4f896-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4f896-133">Attributes</span></span>

<span data-ttu-id="4f896-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="4f896-134">None.</span></span>
  

