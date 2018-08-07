---
title: Элемент Rel (Solution_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Указывает связь с частью с решение, которое XML связанного с решением.
ms.openlocfilehash: 59d9db3f7e0897abf278a27229c07fd3942cee79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814550"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="cf0f9-103">Элемент Rel (Solution_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="cf0f9-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cf0f9-104">Указывает связь с частью с решение, которое XML связанного с решением.</span><span class="sxs-lookup"><span data-stu-id="cf0f9-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cf0f9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cf0f9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cf0f9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cf0f9-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="cf0f9-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cf0f9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cf0f9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cf0f9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cf0f9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cf0f9-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cf0f9-112">Pages.XML, masters.xml, recordsets.xml, страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="cf0f9-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cf0f9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="cf0f9-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cf0f9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="cf0f9-114">Elements and attributes</span></span>

<span data-ttu-id="cf0f9-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="cf0f9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cf0f9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="cf0f9-116">Parent elements</span></span>

|<span data-ttu-id="cf0f9-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-117">**Element**</span></span>|<span data-ttu-id="cf0f9-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-118">**Type**</span></span>|<span data-ttu-id="cf0f9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cf0f9-120">Решение</span><span class="sxs-lookup"><span data-stu-id="cf0f9-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cf0f9-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="cf0f9-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cf0f9-122">Задает один экземпляр решение, которое XML хранятся в документе.</span><span class="sxs-lookup"><span data-stu-id="cf0f9-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cf0f9-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cf0f9-123">Child elements</span></span>

<span data-ttu-id="cf0f9-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="cf0f9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cf0f9-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cf0f9-125">Attributes</span></span>

|<span data-ttu-id="cf0f9-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-126">**Attribute**</span></span>|<span data-ttu-id="cf0f9-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-127">**Type**</span></span>|<span data-ttu-id="cf0f9-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-128">**Required**</span></span>|<span data-ttu-id="cf0f9-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-129">**Description**</span></span>|<span data-ttu-id="cf0f9-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="cf0f9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cf0f9-131">r: код</span><span class="sxs-lookup"><span data-stu-id="cf0f9-131">r:id</span></span>  <br/> |<span data-ttu-id="cf0f9-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="cf0f9-132">xsd:string</span></span>  <br/> <span data-ttu-id="cf0f9-133">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="cf0f9-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="cf0f9-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cf0f9-134">required</span></span>  <br/> |<span data-ttu-id="cf0f9-135">Указывает связь с частью.</span><span class="sxs-lookup"><span data-stu-id="cf0f9-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="cf0f9-136">«Удалить #»</span><span class="sxs-lookup"><span data-stu-id="cf0f9-136">"rId#"</span></span>  <br/> <span data-ttu-id="cf0f9-137">См. раздел "Замечания".</span><span class="sxs-lookup"><span data-stu-id="cf0f9-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf0f9-138">Замечания</span><span class="sxs-lookup"><span data-stu-id="cf0f9-138">Remarks</span></span>

<span data-ttu-id="cf0f9-139">Значение атрибута **r: id** должен быть указан тип **простом типе ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="cf0f9-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="cf0f9-140">Тип **простом типе ST_RelationshipID** — это строка, которая должна быть в формате «избавиться #», где последний символ, должно быть числом.</span><span class="sxs-lookup"><span data-stu-id="cf0f9-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="cf0f9-141">Номер должен быть уникальным во все элементы одного уровня элемента **Rel** .</span><span class="sxs-lookup"><span data-stu-id="cf0f9-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="cf0f9-142">Дополнительные сведения о типе простом типе ST_RelationshipID можно найти в [спецификации ISO/IEC 29500 часть 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="cf0f9-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

