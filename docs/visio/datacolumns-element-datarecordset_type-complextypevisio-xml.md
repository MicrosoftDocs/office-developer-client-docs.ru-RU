---
title: Элемент объектам DataColumn (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Содержит все элементы DataColumn в записей данных.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382521"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="66e29-103">Элемент объектам DataColumn (DataRecordSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="66e29-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="66e29-104">Содержит все элементы **DataColumn** в записей данных.</span><span class="sxs-lookup"><span data-stu-id="66e29-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="66e29-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="66e29-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66e29-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="66e29-106">**Element type**</span></span> <br/> |[<span data-ttu-id="66e29-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="66e29-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="66e29-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="66e29-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="66e29-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="66e29-109">**Schema file**</span></span> <br/> |<span data-ttu-id="66e29-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="66e29-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="66e29-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="66e29-111">**Document parts**</span></span> <br/> |<span data-ttu-id="66e29-112">recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="66e29-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="66e29-113">Определение</span><span class="sxs-lookup"><span data-stu-id="66e29-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="66e29-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="66e29-114">Elements and attributes</span></span>

<span data-ttu-id="66e29-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="66e29-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="66e29-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="66e29-116">Parent elements</span></span>

|<span data-ttu-id="66e29-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="66e29-117">**Element**</span></span>|<span data-ttu-id="66e29-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="66e29-118">**Type**</span></span>|<span data-ttu-id="66e29-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66e29-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66e29-120">Записей данных</span><span class="sxs-lookup"><span data-stu-id="66e29-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66e29-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="66e29-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66e29-122">Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="66e29-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="66e29-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="66e29-123">Child elements</span></span>

|<span data-ttu-id="66e29-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="66e29-124">**Element**</span></span>|<span data-ttu-id="66e29-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="66e29-125">**Type**</span></span>|<span data-ttu-id="66e29-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66e29-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="66e29-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="66e29-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="66e29-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="66e29-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="66e29-129">Определяет, как столбец данных отображается в окне **Внешних данных** в пользовательском интерфейсе Visio и определяет данные в столбце путем определения его типа данных и форматирования.</span><span class="sxs-lookup"><span data-stu-id="66e29-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="66e29-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="66e29-130">Attributes</span></span>

|<span data-ttu-id="66e29-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="66e29-131">**Attribute**</span></span>|<span data-ttu-id="66e29-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="66e29-132">**Type**</span></span>|<span data-ttu-id="66e29-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="66e29-133">**Required**</span></span>|<span data-ttu-id="66e29-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="66e29-134">**Description**</span></span>|<span data-ttu-id="66e29-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="66e29-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="66e29-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="66e29-136">SortAsc</span></span>  <br/> |<span data-ttu-id="66e29-137">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="66e29-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="66e29-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="66e29-138">optional</span></span>  <br/> |<span data-ttu-id="66e29-139">Столбец, по которому выполняется сортировка данных.</span><span class="sxs-lookup"><span data-stu-id="66e29-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="66e29-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="66e29-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="66e29-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="66e29-141">SortColumn</span></span>  <br/> |<span data-ttu-id="66e29-142">XSD:String</span><span class="sxs-lookup"><span data-stu-id="66e29-142">xsd:string</span></span>  <br/> |<span data-ttu-id="66e29-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="66e29-143">optional</span></span>  <br/> |<span data-ttu-id="66e29-144">Требуется ли для сортировки столбца **SortColumn** в порядке возрастания (1) или убыванию (0).</span><span class="sxs-lookup"><span data-stu-id="66e29-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="66e29-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="66e29-145">Values of the xsd:string type.</span></span>  <br/> |
   

