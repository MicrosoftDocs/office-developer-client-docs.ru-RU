---
title: Элемент fld (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Указывает точку вставки текстового поля для соответствующего элемента Field.
ms.openlocfilehash: efacb7ed11968dec5d5c2f62b0ca3e3bcd8580c0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539616"
---
# <a name="fld-element-text_type-complextype-visio-xml"></a><span data-ttu-id="7cda3-103">Элемент fld (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="7cda3-103">fld element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7cda3-104">Указывает точку вставки текстового поля для соответствующего **элемента Field.**</span><span class="sxs-lookup"><span data-stu-id="7cda3-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7cda3-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7cda3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7cda3-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7cda3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7cda3-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="7cda3-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7cda3-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7cda3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7cda3-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7cda3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7cda3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7cda3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7cda3-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="7cda3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7cda3-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="7cda3-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7cda3-113">Определение</span><span class="sxs-lookup"><span data-stu-id="7cda3-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7cda3-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7cda3-114">Elements and attributes</span></span>

<span data-ttu-id="7cda3-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7cda3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7cda3-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7cda3-116">Parent elements</span></span>

|<span data-ttu-id="7cda3-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7cda3-117">**Element**</span></span>|<span data-ttu-id="7cda3-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7cda3-118">**Type**</span></span>|<span data-ttu-id="7cda3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7cda3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7cda3-120">Text</span><span class="sxs-lookup"><span data-stu-id="7cda3-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7cda3-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="7cda3-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7cda3-122">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="7cda3-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7cda3-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7cda3-123">Child elements</span></span>

<span data-ttu-id="7cda3-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="7cda3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cda3-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7cda3-125">Attributes</span></span>

|<span data-ttu-id="7cda3-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7cda3-126">**Attribute**</span></span>|<span data-ttu-id="7cda3-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7cda3-127">**Type**</span></span>|<span data-ttu-id="7cda3-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7cda3-128">**Required**</span></span>|<span data-ttu-id="7cda3-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7cda3-129">**Description**</span></span>|<span data-ttu-id="7cda3-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7cda3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7cda3-131">IX</span><span class="sxs-lookup"><span data-stu-id="7cda3-131">IX</span></span>  <br/> |<span data-ttu-id="7cda3-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7cda3-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7cda3-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7cda3-133">required</span></span>  <br/> |<span data-ttu-id="7cda3-134">Индекс элемента в родительском элементе с нулем.</span><span class="sxs-lookup"><span data-stu-id="7cda3-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="7cda3-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7cda3-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

