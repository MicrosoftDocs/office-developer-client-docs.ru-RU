---
title: Элемент Ровкэйвалуе (Примарикэй_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9077ad4b-c539-c0c8-d268-9a009990abdd
description: Задает значение первичного ключа для отдельной строки набора записей.
ms.openlocfilehash: 12d60bb0ccccdcd8c1790678cae4ad1e887e73b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283505"
---
# <a name="rowkeyvalue-element-primarykeytype-complextype-visio-xml"></a><span data-ttu-id="b5c96-103">Элемент Ровкэйвалуе (Примарикэй_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b5c96-103">RowKeyValue element (PrimaryKey_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b5c96-104">Задает значение первичного ключа для отдельной строки набора записей.</span><span class="sxs-lookup"><span data-stu-id="b5c96-104">Specifies the value of a primary key for an individual row of a recordset.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5c96-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b5c96-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5c96-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b5c96-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b5c96-107">Ровкэйвалуе_типе</span><span class="sxs-lookup"><span data-stu-id="b5c96-107">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b5c96-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b5c96-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b5c96-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b5c96-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b5c96-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b5c96-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b5c96-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b5c96-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b5c96-112">Recordset. XML</span><span class="sxs-lookup"><span data-stu-id="b5c96-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b5c96-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b5c96-113">Definition</span></span>

```XML
< xs:element name="RowKeyValue" type="RowKeyValue_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b5c96-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b5c96-114">Elements and attributes</span></span>

<span data-ttu-id="b5c96-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b5c96-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b5c96-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b5c96-116">Parent elements</span></span>

|<span data-ttu-id="b5c96-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b5c96-117">**Element**</span></span>|<span data-ttu-id="b5c96-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b5c96-118">**Type**</span></span>|<span data-ttu-id="b5c96-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b5c96-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b5c96-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b5c96-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b5c96-121">Примарикэй_типе</span><span class="sxs-lookup"><span data-stu-id="b5c96-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b5c96-122">Задает первичный ключ набора записей.</span><span class="sxs-lookup"><span data-stu-id="b5c96-122">Specifies a primary key of a recordset.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b5c96-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b5c96-123">Child elements</span></span>

<span data-ttu-id="b5c96-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="b5c96-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5c96-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b5c96-125">Attributes</span></span>

|<span data-ttu-id="b5c96-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b5c96-126">**Attribute**</span></span>|<span data-ttu-id="b5c96-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b5c96-127">**Type**</span></span>|<span data-ttu-id="b5c96-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b5c96-128">**Required**</span></span>|<span data-ttu-id="b5c96-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b5c96-129">**Description**</span></span>|<span data-ttu-id="b5c96-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b5c96-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b5c96-131">RowID</span><span class="sxs-lookup"><span data-stu-id="b5c96-131">RowID</span></span>  <br/> |<span data-ttu-id="b5c96-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="b5c96-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b5c96-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b5c96-133">required</span></span>  <br/> |<span data-ttu-id="b5c96-134">Уникальное значение, идентифицирующее строку в наборе записей.</span><span class="sxs-lookup"><span data-stu-id="b5c96-134">A unique value that identifies a row of a recordset.</span></span>  <br/> |<span data-ttu-id="b5c96-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="b5c96-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b5c96-136">Значение</span><span class="sxs-lookup"><span data-stu-id="b5c96-136">Value</span></span>  <br/> |<span data-ttu-id="b5c96-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="b5c96-137">xsd:string</span></span>  <br/> |<span data-ttu-id="b5c96-138">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b5c96-138">required</span></span>  <br/> |<span data-ttu-id="b5c96-139">Значение первичного ключа для этой строки набора записей.</span><span class="sxs-lookup"><span data-stu-id="b5c96-139">The value of the primary key for this row of the recordset.</span></span>  <br/> |<span data-ttu-id="b5c96-140">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="b5c96-140">Values of the xsd:string type.</span></span>  <br/> |
   

