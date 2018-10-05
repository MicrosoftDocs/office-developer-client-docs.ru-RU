---
title: Элемент фигур (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 85aa7df3-d9bd-acb3-61b3-2bd5fa256435
description: Содержит коллекцию элементов фигуры.
ms.openlocfilehash: d4de4436079ec6290b52dd74bf3ee015c5b0d3f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392097"
---
# <a name="shapes-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="e368b-103">Элемент фигур (ShapeSheet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e368b-103">Shapes element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e368b-104">Содержит коллекцию элементов фигуры.</span><span class="sxs-lookup"><span data-stu-id="e368b-104">Contains a collection of Shape elements.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e368b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e368b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e368b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e368b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e368b-107">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="e368b-107">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e368b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e368b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e368b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e368b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e368b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e368b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e368b-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e368b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e368b-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="e368b-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e368b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e368b-113">Definition</span></span>

```XML
< xs:element name="Shapes" type="Shapes_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e368b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e368b-114">Elements and attributes</span></span>

<span data-ttu-id="e368b-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e368b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e368b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e368b-116">Parent elements</span></span>

|<span data-ttu-id="e368b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e368b-117">**Element**</span></span>|<span data-ttu-id="e368b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e368b-118">**Type**</span></span>|<span data-ttu-id="e368b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e368b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e368b-120">Фигура</span><span class="sxs-lookup"><span data-stu-id="e368b-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e368b-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e368b-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e368b-122">Задает набор свойств, связанных с фигурой.</span><span class="sxs-lookup"><span data-stu-id="e368b-122">Specifies a collection of properties associated with a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e368b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e368b-123">Child elements</span></span>

|<span data-ttu-id="e368b-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e368b-124">**Element**</span></span>|<span data-ttu-id="e368b-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e368b-125">**Type**</span></span>|<span data-ttu-id="e368b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e368b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e368b-127">Фигура</span><span class="sxs-lookup"><span data-stu-id="e368b-127">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e368b-128">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="e368b-128">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e368b-129">Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.</span><span class="sxs-lookup"><span data-stu-id="e368b-129">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e368b-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e368b-130">Attributes</span></span>

<span data-ttu-id="e368b-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="e368b-131">None.</span></span>
  

