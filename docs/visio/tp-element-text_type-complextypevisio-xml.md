---
title: элемент tp (Text_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b13b9328-c6a0-e282-257c-2de55901df6a
description: Указывает начало запуска свойств вкладок. Запуск определяется до конца текста или до следующего тега.
ms.openlocfilehash: dad7a3de715473a75c601c1e391c9d51fc1cab85
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542977"
---
# <a name="tp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="c27d6-104">элемент tp (Text_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c27d6-104">tp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c27d6-105">Указывает начало запуска свойств вкладок.</span><span class="sxs-lookup"><span data-stu-id="c27d6-105">Specifies the beginning of a tabs properties run.</span></span> <span data-ttu-id="c27d6-106">Запуск определяется до конца текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="c27d6-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c27d6-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c27d6-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c27d6-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c27d6-108">**Element type**</span></span> <br/> |[<span data-ttu-id="c27d6-109">tp_Type</span><span class="sxs-lookup"><span data-stu-id="c27d6-109">tp_Type</span></span>](tp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c27d6-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c27d6-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c27d6-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c27d6-111">**Schema file**</span></span> <br/> |<span data-ttu-id="c27d6-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c27d6-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c27d6-113">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="c27d6-113">**Document parts**</span></span> <br/> |<span data-ttu-id="c27d6-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="c27d6-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c27d6-115">Определение</span><span class="sxs-lookup"><span data-stu-id="c27d6-115">Definition</span></span>

```XML
< xs:element name="tp" type="tp_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c27d6-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c27d6-116">Elements and attributes</span></span>

<span data-ttu-id="c27d6-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c27d6-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c27d6-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c27d6-118">Parent elements</span></span>

|<span data-ttu-id="c27d6-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c27d6-119">**Element**</span></span>|<span data-ttu-id="c27d6-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c27d6-120">**Type**</span></span>|<span data-ttu-id="c27d6-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c27d6-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c27d6-122">Text</span><span class="sxs-lookup"><span data-stu-id="c27d6-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c27d6-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="c27d6-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c27d6-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="c27d6-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c27d6-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c27d6-125">Child elements</span></span>

<span data-ttu-id="c27d6-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="c27d6-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c27d6-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c27d6-127">Attributes</span></span>

|<span data-ttu-id="c27d6-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c27d6-128">**Attribute**</span></span>|<span data-ttu-id="c27d6-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c27d6-129">**Type**</span></span>|<span data-ttu-id="c27d6-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c27d6-130">**Required**</span></span>|<span data-ttu-id="c27d6-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c27d6-131">**Description**</span></span>|<span data-ttu-id="c27d6-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c27d6-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c27d6-133">IX</span><span class="sxs-lookup"><span data-stu-id="c27d6-133">IX</span></span>  <br/> |<span data-ttu-id="c27d6-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c27d6-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c27d6-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c27d6-135">required</span></span>  <br/> |<span data-ttu-id="c27d6-136">Нулевой индекс элемента в родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="c27d6-136">The zero-based index of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="c27d6-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c27d6-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

