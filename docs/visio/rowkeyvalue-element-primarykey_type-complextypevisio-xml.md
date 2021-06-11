---
title: Элемент RowKeyValue (PrimaryKey_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Указывает значение основного ключа для отдельной строки наборов записей.
ms.openlocfilehash: b21f479a9c0404dc8a3b737208e4d0d634b556f4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538132"
---
# <a name="rowkeyvalue-element-primarykey_type-complextype-visio-xml"></a><span data-ttu-id="423ee-103">Элемент RowKeyValue (PrimaryKey_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="423ee-103">RowKeyValue element (PrimaryKey_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="423ee-104">Указывает значение основного ключа для отдельной строки наборов записей.</span><span class="sxs-lookup"><span data-stu-id="423ee-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="423ee-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="423ee-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="423ee-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="423ee-106">**Element type**</span></span> <br/> |[<span data-ttu-id="423ee-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="423ee-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="423ee-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="423ee-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="423ee-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="423ee-109">**Schema file**</span></span> <br/> |<span data-ttu-id="423ee-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="423ee-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="423ee-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="423ee-111">**Document parts**</span></span> <br/> |<span data-ttu-id="423ee-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="423ee-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="423ee-113">Определение</span><span class="sxs-lookup"><span data-stu-id="423ee-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="423ee-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="423ee-114">Elements and attributes</span></span>

<span data-ttu-id="423ee-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="423ee-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="423ee-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="423ee-116">Parent elements</span></span>

|<span data-ttu-id="423ee-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="423ee-117">**Element**</span></span>|<span data-ttu-id="423ee-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="423ee-118">**Type**</span></span>|<span data-ttu-id="423ee-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="423ee-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="423ee-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="423ee-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="423ee-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="423ee-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="423ee-122">Указывает основной ключ наборов записей.</span><span class="sxs-lookup"><span data-stu-id="423ee-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="423ee-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="423ee-123">Child elements</span></span>

<span data-ttu-id="423ee-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="423ee-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="423ee-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="423ee-125">Attributes</span></span>

|<span data-ttu-id="423ee-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="423ee-126">**Attribute**</span></span>|<span data-ttu-id="423ee-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="423ee-127">**Type**</span></span>|<span data-ttu-id="423ee-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="423ee-128">**Required**</span></span>|<span data-ttu-id="423ee-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="423ee-129">**Description**</span></span>|<span data-ttu-id="423ee-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="423ee-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="423ee-131">RowID</span><span class="sxs-lookup"><span data-stu-id="423ee-131">RowID</span></span>  <br/> |<span data-ttu-id="423ee-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="423ee-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="423ee-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="423ee-133">required</span></span>  <br/> |<span data-ttu-id="423ee-134">Уникальное значение, которое определяет строку наборов записей.</span><span class="sxs-lookup"><span data-stu-id="423ee-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="423ee-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="423ee-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="423ee-136">Значение</span><span class="sxs-lookup"><span data-stu-id="423ee-136">Value</span></span>  <br/> |<span data-ttu-id="423ee-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="423ee-137">xsd:string</span></span>  <br/> |<span data-ttu-id="423ee-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="423ee-138">required</span></span>  <br/> |<span data-ttu-id="423ee-139">Значение основного ключа для этой строки наборов записей.</span><span class="sxs-lookup"><span data-stu-id="423ee-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="423ee-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="423ee-140">Values of the xsd:string type.</span></span>  <br/> |
   

