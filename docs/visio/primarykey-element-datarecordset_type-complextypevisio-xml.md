---
title: Элемент PrimaryKey (Датарекордсет_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Определяет один или несколько столбцов первичного ключа в наборе записей данных.
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355999"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="4af38-103">Элемент PrimaryKey (Датарекордсет_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="4af38-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4af38-104">Определяет один или несколько столбцов первичного ключа в наборе записей данных.</span><span class="sxs-lookup"><span data-stu-id="4af38-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4af38-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4af38-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4af38-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4af38-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4af38-107">Примарикэй_типе</span><span class="sxs-lookup"><span data-stu-id="4af38-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4af38-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4af38-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4af38-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4af38-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4af38-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4af38-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4af38-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4af38-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4af38-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="4af38-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4af38-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4af38-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4af38-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4af38-114">Elements and attributes</span></span>

<span data-ttu-id="4af38-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4af38-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4af38-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4af38-116">Parent elements</span></span>

|<span data-ttu-id="4af38-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4af38-117">**Element**</span></span>|<span data-ttu-id="4af38-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4af38-118">**Type**</span></span>|<span data-ttu-id="4af38-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4af38-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4af38-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="4af38-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4af38-121">Датарекордсет_типе</span><span class="sxs-lookup"><span data-stu-id="4af38-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4af38-122">Хранение, форматирование, обновление и предоставление данных, запрашиваемых из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="4af38-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4af38-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4af38-123">Child elements</span></span>

|<span data-ttu-id="4af38-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4af38-124">**Element**</span></span>|<span data-ttu-id="4af38-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4af38-125">**Type**</span></span>|<span data-ttu-id="4af38-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4af38-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4af38-127">Ровкэйвалуе</span><span class="sxs-lookup"><span data-stu-id="4af38-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4af38-128">Ровкэйвалуе_типе</span><span class="sxs-lookup"><span data-stu-id="4af38-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4af38-129">Задает значение этого компонента первичного ключа для отдельной строки набора записей.</span><span class="sxs-lookup"><span data-stu-id="4af38-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="4af38-130">ДОЛЖЕН быть хотя бы один экземпляр этого дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="4af38-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4af38-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4af38-131">Attributes</span></span>

|<span data-ttu-id="4af38-132">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4af38-132">**Attribute**</span></span>|<span data-ttu-id="4af38-133">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4af38-133">**Type**</span></span>|<span data-ttu-id="4af38-134">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4af38-134">**Required**</span></span>|<span data-ttu-id="4af38-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4af38-135">**Description**</span></span>|<span data-ttu-id="4af38-136">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4af38-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4af38-137">Колумннамеид</span><span class="sxs-lookup"><span data-stu-id="4af38-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="4af38-138">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="4af38-138">xsd:string</span></span>  <br/> |<span data-ttu-id="4af38-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="4af38-139">optional</span></span>  <br/> |<span data-ttu-id="4af38-140">Задает имя поля, которое является компонентом первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="4af38-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="4af38-141">Он должен быть значением атрибута **колумннамеид** элемента потомков Датаколумн_типе элемента датарекордсет_типе, для которого указывается первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="4af38-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="4af38-142">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="4af38-142">Values of the xsd:string type.</span></span>  <br/> |
   

