---
title: Элемент AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Определяет правило, которое сравнивает столбец в родительском элементе DataRecordset с элементом данных фигуры из последнего успешного действия автоматического связывания, выполненного в пользовательском интерфейсе.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537873"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="95c40-103">Элемент AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="95c40-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="95c40-104">Определяет правило, которое сравнивает столбец в родительском элементе **DataRecordset** с элементом данных фигуры из последнего успешного действия автоматического связывания, выполненного в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="95c40-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="95c40-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="95c40-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95c40-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="95c40-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95c40-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="95c40-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95c40-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="95c40-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95c40-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="95c40-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95c40-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="95c40-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95c40-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="95c40-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95c40-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="95c40-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95c40-113">Определение</span><span class="sxs-lookup"><span data-stu-id="95c40-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95c40-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="95c40-114">Elements and attributes</span></span>

<span data-ttu-id="95c40-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="95c40-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95c40-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="95c40-116">Parent elements</span></span>

|<span data-ttu-id="95c40-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="95c40-117">**Element**</span></span>|<span data-ttu-id="95c40-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="95c40-118">**Type**</span></span>|<span data-ttu-id="95c40-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95c40-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95c40-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="95c40-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95c40-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="95c40-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95c40-122">Указывает набор записей и привязку данных между этим набором записей и фигурами на страницах рисования.</span><span class="sxs-lookup"><span data-stu-id="95c40-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95c40-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="95c40-123">Child elements</span></span>

<span data-ttu-id="95c40-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="95c40-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="95c40-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="95c40-125">Attributes</span></span>

|<span data-ttu-id="95c40-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="95c40-126">**Attribute**</span></span>|<span data-ttu-id="95c40-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="95c40-127">**Type**</span></span>|<span data-ttu-id="95c40-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="95c40-128">**Required**</span></span>|<span data-ttu-id="95c40-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95c40-129">**Description**</span></span>|<span data-ttu-id="95c40-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="95c40-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95c40-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="95c40-131">ColumnName</span></span>  <br/> |<span data-ttu-id="95c40-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="95c40-132">xsd:string</span></span>  <br/> |<span data-ttu-id="95c40-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="95c40-133">required</span></span>  <br/> |<span data-ttu-id="95c40-134">Соответствует имени столбца в наборе записей ADO.</span><span class="sxs-lookup"><span data-stu-id="95c40-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="95c40-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="95c40-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="95c40-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="95c40-136">ContextType</span></span>  <br/> |<span data-ttu-id="95c40-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="95c40-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="95c40-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="95c40-138">required</span></span>  <br/> |<span data-ttu-id="95c40-139">Указывает свойства группы или фигуры, которые необходимо использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="95c40-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="95c40-140">Возможные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="95c40-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="95c40-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="95c40-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="95c40-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="95c40-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="95c40-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="95c40-143">xsd:string</span></span>  <br/> |<span data-ttu-id="95c40-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="95c40-144">optional</span></span>  <br/> |<span data-ttu-id="95c40-145">Если значение ContextType — 2 или 3, этот атрибут необходим для определения сравнения.</span><span class="sxs-lookup"><span data-stu-id="95c40-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="95c40-146">Для ContextType = 2 ContextTypeLabel должен быть меткой элемента данных фигуры, а если **ContextType** = 3, ContextTypeLabel должен быть локальным именем строки.</span><span class="sxs-lookup"><span data-stu-id="95c40-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="95c40-147">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="95c40-147">Values of the xsd:string type.</span></span>  <br/> |
   

