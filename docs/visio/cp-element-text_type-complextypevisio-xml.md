---
title: элемент CP (Text_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4edd0a3f-e433-bf54-34cd-3b05fd10a5a5
description: Помечает начало свойства знака, которое отформатировано в соответствии с соответствующим элементом char. Выполнение определяется до конца текста или до следующего тега.
ms.openlocfilehash: 70f7d3f8333ff0f2c109862455fbd8cc3b340bf4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540562"
---
# <a name="cp-element-text_type-complextype-visio-xml"></a><span data-ttu-id="7c639-104">элемент CP (Text_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="7c639-104">cp element (Text_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="7c639-105">Помечает начало свойства знака, которое отформатировано в соответствии с соответствующим элементом char.</span><span class="sxs-lookup"><span data-stu-id="7c639-105">Marks the beginning of a character properties run that is formatted according to the corresponding Char element.</span></span> <span data-ttu-id="7c639-106">Выполнение определяется до конца текста или до следующего тега.</span><span class="sxs-lookup"><span data-stu-id="7c639-106">The run is defined to the end of the text or until the next tag.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7c639-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7c639-107">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c639-108">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="7c639-108">**Element type**</span></span> <br/> |[<span data-ttu-id="7c639-109">cp_Type</span><span class="sxs-lookup"><span data-stu-id="7c639-109">cp_Type</span></span>](cp_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7c639-110">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7c639-110">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7c639-111">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7c639-111">**Schema file**</span></span> <br/> |<span data-ttu-id="7c639-112">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="7c639-112">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7c639-113">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="7c639-113">**Document parts**</span></span> <br/> |<span data-ttu-id="7c639-114">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="7c639-114">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c639-115">Определение</span><span class="sxs-lookup"><span data-stu-id="7c639-115">Definition</span></span>

```XML
< xs:element name="cp" type="cp_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7c639-116">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7c639-116">Elements and attributes</span></span>

<span data-ttu-id="7c639-117">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7c639-117">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7c639-118">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="7c639-118">Parent elements</span></span>

|<span data-ttu-id="7c639-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7c639-119">**Element**</span></span>|<span data-ttu-id="7c639-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7c639-120">**Type**</span></span>|<span data-ttu-id="7c639-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7c639-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c639-122">Text</span><span class="sxs-lookup"><span data-stu-id="7c639-122">Text</span></span>](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c639-123">Text_Type</span><span class="sxs-lookup"><span data-stu-id="7c639-123">Text_Type</span></span>](text_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7c639-124">Содержит текст фигуры.</span><span class="sxs-lookup"><span data-stu-id="7c639-124">Contains the text of a shape.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7c639-125">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7c639-125">Child elements</span></span>

<span data-ttu-id="7c639-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="7c639-126">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7c639-127">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7c639-127">Attributes</span></span>

|<span data-ttu-id="7c639-128">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="7c639-128">**Attribute**</span></span>|<span data-ttu-id="7c639-129">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7c639-129">**Type**</span></span>|<span data-ttu-id="7c639-130">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="7c639-130">**Required**</span></span>|<span data-ttu-id="7c639-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7c639-131">**Description**</span></span>|<span data-ttu-id="7c639-132">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="7c639-132">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7c639-133">IX</span><span class="sxs-lookup"><span data-stu-id="7c639-133">IX</span></span>  <br/> |<span data-ttu-id="7c639-134">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="7c639-134">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c639-135">Обязательный</span><span class="sxs-lookup"><span data-stu-id="7c639-135">required</span></span>  <br/> |<span data-ttu-id="7c639-136">Индекс элемента char, представляемый этим свойством.</span><span class="sxs-lookup"><span data-stu-id="7c639-136">The Char element index that this property run represents.</span></span>  <br/> |<span data-ttu-id="7c639-137">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="7c639-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

