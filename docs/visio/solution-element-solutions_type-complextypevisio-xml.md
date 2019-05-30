---
title: Элемент Solution (Солутионс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Задает один экземпляр XML-файла решения, хранящегося в документе.
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540268"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="6b730-103">Элемент Solution (Солутионс_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="6b730-103">Solution element (Solutions_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6b730-104">Задает один экземпляр XML-файла решения, хранящегося в документе.</span><span class="sxs-lookup"><span data-stu-id="6b730-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b730-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6b730-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b730-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6b730-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b730-107">Солутион_типе</span><span class="sxs-lookup"><span data-stu-id="6b730-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b730-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6b730-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b730-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6b730-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b730-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6b730-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b730-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="6b730-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6b730-112">Solutions. XML</span><span class="sxs-lookup"><span data-stu-id="6b730-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b730-113">Определение</span><span class="sxs-lookup"><span data-stu-id="6b730-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b730-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b730-114">Elements and attributes</span></span>

<span data-ttu-id="6b730-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6b730-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b730-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6b730-116">Parent elements</span></span>

|<span data-ttu-id="6b730-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6b730-117">**Element**</span></span>|<span data-ttu-id="6b730-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b730-118">**Type**</span></span>|<span data-ttu-id="6b730-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b730-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b730-120">Решения</span><span class="sxs-lookup"><span data-stu-id="6b730-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="6b730-121">Солутионс_типе</span><span class="sxs-lookup"><span data-stu-id="6b730-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b730-122">Хранит свойства решений, хранящихся в документе.</span><span class="sxs-lookup"><span data-stu-id="6b730-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6b730-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b730-123">Child elements</span></span>

|<span data-ttu-id="6b730-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6b730-124">**Element**</span></span>|<span data-ttu-id="6b730-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b730-125">**Type**</span></span>|<span data-ttu-id="6b730-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b730-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b730-127">Rel</span><span class="sxs-lookup"><span data-stu-id="6b730-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6b730-128">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="6b730-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b730-129">Задает отношение к части с XML-документом решения, связанным с этим решением.</span><span class="sxs-lookup"><span data-stu-id="6b730-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="6b730-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b730-130">Attributes</span></span>

|<span data-ttu-id="6b730-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6b730-131">**Attribute**</span></span>|<span data-ttu-id="6b730-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b730-132">**Type**</span></span>|<span data-ttu-id="6b730-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="6b730-133">**Required**</span></span>|<span data-ttu-id="6b730-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b730-134">**Description**</span></span>|<span data-ttu-id="6b730-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6b730-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b730-136">Имя</span><span class="sxs-lookup"><span data-stu-id="6b730-136">Name</span></span>  <br/> |<span data-ttu-id="6b730-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="6b730-137">xsd:string</span></span>  <br/> |<span data-ttu-id="6b730-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b730-138">required</span></span>  <br/> |<span data-ttu-id="6b730-139">Имя решения.</span><span class="sxs-lookup"><span data-stu-id="6b730-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="6b730-140">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="6b730-140">Values of the xsd:string type.</span></span>  <br/> |
   

