---
title: Элемент rel (Солутион_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Задает отношение к части с XML-документом решения, связанным с этим решением.
ms.openlocfilehash: 1fe48579da28501b74fedd507f3e44d59736ae87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542767"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="d3254-103">Элемент rel (Солутион_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="d3254-103">Rel element (Solution_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="d3254-104">Задает отношение к части с XML-документом решения, связанным с этим решением.</span><span class="sxs-lookup"><span data-stu-id="d3254-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d3254-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d3254-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3254-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d3254-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d3254-107">Рел_типе</span><span class="sxs-lookup"><span data-stu-id="d3254-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d3254-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d3254-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d3254-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d3254-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d3254-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d3254-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d3254-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="d3254-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d3254-112">Pages. XML, Masters. XML, recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="d3254-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d3254-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d3254-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d3254-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d3254-114">Elements and attributes</span></span>

<span data-ttu-id="d3254-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d3254-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d3254-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d3254-116">Parent elements</span></span>

|<span data-ttu-id="d3254-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d3254-117">**Element**</span></span>|<span data-ttu-id="d3254-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d3254-118">**Type**</span></span>|<span data-ttu-id="d3254-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d3254-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d3254-120">Решение</span><span class="sxs-lookup"><span data-stu-id="d3254-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d3254-121">Солутион_типе</span><span class="sxs-lookup"><span data-stu-id="d3254-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d3254-122">Задает один экземпляр XML-файла решения, хранящегося в документе.</span><span class="sxs-lookup"><span data-stu-id="d3254-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d3254-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d3254-123">Child elements</span></span>

<span data-ttu-id="d3254-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="d3254-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d3254-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d3254-125">Attributes</span></span>

|<span data-ttu-id="d3254-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="d3254-126">**Attribute**</span></span>|<span data-ttu-id="d3254-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d3254-127">**Type**</span></span>|<span data-ttu-id="d3254-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="d3254-128">**Required**</span></span>|<span data-ttu-id="d3254-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d3254-129">**Description**</span></span>|<span data-ttu-id="d3254-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="d3254-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d3254-131">р:ИД</span><span class="sxs-lookup"><span data-stu-id="d3254-131">r:id</span></span>  <br/> |<span data-ttu-id="d3254-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="d3254-132">xsd:string</span></span>  <br/> <span data-ttu-id="d3254-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="d3254-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="d3254-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="d3254-134">required</span></span>  <br/> |<span data-ttu-id="d3254-135">Задает отношение к части.</span><span class="sxs-lookup"><span data-stu-id="d3254-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="d3254-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="d3254-136">"rId#"</span></span>  <br/> <span data-ttu-id="d3254-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="d3254-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3254-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3254-138">Remarks</span></span>

<span data-ttu-id="d3254-139">Значение атрибута **р:ИД** должно быть типом **ст_релатионшипид** .</span><span class="sxs-lookup"><span data-stu-id="d3254-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="d3254-140">Тип **ст_релатионшипид** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом.</span><span class="sxs-lookup"><span data-stu-id="d3254-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="d3254-141">Число должно быть уникальным среди всех родственных элементов элемента **rel** .</span><span class="sxs-lookup"><span data-stu-id="d3254-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="d3254-142">Для получения дополнительных сведений о типе Ст_релатионшипид, ознакомьтесь со [спецификацией ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="d3254-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

