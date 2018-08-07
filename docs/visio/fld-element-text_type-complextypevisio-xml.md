---
title: элемент Fld (Text_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92d90240-012b-9598-c893-6e7085813aa5
description: Указывает точку вставки текстового поля для соответствующего элемента Field.
ms.openlocfilehash: 9ff1a81c8ceba83adc110596de86831b58db0167
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813776"
---
# <a name="fld-element-texttype-complextype-visio-xml"></a><span data-ttu-id="74169-103">элемент Fld (Text_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="74169-103">fld element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="74169-104">Указывает точку вставки текстового поля для соответствующего элемента **Field** .</span><span class="sxs-lookup"><span data-stu-id="74169-104">Indicates a text-field insertion point for the corresponding **Field** element.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="74169-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="74169-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74169-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="74169-106">**Element type**</span></span> <br/> |[<span data-ttu-id="74169-107">fld_Type</span><span class="sxs-lookup"><span data-stu-id="74169-107">fld_Type</span></span>](fld_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="74169-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="74169-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="74169-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="74169-109">**Schema file**</span></span> <br/> |<span data-ttu-id="74169-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="74169-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="74169-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="74169-111">**Document parts**</span></span> <br/> |<span data-ttu-id="74169-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="74169-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="74169-113">Определение</span><span class="sxs-lookup"><span data-stu-id="74169-113">Definition</span></span>

```XML
< xs:element name="fld" type="fld_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="74169-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="74169-114">Elements and attributes</span></span>

<span data-ttu-id="74169-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="74169-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="74169-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="74169-116">Parent elements</span></span>

|<span data-ttu-id="74169-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="74169-117">**Element**</span></span>|<span data-ttu-id="74169-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="74169-118">**Type**</span></span>|<span data-ttu-id="74169-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74169-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="74169-120">Text</span><span class="sxs-lookup"><span data-stu-id="74169-120">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="74169-121">Text_Type</span><span class="sxs-lookup"><span data-stu-id="74169-121">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="74169-122">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="74169-122">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="74169-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="74169-123">Child elements</span></span>

<span data-ttu-id="74169-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="74169-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="74169-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="74169-125">Attributes</span></span>

|<span data-ttu-id="74169-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="74169-126">**Attribute**</span></span>|<span data-ttu-id="74169-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="74169-127">**Type**</span></span>|<span data-ttu-id="74169-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="74169-128">**Required**</span></span>|<span data-ttu-id="74169-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74169-129">**Description**</span></span>|<span data-ttu-id="74169-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="74169-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="74169-131">IX</span><span class="sxs-lookup"><span data-stu-id="74169-131">IX</span></span>  <br/> |<span data-ttu-id="74169-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="74169-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="74169-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="74169-133">required</span></span>  <br/> |<span data-ttu-id="74169-134">Отсчитываемый от нуля индекс элемента в рамках родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="74169-134">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="74169-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="74169-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

