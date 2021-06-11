---
title: элемент pp (Text_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5444543-fcd9-91cc-e7f8-cf860caa9fcc
description: Указывает начало запуска свойств абзаца. Запуск определяется до конца текста или до следующего тега.
ms.openlocfilehash: 695958c77f730abed03f50d6ad9c71f4de76dd63
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537740"
---
# <a name="pp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="4fd56-104">элемент pp (Text_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4fd56-104">pp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4fd56-105">Указывает начало запуска свойств абзаца.</span><span class="sxs-lookup"><span data-stu-id="4fd56-105">Specifies the beginning of a paragraph properties run.</span></span> <span data-ttu-id="4fd56-106">Запуск определяется до конца текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="4fd56-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fd56-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4fd56-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fd56-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4fd56-108">**Element type**</span></span> <br/> |[<span data-ttu-id="4fd56-109">pp_Type</span><span class="sxs-lookup"><span data-stu-id="4fd56-109">pp_Type</span></span>](pp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4fd56-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4fd56-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4fd56-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4fd56-111">**Schema file**</span></span> <br/> |<span data-ttu-id="4fd56-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4fd56-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4fd56-113">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="4fd56-113">**Document parts**</span></span> <br/> |<span data-ttu-id="4fd56-114">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="4fd56-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4fd56-115">Определение</span><span class="sxs-lookup"><span data-stu-id="4fd56-115">Definition</span></span>

```XML
< xs:element name="pp" type="pp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4fd56-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4fd56-116">Elements and attributes</span></span>

<span data-ttu-id="4fd56-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4fd56-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4fd56-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4fd56-118">Parent elements</span></span>

|<span data-ttu-id="4fd56-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4fd56-119">**Element**</span></span>|<span data-ttu-id="4fd56-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4fd56-120">**Type**</span></span>|<span data-ttu-id="4fd56-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4fd56-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4fd56-122">Text</span><span class="sxs-lookup"><span data-stu-id="4fd56-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4fd56-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="4fd56-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4fd56-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="4fd56-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4fd56-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4fd56-125">Child elements</span></span>

<span data-ttu-id="4fd56-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="4fd56-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fd56-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4fd56-127">Attributes</span></span>

|<span data-ttu-id="4fd56-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4fd56-128">**Attribute**</span></span>|<span data-ttu-id="4fd56-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4fd56-129">**Type**</span></span>|<span data-ttu-id="4fd56-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="4fd56-130">**Required**</span></span>|<span data-ttu-id="4fd56-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4fd56-131">**Description**</span></span>|<span data-ttu-id="4fd56-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4fd56-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4fd56-133">IX</span><span class="sxs-lookup"><span data-stu-id="4fd56-133">IX</span></span>  <br/> |<span data-ttu-id="4fd56-134">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4fd56-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4fd56-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4fd56-135">required</span></span>  <br/> |<span data-ttu-id="4fd56-136">Индекс элемента **Para,** который указывает форматирование, примененный к этому запуску.</span><span class="sxs-lookup"><span data-stu-id="4fd56-136">The index of the **Para** element that specifies the formatting applied to this run.</span></span>  <br/> |<span data-ttu-id="4fd56-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4fd56-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

