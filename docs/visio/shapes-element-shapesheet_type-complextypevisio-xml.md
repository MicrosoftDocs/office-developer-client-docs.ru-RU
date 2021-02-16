---
title: Элемент Shapes (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Содержит коллекцию элементов Shape.
ms.openlocfilehash: e9f45d1f61b83339274d24aea2c0473adf282bac
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542102"
---
# <a name="shapes-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="1323f-103">Элемент Shapes (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1323f-103">Shapes element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1323f-104">Содержит коллекцию элементов Shape.</span><span class="sxs-lookup"><span data-stu-id="1323f-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1323f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1323f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1323f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="1323f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1323f-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="1323f-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1323f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1323f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1323f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1323f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1323f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1323f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1323f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="1323f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1323f-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="1323f-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1323f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="1323f-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1323f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1323f-114">Elements and attributes</span></span>

<span data-ttu-id="1323f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1323f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1323f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1323f-116">Parent elements</span></span>

|<span data-ttu-id="1323f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1323f-117">**Element**</span></span>|<span data-ttu-id="1323f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1323f-118">**Type**</span></span>|<span data-ttu-id="1323f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1323f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1323f-120">Shape</span><span class="sxs-lookup"><span data-stu-id="1323f-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1323f-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1323f-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1323f-122">Указывает коллекцию свойств, связанных с фигурой.</span><span class="sxs-lookup"><span data-stu-id="1323f-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1323f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1323f-123">Child elements</span></span>

|<span data-ttu-id="1323f-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1323f-124">**Element**</span></span>|<span data-ttu-id="1323f-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1323f-125">**Type**</span></span>|<span data-ttu-id="1323f-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1323f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1323f-127">Shape</span><span class="sxs-lookup"><span data-stu-id="1323f-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1323f-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="1323f-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1323f-129">Содержит элементы, определяющие фигуру в элементе **"Master",** **"Page"** или "group shape".</span><span class="sxs-lookup"><span data-stu-id="1323f-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1323f-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1323f-130">Attributes</span></span>

<span data-ttu-id="1323f-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="1323f-131">None.</span></span>
  

