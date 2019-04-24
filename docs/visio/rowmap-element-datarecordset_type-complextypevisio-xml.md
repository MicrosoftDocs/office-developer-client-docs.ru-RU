---
title: Элемент Ровмап (Датарекордсет_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Сопоставляет строку набора записей данных с фигурой.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332517"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="01350-103">Элемент Ровмап (Датарекордсет_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="01350-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="01350-104">Сопоставляет строку набора записей данных с фигурой.</span><span class="sxs-lookup"><span data-stu-id="01350-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01350-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="01350-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01350-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="01350-106">**Element type**</span></span> <br/> |[<span data-ttu-id="01350-107">Ровмап_типе</span><span class="sxs-lookup"><span data-stu-id="01350-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="01350-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="01350-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="01350-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="01350-109">**Schema file**</span></span> <br/> |<span data-ttu-id="01350-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="01350-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="01350-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="01350-111">**Document parts**</span></span> <br/> |<span data-ttu-id="01350-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="01350-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="01350-113">Определение</span><span class="sxs-lookup"><span data-stu-id="01350-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="01350-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="01350-114">Elements and attributes</span></span>

<span data-ttu-id="01350-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="01350-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="01350-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="01350-116">Parent elements</span></span>

****

|<span data-ttu-id="01350-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="01350-117">**Element**</span></span>|<span data-ttu-id="01350-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="01350-118">**Type**</span></span>|<span data-ttu-id="01350-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01350-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="01350-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="01350-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="01350-121">Датарекордсет_типе</span><span class="sxs-lookup"><span data-stu-id="01350-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="01350-122">Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="01350-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="01350-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="01350-123">Child elements</span></span>

<span data-ttu-id="01350-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="01350-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01350-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="01350-125">Attributes</span></span>

|<span data-ttu-id="01350-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="01350-126">**Attribute**</span></span>|<span data-ttu-id="01350-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="01350-127">**Type**</span></span>|<span data-ttu-id="01350-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="01350-128">**Required**</span></span>|<span data-ttu-id="01350-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="01350-129">**Description**</span></span>|<span data-ttu-id="01350-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="01350-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="01350-131">PageID</span><span class="sxs-lookup"><span data-stu-id="01350-131">PageID</span></span>  <br/> |<span data-ttu-id="01350-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="01350-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01350-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01350-133">required</span></span>  <br/> |<span data-ttu-id="01350-134">Идентификатор страницы, связанной с данными в строке набора записей данных, определяемой **ROWID**.</span><span class="sxs-lookup"><span data-stu-id="01350-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="01350-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="01350-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01350-136">RowID</span><span class="sxs-lookup"><span data-stu-id="01350-136">RowID</span></span>  <br/> |<span data-ttu-id="01350-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="01350-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01350-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01350-138">required</span></span>  <br/> |<span data-ttu-id="01350-139">Идентификатор строки, уникальный в пределах набора данных.</span><span class="sxs-lookup"><span data-stu-id="01350-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="01350-140">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="01350-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="01350-141">Шапеид</span><span class="sxs-lookup"><span data-stu-id="01350-141">ShapeID</span></span>  <br/> |<span data-ttu-id="01350-142">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="01350-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="01350-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="01350-143">required</span></span>  <br/> |<span data-ttu-id="01350-144">ИДЕНТИФИКАТОР фигуры для фигуры, связанной с данными в строке набора записей Data, которая указана в **ROWID**.</span><span class="sxs-lookup"><span data-stu-id="01350-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="01350-145">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="01350-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

