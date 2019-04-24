---
title: Элемент Висиодокумент (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5954685-3a2d-7848-388f-5dd7e536551c
description: Корневой элемент документа Microsoft Visio.
ms.openlocfilehash: 9829fa8960d78777e0fff4306b96978da90a647d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285315"
---
# <a name="visiodocument-element-visio-xml"></a><span data-ttu-id="59878-103">Элемент Висиодокумент (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="59878-103">VisioDocument element ('Visio XML')</span></span>

<span data-ttu-id="59878-104">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="59878-104">The root element of a Microsoft Visio document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="59878-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="59878-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="59878-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="59878-106">**Element type**</span></span> <br/> |[<span data-ttu-id="59878-107">Висиодокумент_типе</span><span class="sxs-lookup"><span data-stu-id="59878-107">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="59878-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="59878-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="59878-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="59878-109">**Schema file**</span></span> <br/> |<span data-ttu-id="59878-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="59878-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="59878-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="59878-111">**Document parts**</span></span> <br/> |<span data-ttu-id="59878-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="59878-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="59878-113">Определение</span><span class="sxs-lookup"><span data-stu-id="59878-113">Definition</span></span>

```XML
< xs:element name="VisioDocument" type="VisioDocument_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="59878-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="59878-114">Elements and attributes</span></span>

<span data-ttu-id="59878-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="59878-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="59878-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="59878-116">Parent elements</span></span>

<span data-ttu-id="59878-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="59878-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="59878-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="59878-118">Child elements</span></span>

|<span data-ttu-id="59878-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="59878-119">**Element**</span></span>|<span data-ttu-id="59878-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="59878-120">**Type**</span></span>|<span data-ttu-id="59878-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="59878-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="59878-122">Colors</span><span class="sxs-lookup"><span data-stu-id="59878-122">Colors</span></span>](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-123">Колорс_типе</span><span class="sxs-lookup"><span data-stu-id="59878-123">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-124">Содержит таблицу цветов документа.</span><span class="sxs-lookup"><span data-stu-id="59878-124">Contains the document's color table.</span></span>  <br/> |
|[<span data-ttu-id="59878-125">Документсеттингс</span><span class="sxs-lookup"><span data-stu-id="59878-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-126">Документсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="59878-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-127">Содержит элементы, определяющие параметры документа.</span><span class="sxs-lookup"><span data-stu-id="59878-127">Contains elements that specify document settings.</span></span>  <br/> |
|[<span data-ttu-id="59878-128">DocumentSheet</span><span class="sxs-lookup"><span data-stu-id="59878-128">DocumentSheet</span></span>](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-129">Документшит_типе</span><span class="sxs-lookup"><span data-stu-id="59878-129">DocumentSheet_Type</span></span>](documentsheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-130">Указывает структуру **таблицы свойств фигуры** .</span><span class="sxs-lookup"><span data-stu-id="59878-130">Specifies a document's **ShapeSheet** structure.</span></span>  <br/> |
|[<span data-ttu-id="59878-131">EventList</span><span class="sxs-lookup"><span data-stu-id="59878-131">EventList</span></span>](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-132">Евентлист_типе</span><span class="sxs-lookup"><span data-stu-id="59878-132">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-133">Содержит элемент **евентитем** для каждого события, на которое должен отвечать объект.</span><span class="sxs-lookup"><span data-stu-id="59878-133">Contains an **EventItem** element for each event to which an object should respond.</span></span>  <br/> |
|[<span data-ttu-id="59878-134">Фаценамес</span><span class="sxs-lookup"><span data-stu-id="59878-134">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-135">Фаценамес_типе</span><span class="sxs-lookup"><span data-stu-id="59878-135">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-136">Содержит коллекцию элементов **фаценаме** .</span><span class="sxs-lookup"><span data-stu-id="59878-136">Contains a collection of **FaceName** elements.</span></span>  <br/> |
|[<span data-ttu-id="59878-137">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="59878-137">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-138">Хеадерфутер_типе</span><span class="sxs-lookup"><span data-stu-id="59878-138">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-139">Содержит элементы для верхнего и нижнего колонтитулов документа.</span><span class="sxs-lookup"><span data-stu-id="59878-139">Contains elements for a document's header and footer.</span></span>  <br/> |
|[<span data-ttu-id="59878-140">Публишсеттингс</span><span class="sxs-lookup"><span data-stu-id="59878-140">PublishSettings</span></span>](publishsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-141">Публишсеттингс_типе</span><span class="sxs-lookup"><span data-stu-id="59878-141">PublishSettings_Type</span></span>](publishsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-142">Задает набор доступных для обновления и набора наборов записей, доступных для обновления в документе.</span><span class="sxs-lookup"><span data-stu-id="59878-142">Specifies the set of drawing pages that are viewable and set of recordsets that are refreshable in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="59878-143">StyleSheets</span><span class="sxs-lookup"><span data-stu-id="59878-143">StyleSheets</span></span>](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="59878-144">Стилешитс_типе</span><span class="sxs-lookup"><span data-stu-id="59878-144">StyleSheets_Type</span></span>](stylesheets_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="59878-145">Содержит коллекцию элементов StyleSheet для документа.</span><span class="sxs-lookup"><span data-stu-id="59878-145">Contains a collection of StyleSheet elements for the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="59878-146">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="59878-146">Attributes</span></span>

<span data-ttu-id="59878-147">Нет.</span><span class="sxs-lookup"><span data-stu-id="59878-147">None.</span></span>
  

