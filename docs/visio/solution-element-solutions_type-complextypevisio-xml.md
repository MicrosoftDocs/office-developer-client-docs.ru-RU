---
title: Элемент Solution (Солутионс_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Задает один экземпляр XML-файла решения, хранящегося в документе.
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335268"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="e871c-103">Элемент Solution (Солутионс_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="e871c-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e871c-104">Задает один экземпляр XML-файла решения, хранящегося в документе.</span><span class="sxs-lookup"><span data-stu-id="e871c-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e871c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e871c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e871c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e871c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e871c-107">Солутион_типе</span><span class="sxs-lookup"><span data-stu-id="e871c-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e871c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e871c-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e871c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e871c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e871c-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e871c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e871c-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e871c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e871c-112">Solutions. XML</span><span class="sxs-lookup"><span data-stu-id="e871c-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e871c-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e871c-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e871c-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e871c-114">Elements and attributes</span></span>

<span data-ttu-id="e871c-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e871c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e871c-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e871c-116">Parent elements</span></span>

|<span data-ttu-id="e871c-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e871c-117">**Element**</span></span>|<span data-ttu-id="e871c-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e871c-118">**Type**</span></span>|<span data-ttu-id="e871c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e871c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e871c-120">Решения</span><span class="sxs-lookup"><span data-stu-id="e871c-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="e871c-121">Солутионс_типе</span><span class="sxs-lookup"><span data-stu-id="e871c-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e871c-122">Хранит свойства решений, хранящихся в документе.</span><span class="sxs-lookup"><span data-stu-id="e871c-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e871c-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e871c-123">Child elements</span></span>

|<span data-ttu-id="e871c-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e871c-124">**Element**</span></span>|<span data-ttu-id="e871c-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e871c-125">**Type**</span></span>|<span data-ttu-id="e871c-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e871c-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e871c-127">Rel</span><span class="sxs-lookup"><span data-stu-id="e871c-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e871c-128">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="e871c-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e871c-129">Задает отношение к части с XML-ДОКУМЕНТом решения, связанным с этим решением.</span><span class="sxs-lookup"><span data-stu-id="e871c-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e871c-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e871c-130">Attributes</span></span>

|<span data-ttu-id="e871c-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e871c-131">**Attribute**</span></span>|<span data-ttu-id="e871c-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e871c-132">**Type**</span></span>|<span data-ttu-id="e871c-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e871c-133">**Required**</span></span>|<span data-ttu-id="e871c-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e871c-134">**Description**</span></span>|<span data-ttu-id="e871c-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e871c-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e871c-136">Имя</span><span class="sxs-lookup"><span data-stu-id="e871c-136">Name</span></span>  <br/> |<span data-ttu-id="e871c-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e871c-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e871c-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e871c-138">required</span></span>  <br/> |<span data-ttu-id="e871c-139">Имя решения.</span><span class="sxs-lookup"><span data-stu-id="e871c-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="e871c-140">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e871c-140">Values of the xsd:string type.</span></span>  <br/> |
   

