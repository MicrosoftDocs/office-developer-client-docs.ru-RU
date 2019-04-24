---
title: Элемент Рефрешконфликт (Датарекордсет_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360139"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="03bc9-103">Элемент Рефрешконфликт (Датарекордсет_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="03bc9-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="03bc9-104">Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.</span><span class="sxs-lookup"><span data-stu-id="03bc9-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="03bc9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="03bc9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="03bc9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="03bc9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="03bc9-107">Рефрешконфликт_типе</span><span class="sxs-lookup"><span data-stu-id="03bc9-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="03bc9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="03bc9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="03bc9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="03bc9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="03bc9-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="03bc9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="03bc9-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="03bc9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="03bc9-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="03bc9-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="03bc9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="03bc9-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="03bc9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="03bc9-114">Elements and attributes</span></span>

<span data-ttu-id="03bc9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="03bc9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="03bc9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="03bc9-116">Parent elements</span></span>

|<span data-ttu-id="03bc9-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="03bc9-117">**Element**</span></span>|<span data-ttu-id="03bc9-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="03bc9-118">**Type**</span></span>|<span data-ttu-id="03bc9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="03bc9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="03bc9-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="03bc9-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="03bc9-121">Датарекордсет_типе</span><span class="sxs-lookup"><span data-stu-id="03bc9-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="03bc9-122">Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="03bc9-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="03bc9-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="03bc9-123">Child elements</span></span>

<span data-ttu-id="03bc9-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="03bc9-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="03bc9-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="03bc9-125">Attributes</span></span>

|<span data-ttu-id="03bc9-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="03bc9-126">**Attribute**</span></span>|<span data-ttu-id="03bc9-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="03bc9-127">**Type**</span></span>|<span data-ttu-id="03bc9-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="03bc9-128">**Required**</span></span>|<span data-ttu-id="03bc9-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="03bc9-129">**Description**</span></span>|<span data-ttu-id="03bc9-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="03bc9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="03bc9-131">PageID</span><span class="sxs-lookup"><span data-stu-id="03bc9-131">PageID</span></span>  <br/> |<span data-ttu-id="03bc9-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="03bc9-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03bc9-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="03bc9-133">required</span></span>  <br/> |<span data-ttu-id="03bc9-134">Идентификатор страницы, участвующей в конфликте.</span><span class="sxs-lookup"><span data-stu-id="03bc9-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="03bc9-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="03bc9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="03bc9-136">RowID</span><span class="sxs-lookup"><span data-stu-id="03bc9-136">RowID</span></span>  <br/> |<span data-ttu-id="03bc9-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="03bc9-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03bc9-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="03bc9-138">required</span></span>  <br/> |<span data-ttu-id="03bc9-139">После обновления данных идентификатор исходной строки в конфликте.</span><span class="sxs-lookup"><span data-stu-id="03bc9-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="03bc9-140">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="03bc9-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="03bc9-141">Шапеид</span><span class="sxs-lookup"><span data-stu-id="03bc9-141">ShapeID</span></span>  <br/> |<span data-ttu-id="03bc9-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="03bc9-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="03bc9-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="03bc9-143">required</span></span>  <br/> |<span data-ttu-id="03bc9-144">ИДЕНТИФИКАТОР фигуры, участвующей в конфликте.</span><span class="sxs-lookup"><span data-stu-id="03bc9-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="03bc9-145">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="03bc9-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

