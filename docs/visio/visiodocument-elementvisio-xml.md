---
title: Элемент VisioDocument ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Корневой элемент документа Microsoft Visio.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391306"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="be6e8-103">Элемент VisioDocument ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="be6e8-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="be6e8-104">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="be6e8-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="be6e8-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="be6e8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be6e8-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="be6e8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="be6e8-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="be6e8-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="be6e8-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="be6e8-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="be6e8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="be6e8-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="be6e8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="be6e8-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="be6e8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="be6e8-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="be6e8-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be6e8-113">Определение</span><span class="sxs-lookup"><span data-stu-id="be6e8-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="be6e8-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="be6e8-114">Elements and attributes</span></span>

<span data-ttu-id="be6e8-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="be6e8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="be6e8-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="be6e8-116">Parent elements</span></span>

<span data-ttu-id="be6e8-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="be6e8-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="be6e8-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="be6e8-118">Child elements</span></span>

|<span data-ttu-id="be6e8-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="be6e8-119">**Element**</span></span>|<span data-ttu-id="be6e8-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="be6e8-120">**Type**</span></span>|<span data-ttu-id="be6e8-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be6e8-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be6e8-122">цвета;</span><span class="sxs-lookup"><span data-stu-id="be6e8-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-124">Содержит таблицы цветов документа.</span><span class="sxs-lookup"><span data-stu-id="be6e8-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="be6e8-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="be6e8-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-127">Содержит элементы, которые определяют параметры документов.</span><span class="sxs-lookup"><span data-stu-id="be6e8-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="be6e8-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="be6e8-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-130">Задает **ShapeSheet** структуры документа.</span><span class="sxs-lookup"><span data-stu-id="be6e8-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="be6e8-131">EventList</span><span class="sxs-lookup"><span data-stu-id="be6e8-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-133">Содержит элемент **EventItem** для каждого события, к которому должны отвечать объекта.</span><span class="sxs-lookup"><span data-stu-id="be6e8-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="be6e8-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="be6e8-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-136">Содержит коллекцию элементов **Название значка** .</span><span class="sxs-lookup"><span data-stu-id="be6e8-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="be6e8-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="be6e8-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-139">Содержит элементы для колонтитулов документа.</span><span class="sxs-lookup"><span data-stu-id="be6e8-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="be6e8-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="be6e8-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-142">Указывает набор графических страниц, доступных для просмотра и задайте наборов записей, которые обновляемый в документе.</span><span class="sxs-lookup"><span data-stu-id="be6e8-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="be6e8-143">Таблицы стилей</span><span class="sxs-lookup"><span data-stu-id="be6e8-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="be6e8-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="be6e8-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="be6e8-145">Содержит коллекцию элементов таблицы стилей для документа.</span><span class="sxs-lookup"><span data-stu-id="be6e8-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="be6e8-146">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="be6e8-146">Attributes</span></span>

<span data-ttu-id="be6e8-147">Нет.</span><span class="sxs-lookup"><span data-stu-id="be6e8-147">None.</span></span>
  

