---
title: Элемент RefreshConflict (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Указывает строку в записей данных, связанных с фигурой, который находится в конфликт после обновления набора записей данных.
ms.openlocfilehash: 0bcfb38c1a9ef84fc8581476fcce13b0de32c308
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814547"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="5ab9b-103">Элемент RefreshConflict (DataRecordSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="5ab9b-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="5ab9b-104">Указывает строку в записей данных, связанных с фигурой, который находится в конфликт после обновления набора записей данных.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ab9b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5ab9b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ab9b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5ab9b-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="5ab9b-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5ab9b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5ab9b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5ab9b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="5ab9b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5ab9b-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5ab9b-112">recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="5ab9b-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5ab9b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5ab9b-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5ab9b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5ab9b-114">Elements and attributes</span></span>

<span data-ttu-id="5ab9b-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5ab9b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5ab9b-116">Parent elements</span></span>

|<span data-ttu-id="5ab9b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-117">**Element**</span></span>|<span data-ttu-id="5ab9b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-118">**Type**</span></span>|<span data-ttu-id="5ab9b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5ab9b-120">Записей данных</span><span class="sxs-lookup"><span data-stu-id="5ab9b-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5ab9b-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="5ab9b-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5ab9b-122">Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5ab9b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5ab9b-123">Child elements</span></span>

<span data-ttu-id="5ab9b-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ab9b-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5ab9b-125">Attributes</span></span>

|<span data-ttu-id="5ab9b-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-126">**Attribute**</span></span>|<span data-ttu-id="5ab9b-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-127">**Type**</span></span>|<span data-ttu-id="5ab9b-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-128">**Required**</span></span>|<span data-ttu-id="5ab9b-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-129">**Description**</span></span>|<span data-ttu-id="5ab9b-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5ab9b-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5ab9b-131">PageID</span><span class="sxs-lookup"><span data-stu-id="5ab9b-131">PageID</span></span>  <br/> |<span data-ttu-id="5ab9b-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5ab9b-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5ab9b-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5ab9b-133">required</span></span>  <br/> |<span data-ttu-id="5ab9b-134">Идентификатор страницы фигуры, участвующие в конфликте.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="5ab9b-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5ab9b-136">RowID</span><span class="sxs-lookup"><span data-stu-id="5ab9b-136">RowID</span></span>  <br/> |<span data-ttu-id="5ab9b-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5ab9b-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5ab9b-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5ab9b-138">required</span></span>  <br/> |<span data-ttu-id="5ab9b-139">Исходный идентификатор строки строки теперь в конфликт после обновления данных.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="5ab9b-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="5ab9b-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="5ab9b-141">ShapeID</span></span>  <br/> |<span data-ttu-id="5ab9b-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="5ab9b-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5ab9b-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5ab9b-143">required</span></span>  <br/> |<span data-ttu-id="5ab9b-144">Код фигуры, участвующие в конфликте фигуры.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="5ab9b-145">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="5ab9b-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

