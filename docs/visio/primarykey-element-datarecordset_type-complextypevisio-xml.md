---
title: Элемент PrimaryKey (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 47533e6e-0a48-af61-a0c2-b2cec140ae4b
description: Определяет один или несколько столбцы первичных ключей в записей данных.
ms.openlocfilehash: c001c343c33e65c3990744b885f1c345575b1ab3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396360"
---
# <a name="primarykey-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="e03e6-103">Элемент PrimaryKey (DataRecordSet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e03e6-103">PrimaryKey element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e03e6-104">Определяет один или несколько столбцы первичных ключей в записей данных.</span><span class="sxs-lookup"><span data-stu-id="e03e6-104">Identifies one or more primary-key columns in the data recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e03e6-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e03e6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e03e6-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e03e6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e03e6-107">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="e03e6-107">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e03e6-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e03e6-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e03e6-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e03e6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e03e6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e03e6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e03e6-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e03e6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e03e6-112">recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="e03e6-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e03e6-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e03e6-113">Definition</span></span>

```XML
< xs:element name="PrimaryKey" type="PrimaryKey_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e03e6-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e03e6-114">Elements and attributes</span></span>

<span data-ttu-id="e03e6-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e03e6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e03e6-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e03e6-116">Parent elements</span></span>

|<span data-ttu-id="e03e6-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e03e6-117">**Element**</span></span>|<span data-ttu-id="e03e6-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e03e6-118">**Type**</span></span>|<span data-ttu-id="e03e6-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e03e6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e03e6-120">Записей данных</span><span class="sxs-lookup"><span data-stu-id="e03e6-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e03e6-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="e03e6-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e03e6-122">Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="e03e6-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e03e6-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e03e6-123">Child elements</span></span>

|<span data-ttu-id="e03e6-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e03e6-124">**Element**</span></span>|<span data-ttu-id="e03e6-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e03e6-125">**Type**</span></span>|<span data-ttu-id="e03e6-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e03e6-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e03e6-127">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="e03e6-127">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e03e6-128">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="e03e6-128">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e03e6-129">Указывает значение этот компонент основной ключ для отдельных строк набора записей.</span><span class="sxs-lookup"><span data-stu-id="e03e6-129">Specifies the value of this component of the primary key for an individual row of a recordset.</span></span> <span data-ttu-id="e03e6-130">НЕОБХОДИМО быть по крайней мере одно вхождение дочернего элемента.</span><span class="sxs-lookup"><span data-stu-id="e03e6-130">There MUST be at least one occurrence of this child element.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e03e6-131">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e03e6-131">Attributes</span></span>

|<span data-ttu-id="e03e6-132">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e03e6-132">**Attribute**</span></span>|<span data-ttu-id="e03e6-133">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e03e6-133">**Type**</span></span>|<span data-ttu-id="e03e6-134">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e03e6-134">**Required**</span></span>|<span data-ttu-id="e03e6-135">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e03e6-135">**Description**</span></span>|<span data-ttu-id="e03e6-136">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e03e6-136">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e03e6-137">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="e03e6-137">ColumnNameID</span></span>  <br/> |<span data-ttu-id="e03e6-138">XSD:String</span><span class="sxs-lookup"><span data-stu-id="e03e6-138">xsd:string</span></span>  <br/> |<span data-ttu-id="e03e6-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="e03e6-139">optional</span></span>  <br/> |<span data-ttu-id="e03e6-140">Указывает имя поля, который является частью первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="e03e6-140">Specifies the name of a field that is a component of the primary key.</span></span> <span data-ttu-id="e03e6-141">Оно должно быть значение атрибута **ColumnNameID** элемента DataColumn_Type потомкам из DataRecordSet_Type, указано, первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="e03e6-141">It MUST be the value of the **ColumnNameID** attribute of a DataColumn_Type descendant element of the DataRecordSet_Type whose primary key is being specified.</span></span>  <br/> |<span data-ttu-id="e03e6-142">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e03e6-142">Values of the xsd:string type.</span></span>  <br/> |
   

