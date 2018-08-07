---
title: Элемент объектам DataColumn (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Содержит все элементы DataColumn в записей данных.
ms.openlocfilehash: b90b6cb18fc2bd1edc393d58a9d761cfb36ea220
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813537"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="3971e-103">Элемент объектам DataColumn (DataRecordSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="3971e-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3971e-104">Содержит все элементы **DataColumn** в записей данных.</span><span class="sxs-lookup"><span data-stu-id="3971e-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3971e-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3971e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3971e-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3971e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3971e-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="3971e-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3971e-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3971e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3971e-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3971e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3971e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3971e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3971e-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3971e-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3971e-112">recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="3971e-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3971e-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3971e-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3971e-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3971e-114">Elements and attributes</span></span>

<span data-ttu-id="3971e-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="3971e-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3971e-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3971e-116">Parent elements</span></span>

|<span data-ttu-id="3971e-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3971e-117">**Element**</span></span>|<span data-ttu-id="3971e-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3971e-118">**Type**</span></span>|<span data-ttu-id="3971e-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3971e-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3971e-120">Записей данных</span><span class="sxs-lookup"><span data-stu-id="3971e-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3971e-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="3971e-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3971e-122">Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="3971e-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3971e-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3971e-123">Child elements</span></span>

|<span data-ttu-id="3971e-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3971e-124">**Element**</span></span>|<span data-ttu-id="3971e-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3971e-125">**Type**</span></span>|<span data-ttu-id="3971e-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3971e-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3971e-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="3971e-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3971e-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="3971e-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3971e-129">Определяет, как столбец данных отображается в окне **Внешних данных** в пользовательском интерфейсе Visio и определяет данные в столбце путем определения его типа данных и форматирования.</span><span class="sxs-lookup"><span data-stu-id="3971e-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3971e-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3971e-130">Attributes</span></span>

|<span data-ttu-id="3971e-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3971e-131">**Attribute**</span></span>|<span data-ttu-id="3971e-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3971e-132">**Type**</span></span>|<span data-ttu-id="3971e-133">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="3971e-133">**Required**</span></span>|<span data-ttu-id="3971e-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3971e-134">**Description**</span></span>|<span data-ttu-id="3971e-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3971e-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3971e-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="3971e-136">SortAsc</span></span>  <br/> |<span data-ttu-id="3971e-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="3971e-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3971e-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="3971e-138">optional</span></span>  <br/> |<span data-ttu-id="3971e-139">Столбец, по которому выполняется сортировка данных.</span><span class="sxs-lookup"><span data-stu-id="3971e-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="3971e-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3971e-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3971e-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="3971e-141">SortColumn</span></span>  <br/> |<span data-ttu-id="3971e-142">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3971e-142">xsd:string</span></span>  <br/> |<span data-ttu-id="3971e-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="3971e-143">optional</span></span>  <br/> |<span data-ttu-id="3971e-144">Требуется ли для сортировки столбца **SortColumn** в порядке возрастания (1) или убыванию (0).</span><span class="sxs-lookup"><span data-stu-id="3971e-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="3971e-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3971e-145">Values of the xsd:string type.</span></span>  <br/> |
   

