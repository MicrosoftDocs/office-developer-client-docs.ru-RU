---
title: Элемент RowMap (DataRecordSet_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Карты строку с набором данных в форму.
ms.openlocfilehash: 178ceb06d64bfc9ef50f75dd22f8bd94f09f5c33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540772"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="63be2-103">Элемент RowMap (DataRecordSet_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="63be2-103">RowMap element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="63be2-104">Карты строку с набором данных в форму.</span><span class="sxs-lookup"><span data-stu-id="63be2-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63be2-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="63be2-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63be2-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="63be2-106">**Element type**</span></span> <br/> |[<span data-ttu-id="63be2-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="63be2-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="63be2-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="63be2-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="63be2-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="63be2-109">**Schema file**</span></span> <br/> |<span data-ttu-id="63be2-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="63be2-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="63be2-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="63be2-111">**Document parts**</span></span> <br/> |<span data-ttu-id="63be2-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="63be2-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="63be2-113">Определение</span><span class="sxs-lookup"><span data-stu-id="63be2-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="63be2-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="63be2-114">Elements and attributes</span></span>

<span data-ttu-id="63be2-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="63be2-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="63be2-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="63be2-116">Parent elements</span></span>

****

|<span data-ttu-id="63be2-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="63be2-117">**Element**</span></span>|<span data-ttu-id="63be2-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="63be2-118">**Type**</span></span>|<span data-ttu-id="63be2-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="63be2-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="63be2-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="63be2-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="63be2-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="63be2-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="63be2-122">Магазины, форматы, обновления и доступ к данным, запрашиваемой из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="63be2-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="63be2-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="63be2-123">Child elements</span></span>

<span data-ttu-id="63be2-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="63be2-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63be2-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="63be2-125">Attributes</span></span>

|<span data-ttu-id="63be2-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="63be2-126">**Attribute**</span></span>|<span data-ttu-id="63be2-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="63be2-127">**Type**</span></span>|<span data-ttu-id="63be2-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="63be2-128">**Required**</span></span>|<span data-ttu-id="63be2-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="63be2-129">**Description**</span></span>|<span data-ttu-id="63be2-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="63be2-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="63be2-131">PageID</span><span class="sxs-lookup"><span data-stu-id="63be2-131">PageID</span></span>  <br/> |<span data-ttu-id="63be2-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="63be2-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63be2-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="63be2-133">required</span></span>  <br/> |<span data-ttu-id="63be2-134">Page ID формы, связанной с данными в строке data-recordset, идентифицированной **RowID**.</span><span class="sxs-lookup"><span data-stu-id="63be2-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="63be2-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="63be2-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="63be2-136">RowID</span><span class="sxs-lookup"><span data-stu-id="63be2-136">RowID</span></span>  <br/> |<span data-ttu-id="63be2-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="63be2-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63be2-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="63be2-138">required</span></span>  <br/> |<span data-ttu-id="63be2-139">Строка ID строки, уникальная в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="63be2-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="63be2-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="63be2-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="63be2-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="63be2-141">ShapeID</span></span>  <br/> |<span data-ttu-id="63be2-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="63be2-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="63be2-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="63be2-143">required</span></span>  <br/> |<span data-ttu-id="63be2-144">Форма ID фигуры, связанной с данными в строке data-recordset, идентифицированной **RowID.**</span><span class="sxs-lookup"><span data-stu-id="63be2-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="63be2-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="63be2-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

