---
title: Элемент RowMap (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Сопоставление строк набора записей данных фигуры.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385314"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="eb6a3-103">Элемент RowMap (DataRecordSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="eb6a3-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="eb6a3-104">Сопоставление строк набора записей данных фигуры.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="eb6a3-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="eb6a3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb6a3-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="eb6a3-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="eb6a3-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="eb6a3-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="eb6a3-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="eb6a3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="eb6a3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="eb6a3-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="eb6a3-112">recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="eb6a3-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eb6a3-113">Определение</span><span class="sxs-lookup"><span data-stu-id="eb6a3-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eb6a3-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="eb6a3-114">Elements and attributes</span></span>

<span data-ttu-id="eb6a3-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="eb6a3-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="eb6a3-116">Parent elements</span></span>

****

|<span data-ttu-id="eb6a3-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-117">**Element**</span></span>|<span data-ttu-id="eb6a3-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-118">**Type**</span></span>|<span data-ttu-id="eb6a3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="eb6a3-120">Записей данных</span><span class="sxs-lookup"><span data-stu-id="eb6a3-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="eb6a3-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="eb6a3-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="eb6a3-122">Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="eb6a3-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="eb6a3-123">Child elements</span></span>

<span data-ttu-id="eb6a3-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb6a3-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="eb6a3-125">Attributes</span></span>

|<span data-ttu-id="eb6a3-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-126">**Attribute**</span></span>|<span data-ttu-id="eb6a3-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-127">**Type**</span></span>|<span data-ttu-id="eb6a3-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-128">**Required**</span></span>|<span data-ttu-id="eb6a3-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-129">**Description**</span></span>|<span data-ttu-id="eb6a3-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="eb6a3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eb6a3-131">PageID</span><span class="sxs-lookup"><span data-stu-id="eb6a3-131">PageID</span></span>  <br/> |<span data-ttu-id="eb6a3-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb6a3-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb6a3-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eb6a3-133">required</span></span>  <br/> |<span data-ttu-id="eb6a3-134">Идентификатор страницы фигуры, связанная с данными в строки набора записей данных, **RowID**.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="eb6a3-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eb6a3-136">RowID</span><span class="sxs-lookup"><span data-stu-id="eb6a3-136">RowID</span></span>  <br/> |<span data-ttu-id="eb6a3-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb6a3-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb6a3-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eb6a3-138">required</span></span>  <br/> |<span data-ttu-id="eb6a3-139">Идентификатор строки строки, уникальных в пределах набора данных.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="eb6a3-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eb6a3-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="eb6a3-141">ShapeID</span></span>  <br/> |<span data-ttu-id="eb6a3-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb6a3-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb6a3-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="eb6a3-143">required</span></span>  <br/> |<span data-ttu-id="eb6a3-144">Код фигуры фигуры, связанная с данными в строки набора записей данных, **RowID**.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="eb6a3-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb6a3-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

