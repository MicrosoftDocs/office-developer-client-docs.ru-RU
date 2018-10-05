---
title: Элемент AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Задает правило, которое представлено сравнение столбцов в родительском элементе записей данных с помощью элемента данных фигуры из последней успешной автоматического связывания действия, выполняемые в пользовательском интерфейсе.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385720"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="3ad94-103">Элемент AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="3ad94-103">AutoLinkComparison element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="3ad94-104">Задает правило, которое представлено сравнение столбцов в родительском элементе **записей данных** с помощью элемента данных фигуры из последней успешной автоматического связывания действия, выполняемые в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3ad94-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3ad94-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3ad94-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ad94-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3ad94-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3ad94-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="3ad94-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3ad94-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3ad94-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3ad94-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3ad94-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3ad94-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="3ad94-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3ad94-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3ad94-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3ad94-112">recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="3ad94-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ad94-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3ad94-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ad94-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3ad94-114">Elements and attributes</span></span>

<span data-ttu-id="3ad94-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3ad94-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3ad94-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3ad94-116">Parent elements</span></span>

|<span data-ttu-id="3ad94-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3ad94-117">**Element**</span></span>|<span data-ttu-id="3ad94-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3ad94-118">**Type**</span></span>|<span data-ttu-id="3ad94-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ad94-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ad94-120">Записей данных</span><span class="sxs-lookup"><span data-stu-id="3ad94-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ad94-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="3ad94-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ad94-122">Задает набор записей и привязки данных между этого набора записей и фигур в страницы документа.</span><span class="sxs-lookup"><span data-stu-id="3ad94-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="3ad94-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3ad94-123">Child elements</span></span>

<span data-ttu-id="3ad94-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="3ad94-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3ad94-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3ad94-125">Attributes</span></span>

|<span data-ttu-id="3ad94-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="3ad94-126">**Attribute**</span></span>|<span data-ttu-id="3ad94-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3ad94-127">**Type**</span></span>|<span data-ttu-id="3ad94-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="3ad94-128">**Required**</span></span>|<span data-ttu-id="3ad94-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ad94-129">**Description**</span></span>|<span data-ttu-id="3ad94-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="3ad94-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ad94-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="3ad94-131">ColumnName</span></span>  <br/> |<span data-ttu-id="3ad94-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3ad94-132">xsd:string</span></span>  <br/> |<span data-ttu-id="3ad94-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3ad94-133">required</span></span>  <br/> |<span data-ttu-id="3ad94-134">Соответствует имени столбца в записей ADO.</span><span class="sxs-lookup"><span data-stu-id="3ad94-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="3ad94-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3ad94-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3ad94-136">ContextType</span><span class="sxs-lookup"><span data-stu-id="3ad94-136">ContextType</span></span>  <br/> |<span data-ttu-id="3ad94-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3ad94-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3ad94-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="3ad94-138">required</span></span>  <br/> |<span data-ttu-id="3ad94-139">Задает свойства группы или фигуры, используется для сравнения.</span><span class="sxs-lookup"><span data-stu-id="3ad94-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="3ad94-140">В следующей таблице показаны возможные значения.</span><span class="sxs-lookup"><span data-stu-id="3ad94-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="3ad94-141">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3ad94-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3ad94-142">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="3ad94-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="3ad94-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="3ad94-143">xsd:string</span></span>  <br/> |<span data-ttu-id="3ad94-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="3ad94-144">optional</span></span>  <br/> |<span data-ttu-id="3ad94-145">Если значение ContextType 2 или 3, этот атрибут требуется для определения сравнение.</span><span class="sxs-lookup"><span data-stu-id="3ad94-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="3ad94-146">ContextType = 2, ContextTypeLabel должна быть метка элемента данных фигуры и если **ContextType** = 3, ContextTypeLabel должно быть имя локального строки.</span><span class="sxs-lookup"><span data-stu-id="3ad94-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="3ad94-147">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3ad94-147">Values of the xsd:string type.</span></span>  <br/> |
   

