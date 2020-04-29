---
title: Элемент rel (Solution_Type complexType) (XML для Visio)
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
# <a name="rel-element-solution_type-complextype-visio-xml"></a><span data-ttu-id="b0e0a-103">Элемент rel (Solution_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="b0e0a-103">Rel element (Solution_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b0e0a-104">Задает отношение к части с XML-документом решения, связанным с этим решением.</span><span class="sxs-lookup"><span data-stu-id="b0e0a-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b0e0a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b0e0a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b0e0a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b0e0a-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="b0e0a-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b0e0a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b0e0a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b0e0a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b0e0a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b0e0a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b0e0a-112">Pages. XML, Masters. XML, recordsets. XML, Page #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="b0e0a-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b0e0a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b0e0a-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b0e0a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b0e0a-114">Elements and attributes</span></span>

<span data-ttu-id="b0e0a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b0e0a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b0e0a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b0e0a-116">Parent elements</span></span>

|<span data-ttu-id="b0e0a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-117">**Element**</span></span>|<span data-ttu-id="b0e0a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-118">**Type**</span></span>|<span data-ttu-id="b0e0a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b0e0a-120">Решение</span><span class="sxs-lookup"><span data-stu-id="b0e0a-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b0e0a-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="b0e0a-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b0e0a-122">Задает один экземпляр XML-файла решения, хранящегося в документе.</span><span class="sxs-lookup"><span data-stu-id="b0e0a-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b0e0a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b0e0a-123">Child elements</span></span>

<span data-ttu-id="b0e0a-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="b0e0a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b0e0a-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b0e0a-125">Attributes</span></span>

|<span data-ttu-id="b0e0a-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-126">**Attribute**</span></span>|<span data-ttu-id="b0e0a-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-127">**Type**</span></span>|<span data-ttu-id="b0e0a-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-128">**Required**</span></span>|<span data-ttu-id="b0e0a-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-129">**Description**</span></span>|<span data-ttu-id="b0e0a-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b0e0a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b0e0a-131">р:ид</span><span class="sxs-lookup"><span data-stu-id="b0e0a-131">r:id</span></span>  <br/> |<span data-ttu-id="b0e0a-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="b0e0a-132">xsd:string</span></span>  <br/> <span data-ttu-id="b0e0a-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="b0e0a-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="b0e0a-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b0e0a-134">required</span></span>  <br/> |<span data-ttu-id="b0e0a-135">Задает отношение к части.</span><span class="sxs-lookup"><span data-stu-id="b0e0a-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="b0e0a-136">"rId #"</span><span class="sxs-lookup"><span data-stu-id="b0e0a-136">"rId#"</span></span>  <br/> <span data-ttu-id="b0e0a-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="b0e0a-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0e0a-138">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0e0a-138">Remarks</span></span>

<span data-ttu-id="b0e0a-139">Значение атрибута **р:ИД** должно быть типом **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="b0e0a-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="b0e0a-140">Тип **ST_RelationshipID** — это строка, которая должна быть в формате rId #, где конечный символ должен быть числом.</span><span class="sxs-lookup"><span data-stu-id="b0e0a-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="b0e0a-141">Число должно быть уникальным среди всех родственных элементов элемента **rel** .</span><span class="sxs-lookup"><span data-stu-id="b0e0a-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="b0e0a-142">Для получения дополнительных сведений о типе ST_RelationshipID, ознакомьтесь со [спецификацией ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="b0e0a-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

