---
title: Элемент AutoLinkComparison (DataRecordSet_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Определяет правило, которое сравнивает столбец в родительском элементе DataRecordset с элементом данных фигуры из последнего успешного действия автоматической привязки, выполняемого в пользовательском интерфейсе.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537873"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="09e82-103">Элемент AutoLinkComparison (DataRecordSet_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="09e82-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="09e82-104">Определяет правило, которое сравнивает столбец в родительском элементе **DataRecordset** с элементом данных фигуры из последнего успешного действия автоматической привязки, выполняемого в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="09e82-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="09e82-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="09e82-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09e82-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="09e82-106">**Element type**</span></span> <br/> |[<span data-ttu-id="09e82-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="09e82-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="09e82-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="09e82-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="09e82-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="09e82-109">**Schema file**</span></span> <br/> |<span data-ttu-id="09e82-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="09e82-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="09e82-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="09e82-111">**Document parts**</span></span> <br/> |<span data-ttu-id="09e82-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="09e82-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="09e82-113">Определение</span><span class="sxs-lookup"><span data-stu-id="09e82-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="09e82-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="09e82-114">Elements and attributes</span></span>

<span data-ttu-id="09e82-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="09e82-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="09e82-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="09e82-116">Parent elements</span></span>

|<span data-ttu-id="09e82-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="09e82-117">**Element**</span></span>|<span data-ttu-id="09e82-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="09e82-118">**Type**</span></span>|<span data-ttu-id="09e82-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="09e82-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="09e82-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="09e82-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="09e82-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="09e82-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="09e82-122">Указывает набор записей и привязку данных между этим набором записей и фигурами на страницах рисования.</span><span class="sxs-lookup"><span data-stu-id="09e82-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="09e82-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="09e82-123">Child elements</span></span>

<span data-ttu-id="09e82-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="09e82-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09e82-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="09e82-125">Attributes</span></span>

|<span data-ttu-id="09e82-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="09e82-126">**Attribute**</span></span>|<span data-ttu-id="09e82-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="09e82-127">**Type**</span></span>|<span data-ttu-id="09e82-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="09e82-128">**Required**</span></span>|<span data-ttu-id="09e82-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="09e82-129">**Description**</span></span>|<span data-ttu-id="09e82-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="09e82-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="09e82-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="09e82-131">ColumnName</span></span>  <br/> |<span data-ttu-id="09e82-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09e82-132">xsd:string</span></span>  <br/> |<span data-ttu-id="09e82-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="09e82-133">required</span></span>  <br/> |<span data-ttu-id="09e82-134">Соответствует имени столбца в наборе записей ADO.</span><span class="sxs-lookup"><span data-stu-id="09e82-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="09e82-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="09e82-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="09e82-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="09e82-136">ContextType</span></span>  <br/> |<span data-ttu-id="09e82-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="09e82-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="09e82-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="09e82-138">required</span></span>  <br/> |<span data-ttu-id="09e82-139">Указывает свойства группы или формы для сравнения.</span><span class="sxs-lookup"><span data-stu-id="09e82-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="09e82-140">Возможные значения показаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="09e82-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="09e82-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="09e82-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="09e82-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="09e82-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="09e82-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="09e82-143">xsd:string</span></span>  <br/> |<span data-ttu-id="09e82-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="09e82-144">optional</span></span>  <br/> |<span data-ttu-id="09e82-145">Если значение ContextType — 2 или 3, этот атрибут необходим для определения сравнения.</span><span class="sxs-lookup"><span data-stu-id="09e82-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="09e82-146">Для ContextType = 2 contextTypeLabel должен быть меткой элемента данных фигуры, а если **ContextType** = 3, ContextTypeLabel должен быть локальным названием строки.</span><span class="sxs-lookup"><span data-stu-id="09e82-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="09e82-147">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="09e82-147">Values of the xsd:string type.</span></span>  <br/> |
   

