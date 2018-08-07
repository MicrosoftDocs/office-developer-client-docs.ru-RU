---
title: элемент позиции символа (Text_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Метки в начале символ свойства запустите то есть отформатированное в соответствии с соответствующих элементов (знак). Запустить определен в конец текста или до следующего тега.
ms.openlocfilehash: 16e5bb94afeb860220c6cb49a9b98e36e45d76cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813515"
---
# <a name="cp-element-texttype-complextype-visio-xml"></a><span data-ttu-id="39be4-104">элемент позиции символа (Text_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="39be4-104">cp element (Text_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="39be4-105">Метки в начале символ свойства запустите то есть отформатированное в соответствии с соответствующих элементов (знак).</span><span class="sxs-lookup"><span data-stu-id="39be4-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="39be4-106">Запустить определен в конец текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="39be4-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="39be4-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="39be4-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39be4-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="39be4-108">**Element type**</span></span> <br/> |[<span data-ttu-id="39be4-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="39be4-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="39be4-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="39be4-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="39be4-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="39be4-111">**Schema file**</span></span> <br/> |<span data-ttu-id="39be4-112">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="39be4-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="39be4-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="39be4-113">**Document parts**</span></span> <br/> |<span data-ttu-id="39be4-114">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="39be4-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="39be4-115">Определение</span><span class="sxs-lookup"><span data-stu-id="39be4-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="39be4-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="39be4-116">Elements and attributes</span></span>

<span data-ttu-id="39be4-117">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="39be4-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="39be4-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="39be4-118">Parent elements</span></span>

|<span data-ttu-id="39be4-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="39be4-119">**Element**</span></span>|<span data-ttu-id="39be4-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="39be4-120">**Type**</span></span>|<span data-ttu-id="39be4-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="39be4-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="39be4-122">Text</span><span class="sxs-lookup"><span data-stu-id="39be4-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="39be4-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="39be4-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="39be4-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="39be4-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="39be4-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="39be4-125">Child elements</span></span>

<span data-ttu-id="39be4-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="39be4-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39be4-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="39be4-127">Attributes</span></span>

|<span data-ttu-id="39be4-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="39be4-128">**Attribute**</span></span>|<span data-ttu-id="39be4-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="39be4-129">**Type**</span></span>|<span data-ttu-id="39be4-130">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="39be4-130">**Required**</span></span>|<span data-ttu-id="39be4-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="39be4-131">**Description**</span></span>|<span data-ttu-id="39be4-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="39be4-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="39be4-133">IX</span><span class="sxs-lookup"><span data-stu-id="39be4-133">IX</span></span>  <br/> |<span data-ttu-id="39be4-134">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="39be4-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="39be4-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="39be4-135">required</span></span>  <br/> |<span data-ttu-id="39be4-136">Индекс элемента (знак), который представляет это свойство запуска.</span><span class="sxs-lookup"><span data-stu-id="39be4-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="39be4-137">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="39be4-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

