---
title: Элемент PageSheet (Page_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Задает свойства страницы документа, связанной со страницей документа.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540625"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a><span data-ttu-id="240ba-103">Элемент PageSheet (Page_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="240ba-103">PageSheet element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="240ba-104">Задает свойства страницы документа, связанной со страницей документа.</span><span class="sxs-lookup"><span data-stu-id="240ba-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="240ba-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="240ba-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="240ba-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="240ba-106">**Element type**</span></span> <br/> |[<span data-ttu-id="240ba-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="240ba-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="240ba-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="240ba-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="240ba-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="240ba-109">**Schema file**</span></span> <br/> |<span data-ttu-id="240ba-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="240ba-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="240ba-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="240ba-111">**Document parts**</span></span> <br/> |<span data-ttu-id="240ba-112">Pages. XML</span><span class="sxs-lookup"><span data-stu-id="240ba-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="240ba-113">Определение</span><span class="sxs-lookup"><span data-stu-id="240ba-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="240ba-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="240ba-114">Elements and attributes</span></span>

<span data-ttu-id="240ba-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="240ba-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="240ba-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="240ba-116">Parent elements</span></span>

|<span data-ttu-id="240ba-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="240ba-117">**Element**</span></span>|<span data-ttu-id="240ba-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="240ba-118">**Type**</span></span>|<span data-ttu-id="240ba-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="240ba-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="240ba-120">Page</span><span class="sxs-lookup"><span data-stu-id="240ba-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="240ba-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="240ba-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="240ba-122">Содержит элементы, определяющие страницу в документе.</span><span class="sxs-lookup"><span data-stu-id="240ba-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="240ba-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="240ba-123">Child elements</span></span>

<span data-ttu-id="240ba-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="240ba-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="240ba-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="240ba-125">Attributes</span></span>

|<span data-ttu-id="240ba-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="240ba-126">**Attribute**</span></span>|<span data-ttu-id="240ba-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="240ba-127">**Type**</span></span>|<span data-ttu-id="240ba-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="240ba-128">**Required**</span></span>|<span data-ttu-id="240ba-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="240ba-129">**Description**</span></span>|<span data-ttu-id="240ba-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="240ba-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="240ba-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="240ba-131">FillStyle</span></span>  <br/> |<span data-ttu-id="240ba-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="240ba-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="240ba-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="240ba-133">optional</span></span>  <br/> |<span data-ttu-id="240ba-134">Указывает идентификатор таблицы стилей, из которой требуется наследовать форматирование заливки.</span><span class="sxs-lookup"><span data-stu-id="240ba-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="240ba-135">Он должен быть значением атрибута **ID** , связанным с **StyleSheet_Type** в документе.</span><span class="sxs-lookup"><span data-stu-id="240ba-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="240ba-136">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="240ba-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="240ba-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="240ba-137">LineStyle</span></span>  <br/> |<span data-ttu-id="240ba-138">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="240ba-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="240ba-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="240ba-139">optional</span></span>  <br/> |<span data-ttu-id="240ba-140">Задает идентификатор таблицы стилей, из которой наследуются форматирование линий.</span><span class="sxs-lookup"><span data-stu-id="240ba-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="240ba-141">Он должен быть значением атрибута **ID** , связанным с **StyleSheet_Type** в документе.</span><span class="sxs-lookup"><span data-stu-id="240ba-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="240ba-142">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="240ba-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="240ba-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="240ba-143">TextStyle</span></span>  <br/> |<span data-ttu-id="240ba-144">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="240ba-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="240ba-145">необязательный</span><span class="sxs-lookup"><span data-stu-id="240ba-145">optional</span></span>  <br/> |<span data-ttu-id="240ba-146">Задает идентификатор таблицы стилей, из которой требуется наследовать форматирование текста.</span><span class="sxs-lookup"><span data-stu-id="240ba-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="240ba-147">Он должен быть значением атрибута **ID** , связанным с **StyleSheet_Type** в документе.</span><span class="sxs-lookup"><span data-stu-id="240ba-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="240ba-148">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="240ba-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="240ba-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="240ba-149">UniqueID</span></span>  <br/> |<span data-ttu-id="240ba-150">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="240ba-150">xsd:string</span></span>  <br/> |<span data-ttu-id="240ba-151">необязательный</span><span class="sxs-lookup"><span data-stu-id="240ba-151">optional</span></span>  <br/> |<span data-ttu-id="240ba-152">Уникальный идентификатор элемента в родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="240ba-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="240ba-153">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="240ba-153">Values of the xsd:string type.</span></span>  <br/> |
   

