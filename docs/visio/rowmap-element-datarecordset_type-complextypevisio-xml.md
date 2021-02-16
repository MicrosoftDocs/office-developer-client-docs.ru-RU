---
title: Элемент RowMap (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Сопописывая строка наборов данных с фигурой.
ms.openlocfilehash: 178ceb06d64bfc9ef50f75dd22f8bd94f09f5c33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540772"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="e2c85-103">Элемент RowMap (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e2c85-103">RowMap element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e2c85-104">Сопописывая строка наборов данных с фигурой.</span><span class="sxs-lookup"><span data-stu-id="e2c85-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2c85-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e2c85-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2c85-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e2c85-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e2c85-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="e2c85-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e2c85-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e2c85-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e2c85-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e2c85-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e2c85-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e2c85-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e2c85-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e2c85-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e2c85-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="e2c85-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e2c85-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e2c85-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e2c85-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e2c85-114">Elements and attributes</span></span>

<span data-ttu-id="e2c85-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e2c85-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e2c85-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e2c85-116">Parent elements</span></span>

****

|<span data-ttu-id="e2c85-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e2c85-117">**Element**</span></span>|<span data-ttu-id="e2c85-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e2c85-118">**Type**</span></span>|<span data-ttu-id="e2c85-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2c85-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2c85-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="e2c85-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2c85-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="e2c85-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e2c85-122">Хранит, форматирует, обновляет и предоставляет данные, запрашиваемые из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="e2c85-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2c85-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e2c85-123">Child elements</span></span>

<span data-ttu-id="e2c85-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="e2c85-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2c85-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e2c85-125">Attributes</span></span>

|<span data-ttu-id="e2c85-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e2c85-126">**Attribute**</span></span>|<span data-ttu-id="e2c85-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e2c85-127">**Type**</span></span>|<span data-ttu-id="e2c85-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e2c85-128">**Required**</span></span>|<span data-ttu-id="e2c85-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2c85-129">**Description**</span></span>|<span data-ttu-id="e2c85-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e2c85-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2c85-131">PageID</span><span class="sxs-lookup"><span data-stu-id="e2c85-131">PageID</span></span>  <br/> |<span data-ttu-id="e2c85-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e2c85-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e2c85-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e2c85-133">required</span></span>  <br/> |<span data-ttu-id="e2c85-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span><span class="sxs-lookup"><span data-stu-id="e2c85-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="e2c85-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e2c85-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e2c85-136">RowID</span><span class="sxs-lookup"><span data-stu-id="e2c85-136">RowID</span></span>  <br/> |<span data-ttu-id="e2c85-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e2c85-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e2c85-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e2c85-138">required</span></span>  <br/> |<span data-ttu-id="e2c85-139">Уникальный ИД строки в наборе записей данных.</span><span class="sxs-lookup"><span data-stu-id="e2c85-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="e2c85-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e2c85-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e2c85-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="e2c85-141">ShapeID</span></span>  <br/> |<span data-ttu-id="e2c85-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e2c85-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e2c85-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e2c85-143">required</span></span>  <br/> |<span data-ttu-id="e2c85-144">ИД фигуры, связанной с данными в строке наборов записей данных, заданной **rowID.**</span><span class="sxs-lookup"><span data-stu-id="e2c85-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="e2c85-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e2c85-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

