---
title: Элемент Аутолинккомпарисон (DataRecordSet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Определяет правило, которое сравнивает столбец в родительском элементе данных фигуры с элементом данных фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537873"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="e1ad5-103">Элемент Аутолинккомпарисон (DataRecordSet_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="e1ad5-103">AutoLinkComparison element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e1ad5-104">Определяет правило, которое сравнивает столбец в родительском элементе данных фигуры **с элементом данных** фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-104">Defines a rule that compares a column in the parent **DataRecordset** element with a shape data item from the last successful automatic linking action performed in the user interface.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e1ad5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e1ad5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1ad5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e1ad5-107">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="e1ad5-107">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e1ad5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e1ad5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e1ad5-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e1ad5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e1ad5-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e1ad5-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="e1ad5-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e1ad5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e1ad5-113">Definition</span></span>

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e1ad5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1ad5-114">Elements and attributes</span></span>

<span data-ttu-id="e1ad5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e1ad5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e1ad5-116">Parent elements</span></span>

|<span data-ttu-id="e1ad5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-117">**Element**</span></span>|<span data-ttu-id="e1ad5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-118">**Type**</span></span>|<span data-ttu-id="e1ad5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1ad5-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="e1ad5-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e1ad5-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="e1ad5-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e1ad5-122">Задает набор записей и привязку данных между этим набором записей и фигурами на страницах документа.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-122">Specifies a recordset and the data binding between that recordset and shapes in drawing pages.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e1ad5-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e1ad5-123">Child elements</span></span>

<span data-ttu-id="e1ad5-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e1ad5-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1ad5-125">Attributes</span></span>

|<span data-ttu-id="e1ad5-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-126">**Attribute**</span></span>|<span data-ttu-id="e1ad5-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-127">**Type**</span></span>|<span data-ttu-id="e1ad5-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-128">**Required**</span></span>|<span data-ttu-id="e1ad5-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-129">**Description**</span></span>|<span data-ttu-id="e1ad5-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e1ad5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e1ad5-131">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e1ad5-131">ColumnName</span></span>  <br/> |<span data-ttu-id="e1ad5-132">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e1ad5-132">xsd:string</span></span>  <br/> |<span data-ttu-id="e1ad5-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1ad5-133">required</span></span>  <br/> |<span data-ttu-id="e1ad5-134">Соответствует имени столбца в наборе записей ADO.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-134">Corresponds to a column name in the ADO recordset.</span></span>  <br/> |<span data-ttu-id="e1ad5-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e1ad5-136">контексттипе</span><span class="sxs-lookup"><span data-stu-id="e1ad5-136">ContextType</span></span>  <br/> |<span data-ttu-id="e1ad5-137">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="e1ad5-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e1ad5-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e1ad5-138">required</span></span>  <br/> |<span data-ttu-id="e1ad5-139">Задает свойства группы или фигуры, которые необходимо использовать для сравнения.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-139">Specifies properties of the group or shape to use for the comparison.</span></span> <span data-ttu-id="e1ad5-140">Возможные значения показаны в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-140">Possible values are shown in the following table.</span></span>  <br/> |<span data-ttu-id="e1ad5-141">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-141">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e1ad5-142">контексттипелабел</span><span class="sxs-lookup"><span data-stu-id="e1ad5-142">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="e1ad5-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e1ad5-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e1ad5-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="e1ad5-144">optional</span></span>  <br/> |<span data-ttu-id="e1ad5-145">Если значение Контексттипе равно 2 или 3, этот атрибут является обязательным для определения сравнения.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-145">If the ContextType value is 2 or 3, this attribute is required to define a comparison.</span></span> <span data-ttu-id="e1ad5-146">Для Контексттипе = 2 Контексттипелабел должен быть меткой элемента данных Shape, а если **контексттипе** = 3, контексттипелабел должно быть именем локальной строки.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-146">For ContextType = 2, ContextTypeLabel must be the shape data item label, and if **ContextType** = 3, ContextTypeLabel must be the local row name.</span></span>  <br/> |<span data-ttu-id="e1ad5-147">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e1ad5-147">Values of the xsd:string type.</span></span>  <br/> |
   

