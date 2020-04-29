---
title: Элемент Рефрешконфликт (DataRecordSet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542837"
---
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="c3524-103">Элемент Рефрешконфликт (DataRecordSet_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="c3524-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c3524-104">Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления набора записей данных.</span><span class="sxs-lookup"><span data-stu-id="c3524-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3524-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c3524-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3524-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c3524-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c3524-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="c3524-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c3524-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c3524-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c3524-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c3524-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c3524-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="c3524-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c3524-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c3524-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c3524-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="c3524-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3524-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c3524-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c3524-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c3524-114">Elements and attributes</span></span>

<span data-ttu-id="c3524-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c3524-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c3524-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c3524-116">Parent elements</span></span>

|<span data-ttu-id="c3524-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c3524-117">**Element**</span></span>|<span data-ttu-id="c3524-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c3524-118">**Type**</span></span>|<span data-ttu-id="c3524-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c3524-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3524-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="c3524-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3524-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="c3524-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3524-122">Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="c3524-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c3524-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c3524-123">Child elements</span></span>

<span data-ttu-id="c3524-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="c3524-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c3524-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c3524-125">Attributes</span></span>

|<span data-ttu-id="c3524-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c3524-126">**Attribute**</span></span>|<span data-ttu-id="c3524-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c3524-127">**Type**</span></span>|<span data-ttu-id="c3524-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c3524-128">**Required**</span></span>|<span data-ttu-id="c3524-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c3524-129">**Description**</span></span>|<span data-ttu-id="c3524-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c3524-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c3524-131">PageID</span><span class="sxs-lookup"><span data-stu-id="c3524-131">PageID</span></span>  <br/> |<span data-ttu-id="c3524-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="c3524-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3524-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c3524-133">required</span></span>  <br/> |<span data-ttu-id="c3524-134">Идентификатор страницы, участвующей в конфликте.</span><span class="sxs-lookup"><span data-stu-id="c3524-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="c3524-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="c3524-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3524-136">RowID</span><span class="sxs-lookup"><span data-stu-id="c3524-136">RowID</span></span>  <br/> |<span data-ttu-id="c3524-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="c3524-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3524-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c3524-138">required</span></span>  <br/> |<span data-ttu-id="c3524-139">После обновления данных идентификатор исходной строки в конфликте.</span><span class="sxs-lookup"><span data-stu-id="c3524-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="c3524-140">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="c3524-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c3524-141">шапеид</span><span class="sxs-lookup"><span data-stu-id="c3524-141">ShapeID</span></span>  <br/> |<span data-ttu-id="c3524-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="c3524-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c3524-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c3524-143">required</span></span>  <br/> |<span data-ttu-id="c3524-144">ИДЕНТИФИКАТОР фигуры, участвующей в конфликте.</span><span class="sxs-lookup"><span data-stu-id="c3524-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="c3524-145">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="c3524-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

