---
title: Элемент Аутолинккомпарисон (Датарекордсет_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Определяет правило, которое сравнивает столбец в родительском элементе данных фигуры с элементом данных фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338320"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="a051a-103">Элемент Аутолинккомпарисон (Датарекордсет_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="a051a-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="a051a-104">Определяет правило, которое сравнивает столбец в родительском элементе данных \*\*\*\* фигуры с элементом данных фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="a051a-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a051a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a051a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a051a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a051a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a051a-107">Аутолинккомпарисон_типе</span><span class="sxs-lookup"><span data-stu-id="a051a-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a051a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a051a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a051a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a051a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a051a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="a051a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a051a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="a051a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a051a-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="a051a-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a051a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="a051a-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a051a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a051a-114">Elements and attributes</span></span>

<span data-ttu-id="a051a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a051a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a051a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a051a-116">Parent elements</span></span>

|<span data-ttu-id="a051a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a051a-117">**Element**</span></span>|<span data-ttu-id="a051a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a051a-118">**Type**</span></span>|<span data-ttu-id="a051a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a051a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a051a-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="a051a-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a051a-121">Датарекордсет_типе</span><span class="sxs-lookup"><span data-stu-id="a051a-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a051a-122">Задает набор записей и привязку данных между этим набором записей и фигурами на страницах документа.</span><span class="sxs-lookup"><span data-stu-id="a051a-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a051a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a051a-123">Child elements</span></span>

<span data-ttu-id="a051a-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="a051a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a051a-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a051a-125">Attributes</span></span>

|<span data-ttu-id="a051a-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a051a-126">**Attribute**</span></span>|<span data-ttu-id="a051a-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a051a-127">**Type**</span></span>|<span data-ttu-id="a051a-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a051a-128">**Required**</span></span>|<span data-ttu-id="a051a-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a051a-129">**Description**</span></span>|<span data-ttu-id="a051a-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a051a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a051a-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="a051a-131">ColumnName</span></span>  <br/> |<span data-ttu-id="a051a-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a051a-132">xsd:string</span></span>  <br/> |<span data-ttu-id="a051a-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a051a-133">required</span></span>  <br/> |<span data-ttu-id="a051a-134">Соответствует имени столбца в наборе записей ADO.</span><span class="sxs-lookup"><span data-stu-id="a051a-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="a051a-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a051a-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a051a-136">Контексттипе</span><span class="sxs-lookup"><span data-stu-id="a051a-136">ContextType</span></span>  <br/> |<span data-ttu-id="a051a-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="a051a-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a051a-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a051a-138">required</span></span>  <br/> |<span data-ttu-id="a051a-139">Задает свойства группы или фигуры, которые необходимо использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a051a-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="a051a-140">Возможные значения показаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="a051a-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="a051a-141">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="a051a-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a051a-142">Контексттипелабел</span><span class="sxs-lookup"><span data-stu-id="a051a-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="a051a-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="a051a-143">xsd:string</span></span>  <br/> |<span data-ttu-id="a051a-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="a051a-144">optional</span></span>  <br/> |<span data-ttu-id="a051a-145">Если значение Контексттипе равно 2 или 3, этот атрибут является обязательным для определения сравнения.</span><span class="sxs-lookup"><span data-stu-id="a051a-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="a051a-146">Для Контексттипе = 2 Контексттипелабел должен быть меткой элемента данных Shape, а если **контексттипе** = 3, контексттипелабел должно быть именем локальной строки.</span><span class="sxs-lookup"><span data-stu-id="a051a-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="a051a-147">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="a051a-147">Values of the xsd:string type.</span></span>  <br/> |
   

