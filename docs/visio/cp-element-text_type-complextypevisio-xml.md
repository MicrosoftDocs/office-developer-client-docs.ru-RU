---
title: элемент позиции символа (Text_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Метки в начале символ свойства запустите то есть отформатированное в соответствии с соответствующих элементов (знак). Запустить определен в конец текста или до следующего тега.
ms.openlocfilehash: eb7fd30c2314e159dc3649e87cd63bd4090ba283
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388198"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="1d4c8-104">элемент позиции символа (Text_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1d4c8-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="1d4c8-105">Метки в начале символ свойства запустите то есть отформатированное в соответствии с соответствующих элементов (знак).</span><span class="sxs-lookup"><span data-stu-id="1d4c8-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="1d4c8-106">Запустить определен в конец текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="1d4c8-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d4c8-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="1d4c8-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d4c8-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-108">**Element type**</span></span> <br/> |[<span data-ttu-id="1d4c8-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="1d4c8-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1d4c8-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-110">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1d4c8-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-111">**Schema file**</span></span> <br/> |<span data-ttu-id="1d4c8-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1d4c8-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1d4c8-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-113">**Document parts**</span></span> <br/> |<span data-ttu-id="1d4c8-114">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="1d4c8-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1d4c8-115">Определение</span><span class="sxs-lookup"><span data-stu-id="1d4c8-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1d4c8-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1d4c8-116">Elements and attributes</span></span>

<span data-ttu-id="1d4c8-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1d4c8-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1d4c8-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="1d4c8-118">Parent elements</span></span>

|<span data-ttu-id="1d4c8-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-119">**Element**</span></span>|<span data-ttu-id="1d4c8-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-120">**Type**</span></span>|<span data-ttu-id="1d4c8-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1d4c8-122">Text</span><span class="sxs-lookup"><span data-stu-id="1d4c8-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1d4c8-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="1d4c8-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1d4c8-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="1d4c8-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1d4c8-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1d4c8-125">Child elements</span></span>

<span data-ttu-id="1d4c8-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="1d4c8-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d4c8-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1d4c8-127">Attributes</span></span>

|<span data-ttu-id="1d4c8-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-128">**Attribute**</span></span>|<span data-ttu-id="1d4c8-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-129">**Type**</span></span>|<span data-ttu-id="1d4c8-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-130">**Required**</span></span>|<span data-ttu-id="1d4c8-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-131">**Description**</span></span>|<span data-ttu-id="1d4c8-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1d4c8-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1d4c8-133">IX</span><span class="sxs-lookup"><span data-stu-id="1d4c8-133">IX</span></span>  <br/> |<span data-ttu-id="1d4c8-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1d4c8-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1d4c8-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1d4c8-135">required</span></span>  <br/> |<span data-ttu-id="1d4c8-136">Индекс элемента (знак), который представляет это свойство запуска.</span><span class="sxs-lookup"><span data-stu-id="1d4c8-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="1d4c8-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1d4c8-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

