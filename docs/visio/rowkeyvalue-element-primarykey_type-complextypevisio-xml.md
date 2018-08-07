---
title: Элемент RowKeyValue (PrimaryKey_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Указывает значение первичный ключ для отдельных строк набора записей.
ms.openlocfilehash: 3b91997b5fe8184eb89f8c53197a512d809171b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814694"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="bcaae-103">Элемент RowKeyValue (PrimaryKey_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="bcaae-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="bcaae-104">Указывает значение первичный ключ для отдельных строк набора записей.</span><span class="sxs-lookup"><span data-stu-id="bcaae-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bcaae-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="bcaae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bcaae-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="bcaae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bcaae-107">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="bcaae-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bcaae-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bcaae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bcaae-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bcaae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bcaae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="bcaae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bcaae-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="bcaae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bcaae-112">recordsets.XML</span><span class="sxs-lookup"><span data-stu-id="bcaae-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bcaae-113">Определение</span><span class="sxs-lookup"><span data-stu-id="bcaae-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bcaae-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bcaae-114">Elements and attributes</span></span>

<span data-ttu-id="bcaae-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="bcaae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bcaae-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="bcaae-116">Parent elements</span></span>

|<span data-ttu-id="bcaae-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bcaae-117">**Element**</span></span>|<span data-ttu-id="bcaae-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bcaae-118">**Type**</span></span>|<span data-ttu-id="bcaae-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bcaae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bcaae-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="bcaae-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bcaae-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="bcaae-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bcaae-122">Указывает первичный ключ набора записей.</span><span class="sxs-lookup"><span data-stu-id="bcaae-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bcaae-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bcaae-123">Child elements</span></span>

<span data-ttu-id="bcaae-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="bcaae-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bcaae-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bcaae-125">Attributes</span></span>

|<span data-ttu-id="bcaae-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="bcaae-126">**Attribute**</span></span>|<span data-ttu-id="bcaae-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bcaae-127">**Type**</span></span>|<span data-ttu-id="bcaae-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="bcaae-128">**Required**</span></span>|<span data-ttu-id="bcaae-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bcaae-129">**Description**</span></span>|<span data-ttu-id="bcaae-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="bcaae-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bcaae-131">RowID</span><span class="sxs-lookup"><span data-stu-id="bcaae-131">RowID</span></span>  <br/> |<span data-ttu-id="bcaae-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bcaae-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bcaae-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bcaae-133">required</span></span>  <br/> |<span data-ttu-id="bcaae-134">Уникальное значение, определяющее строки набора записей.</span><span class="sxs-lookup"><span data-stu-id="bcaae-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="bcaae-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bcaae-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bcaae-136">Значение</span><span class="sxs-lookup"><span data-stu-id="bcaae-136">Value</span></span>  <br/> |<span data-ttu-id="bcaae-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bcaae-137">xsd:string</span></span>  <br/> |<span data-ttu-id="bcaae-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bcaae-138">required</span></span>  <br/> |<span data-ttu-id="bcaae-139">Значение основной ключ для этой строки набора записей.</span><span class="sxs-lookup"><span data-stu-id="bcaae-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="bcaae-140">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bcaae-140">Values of the xsd:string type.</span></span>  <br/> |
   

