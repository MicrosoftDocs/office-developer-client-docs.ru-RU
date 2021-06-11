---
title: Элемент DataColumns (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Содержит все элементы DataColumn в наборе данных.
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541199"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="aba1a-103">Элемент DataColumns (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="aba1a-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="aba1a-104">Содержит все **элементы DataColumn** в наборе данных.</span><span class="sxs-lookup"><span data-stu-id="aba1a-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="aba1a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="aba1a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aba1a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="aba1a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="aba1a-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="aba1a-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="aba1a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="aba1a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="aba1a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="aba1a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="aba1a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="aba1a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="aba1a-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="aba1a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="aba1a-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="aba1a-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aba1a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="aba1a-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aba1a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="aba1a-114">Elements and attributes</span></span>

<span data-ttu-id="aba1a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="aba1a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="aba1a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="aba1a-116">Parent elements</span></span>

|<span data-ttu-id="aba1a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="aba1a-117">**Element**</span></span>|<span data-ttu-id="aba1a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="aba1a-118">**Type**</span></span>|<span data-ttu-id="aba1a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aba1a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aba1a-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="aba1a-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aba1a-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="aba1a-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aba1a-122">Магазины, форматы, обновления и доступ к данным, запрашиваемой из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="aba1a-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="aba1a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aba1a-123">Child elements</span></span>

|<span data-ttu-id="aba1a-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="aba1a-124">**Element**</span></span>|<span data-ttu-id="aba1a-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="aba1a-125">**Type**</span></span>|<span data-ttu-id="aba1a-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aba1a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aba1a-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="aba1a-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aba1a-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="aba1a-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aba1a-129">Определяет, как столбец данных  отображается в окне внешних данных в пользовательском интерфейсе Visio и квалифицирует данные в столбце, определяя его тип данных и форматирование.</span><span class="sxs-lookup"><span data-stu-id="aba1a-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="aba1a-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="aba1a-130">Attributes</span></span>

|<span data-ttu-id="aba1a-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="aba1a-131">**Attribute**</span></span>|<span data-ttu-id="aba1a-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="aba1a-132">**Type**</span></span>|<span data-ttu-id="aba1a-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="aba1a-133">**Required**</span></span>|<span data-ttu-id="aba1a-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aba1a-134">**Description**</span></span>|<span data-ttu-id="aba1a-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="aba1a-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="aba1a-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="aba1a-136">SortAsc</span></span>  <br/> |<span data-ttu-id="aba1a-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="aba1a-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="aba1a-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="aba1a-138">optional</span></span>  <br/> |<span data-ttu-id="aba1a-139">Столбец, на котором сортировать данные.</span><span class="sxs-lookup"><span data-stu-id="aba1a-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="aba1a-140">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="aba1a-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="aba1a-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="aba1a-141">SortColumn</span></span>  <br/> |<span data-ttu-id="aba1a-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="aba1a-142">xsd:string</span></span>  <br/> |<span data-ttu-id="aba1a-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="aba1a-143">optional</span></span>  <br/> |<span data-ttu-id="aba1a-144">Следует ли сортировать **столбец SortColumn** в порядке по возрастанию (1) или по убыванию (0).</span><span class="sxs-lookup"><span data-stu-id="aba1a-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="aba1a-145">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="aba1a-145">Values of the xsd:string type.</span></span>  <br/> |
   

