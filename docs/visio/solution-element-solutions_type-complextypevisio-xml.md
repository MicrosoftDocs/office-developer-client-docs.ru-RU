---
title: Элемент Solution (Solutions_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Задает один экземпляр решение, которое XML хранятся в документе.
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397200"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="3fd3d-103">Элемент Solution (Solutions_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="3fd3d-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3fd3d-104">Задает один экземпляр решение, которое XML хранятся в документе.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3fd3d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3fd3d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3fd3d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3fd3d-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="3fd3d-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3fd3d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3fd3d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3fd3d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3fd3d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3fd3d-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3fd3d-112">Solutions.XML</span><span class="sxs-lookup"><span data-stu-id="3fd3d-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3fd3d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3fd3d-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3fd3d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3fd3d-114">Elements and attributes</span></span>

<span data-ttu-id="3fd3d-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3fd3d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3fd3d-116">Parent elements</span></span>

|<span data-ttu-id="3fd3d-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-117">**Element**</span></span>|<span data-ttu-id="3fd3d-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-118">**Type**</span></span>|<span data-ttu-id="3fd3d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3fd3d-120">Решения</span><span class="sxs-lookup"><span data-stu-id="3fd3d-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="3fd3d-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="3fd3d-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3fd3d-122">Хранилище свойств решений, хранимого в документе.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3fd3d-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3fd3d-123">Child elements</span></span>

|<span data-ttu-id="3fd3d-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-124">**Element**</span></span>|<span data-ttu-id="3fd3d-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-125">**Type**</span></span>|<span data-ttu-id="3fd3d-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3fd3d-127">Rel</span><span class="sxs-lookup"><span data-stu-id="3fd3d-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3fd3d-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="3fd3d-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3fd3d-129">Указывает связь с частью с решение, которое XML связанного с решением.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3fd3d-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3fd3d-130">Attributes</span></span>

|<span data-ttu-id="3fd3d-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-131">**Attribute**</span></span>|<span data-ttu-id="3fd3d-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-132">**Type**</span></span>|<span data-ttu-id="3fd3d-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-133">**Required**</span></span>|<span data-ttu-id="3fd3d-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-134">**Description**</span></span>|<span data-ttu-id="3fd3d-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3fd3d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3fd3d-136">Имя</span><span class="sxs-lookup"><span data-stu-id="3fd3d-136">Name</span></span>  <br/> |<span data-ttu-id="3fd3d-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3fd3d-137">xsd:string</span></span>  <br/> |<span data-ttu-id="3fd3d-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3fd3d-138">required</span></span>  <br/> |<span data-ttu-id="3fd3d-139">Имя решения.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="3fd3d-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3fd3d-140">Values of the xsd:string type.</span></span>  <br/> |
   

