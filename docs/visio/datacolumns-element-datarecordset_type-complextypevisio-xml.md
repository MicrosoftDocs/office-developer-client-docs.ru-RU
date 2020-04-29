---
title: Элемент DataColumns (DataRecordSet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Содержит все элементы DataColumn в наборе данных данных.
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541199"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="8116f-103">Элемент DataColumns (DataRecordSet_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8116f-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8116f-104">Содержит все элементы **DataColumn** в наборе данных данных.</span><span class="sxs-lookup"><span data-stu-id="8116f-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8116f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8116f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8116f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="8116f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8116f-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="8116f-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8116f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8116f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8116f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8116f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8116f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8116f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8116f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="8116f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8116f-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="8116f-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8116f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="8116f-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8116f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8116f-114">Elements and attributes</span></span>

<span data-ttu-id="8116f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8116f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8116f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8116f-116">Parent elements</span></span>

|<span data-ttu-id="8116f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8116f-117">**Element**</span></span>|<span data-ttu-id="8116f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8116f-118">**Type**</span></span>|<span data-ttu-id="8116f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8116f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8116f-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="8116f-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8116f-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="8116f-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8116f-122">Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="8116f-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8116f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8116f-123">Child elements</span></span>

|<span data-ttu-id="8116f-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8116f-124">**Element**</span></span>|<span data-ttu-id="8116f-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8116f-125">**Type**</span></span>|<span data-ttu-id="8116f-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8116f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8116f-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="8116f-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8116f-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="8116f-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8116f-129">Определяет, как столбец данных отображается в окне " **Внешние данные** " в пользовательском интерфейсе Visio, и определяет данные в столбце, определяя тип данных и форматирование.</span><span class="sxs-lookup"><span data-stu-id="8116f-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8116f-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8116f-130">Attributes</span></span>

|<span data-ttu-id="8116f-131">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8116f-131">**Attribute**</span></span>|<span data-ttu-id="8116f-132">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8116f-132">**Type**</span></span>|<span data-ttu-id="8116f-133">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8116f-133">**Required**</span></span>|<span data-ttu-id="8116f-134">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8116f-134">**Description**</span></span>|<span data-ttu-id="8116f-135">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8116f-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8116f-136">сортаск</span><span class="sxs-lookup"><span data-stu-id="8116f-136">SortAsc</span></span>  <br/> |<span data-ttu-id="8116f-137">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="8116f-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="8116f-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="8116f-138">optional</span></span>  <br/> |<span data-ttu-id="8116f-139">Столбец, по которому необходимо отсортировать данные.</span><span class="sxs-lookup"><span data-stu-id="8116f-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="8116f-140">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="8116f-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="8116f-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="8116f-141">SortColumn</span></span>  <br/> |<span data-ttu-id="8116f-142">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="8116f-142">xsd:string</span></span>  <br/> |<span data-ttu-id="8116f-143">необязательный</span><span class="sxs-lookup"><span data-stu-id="8116f-143">optional</span></span>  <br/> |<span data-ttu-id="8116f-144">Следует ли сортировать столбец **sortColumn** в порядке возрастания (1) или убыванию (0).</span><span class="sxs-lookup"><span data-stu-id="8116f-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="8116f-145">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="8116f-145">Values of the xsd:string type.</span></span>  <br/> |
   

