---
title: Элемент Solution (Solutions_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Указывает один экземпляр XML решения, хранимый в документе.
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540268"
---
# <a name="solution-element-solutions_type-complextype-visio-xml"></a><span data-ttu-id="d5f67-103">Элемент Solution (Solutions_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d5f67-103">Solution element (Solutions_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="d5f67-104">Указывает один экземпляр XML решения, хранимый в документе.</span><span class="sxs-lookup"><span data-stu-id="d5f67-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d5f67-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d5f67-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d5f67-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d5f67-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d5f67-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="d5f67-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d5f67-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d5f67-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d5f67-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d5f67-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d5f67-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d5f67-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d5f67-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="d5f67-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d5f67-112">solutions.xml</span><span class="sxs-lookup"><span data-stu-id="d5f67-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d5f67-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d5f67-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d5f67-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d5f67-114">Elements and attributes</span></span>

<span data-ttu-id="d5f67-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d5f67-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d5f67-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d5f67-116">Parent elements</span></span>

|<span data-ttu-id="d5f67-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d5f67-117">**Element**</span></span>|<span data-ttu-id="d5f67-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d5f67-118">**Type**</span></span>|<span data-ttu-id="d5f67-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5f67-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5f67-120">Решения</span><span class="sxs-lookup"><span data-stu-id="d5f67-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="d5f67-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="d5f67-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d5f67-122">Сохраняет свойства решений, хранимых в документе.</span><span class="sxs-lookup"><span data-stu-id="d5f67-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d5f67-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d5f67-123">Child elements</span></span>

|<span data-ttu-id="d5f67-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d5f67-124">**Element**</span></span>|<span data-ttu-id="d5f67-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d5f67-125">**Type**</span></span>|<span data-ttu-id="d5f67-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5f67-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d5f67-127">Rel</span><span class="sxs-lookup"><span data-stu-id="d5f67-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d5f67-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="d5f67-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d5f67-129">Указывает связь с частью с XML-данными решения, связанными с этим решением.</span><span class="sxs-lookup"><span data-stu-id="d5f67-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d5f67-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d5f67-130">Attributes</span></span>

|<span data-ttu-id="d5f67-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d5f67-131">**Attribute**</span></span>|<span data-ttu-id="d5f67-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d5f67-132">**Type**</span></span>|<span data-ttu-id="d5f67-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d5f67-133">**Required**</span></span>|<span data-ttu-id="d5f67-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d5f67-134">**Description**</span></span>|<span data-ttu-id="d5f67-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d5f67-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d5f67-136">Имя</span><span class="sxs-lookup"><span data-stu-id="d5f67-136">Name</span></span>  <br/> |<span data-ttu-id="d5f67-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="d5f67-137">xsd:string</span></span>  <br/> |<span data-ttu-id="d5f67-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d5f67-138">required</span></span>  <br/> |<span data-ttu-id="d5f67-139">Имя решения.</span><span class="sxs-lookup"><span data-stu-id="d5f67-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="d5f67-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="d5f67-140">Values of the xsd:string type.</span></span>  <br/> |
   

