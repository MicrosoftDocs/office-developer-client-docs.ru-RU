---
title: Элемент VisioDocument (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Корневой элемент документа Microsoft Visio.
ms.openlocfilehash: acb0a4e8ef1efb6d6d5872118241e36bb4e9630c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538489"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="a1ed9-103">Элемент VisioDocument (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a1ed9-103">VisioDocument element (Visio XML)</span></span>

<span data-ttu-id="a1ed9-104">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a1ed9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a1ed9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a1ed9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a1ed9-107">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a1ed9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a1ed9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a1ed9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a1ed9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a1ed9-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="a1ed9-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="a1ed9-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a1ed9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="a1ed9-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a1ed9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1ed9-114">Elements and attributes</span></span>

<span data-ttu-id="a1ed9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a1ed9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a1ed9-116">Parent elements</span></span>

<span data-ttu-id="a1ed9-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a1ed9-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a1ed9-118">Child elements</span></span>

|<span data-ttu-id="a1ed9-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-119">**Element**</span></span>|<span data-ttu-id="a1ed9-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-120">**Type**</span></span>|<span data-ttu-id="a1ed9-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a1ed9-122">Colors</span><span class="sxs-lookup"><span data-stu-id="a1ed9-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-123">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-124">Содержит цветовую таблицу документа.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="a1ed9-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="a1ed9-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-127">Содержит элементы, указывающие параметры документов.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="a1ed9-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="a1ed9-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-129">DocumentSheet_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-130">Указывает структуру **ShapeSheet документа.**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="a1ed9-131">EventList</span><span class="sxs-lookup"><span data-stu-id="a1ed9-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-132">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-133">Содержит элемент **EventItem** для каждого события, на которое должен отвечать объект.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="a1ed9-134">FaceNames</span><span class="sxs-lookup"><span data-stu-id="a1ed9-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-135">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-136">Содержит коллекцию **элементов FaceName.**</span><span class="sxs-lookup"><span data-stu-id="a1ed9-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="a1ed9-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="a1ed9-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-138">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-139">Содержит элементы для загона и подножки документа.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="a1ed9-140">PublishSettings</span><span class="sxs-lookup"><span data-stu-id="a1ed9-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-141">PublishSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-142">Указывает набор страниц рисования, которые можно просмотреть, и набор записей, которые обновляются в рисунке.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="a1ed9-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="a1ed9-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a1ed9-144">StyleSheets_Type</span><span class="sxs-lookup"><span data-stu-id="a1ed9-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a1ed9-145">Содержит коллекцию элементов StyleSheet для документа.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a1ed9-146">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a1ed9-146">Attributes</span></span>

<span data-ttu-id="a1ed9-147">Нет.</span><span class="sxs-lookup"><span data-stu-id="a1ed9-147">None.</span></span>
  

