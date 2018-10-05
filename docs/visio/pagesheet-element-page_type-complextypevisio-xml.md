---
title: Элемент PageSheet (Page_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Задает свойства страницы рисунка, связанного с странице документа.
ms.openlocfilehash: 8b60795c02717e4b752c09af19fa932f87924d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395135"
---
# <a name="pagesheet-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="9ac89-103">Элемент PageSheet (Page_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="9ac89-103">PageSheet element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="9ac89-104">Задает свойства страницы рисунка, связанного с странице документа.</span><span class="sxs-lookup"><span data-stu-id="9ac89-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ac89-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="9ac89-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ac89-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="9ac89-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9ac89-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9ac89-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="9ac89-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9ac89-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="9ac89-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9ac89-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9ac89-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="9ac89-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="9ac89-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="9ac89-111">**Document parts**</span></span> <br/> |<span data-ttu-id="9ac89-112">Pages.XML</span><span class="sxs-lookup"><span data-stu-id="9ac89-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ac89-113">Определение</span><span class="sxs-lookup"><span data-stu-id="9ac89-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ac89-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9ac89-114">Elements and attributes</span></span>

<span data-ttu-id="9ac89-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9ac89-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9ac89-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="9ac89-116">Parent elements</span></span>

|<span data-ttu-id="9ac89-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9ac89-117">**Element**</span></span>|<span data-ttu-id="9ac89-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9ac89-118">**Type**</span></span>|<span data-ttu-id="9ac89-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9ac89-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ac89-120">Страница</span><span class="sxs-lookup"><span data-stu-id="9ac89-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ac89-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="9ac89-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="9ac89-122">Содержит элементы, определяющие страницы в документе.</span><span class="sxs-lookup"><span data-stu-id="9ac89-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9ac89-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9ac89-123">Child elements</span></span>

<span data-ttu-id="9ac89-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="9ac89-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ac89-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9ac89-125">Attributes</span></span>

|<span data-ttu-id="9ac89-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="9ac89-126">**Attribute**</span></span>|<span data-ttu-id="9ac89-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9ac89-127">**Type**</span></span>|<span data-ttu-id="9ac89-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="9ac89-128">**Required**</span></span>|<span data-ttu-id="9ac89-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9ac89-129">**Description**</span></span>|<span data-ttu-id="9ac89-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="9ac89-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ac89-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="9ac89-131">FillStyle</span></span>  <br/> |<span data-ttu-id="9ac89-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ac89-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ac89-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="9ac89-133">optional</span></span>  <br/> |<span data-ttu-id="9ac89-134">Задает идентификатор таблицы стилей для наследования заливки форматирования.</span><span class="sxs-lookup"><span data-stu-id="9ac89-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="9ac89-135">Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.</span><span class="sxs-lookup"><span data-stu-id="9ac89-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="9ac89-136">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ac89-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ac89-137">Стиль линии</span><span class="sxs-lookup"><span data-stu-id="9ac89-137">LineStyle</span></span>  <br/> |<span data-ttu-id="9ac89-138">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ac89-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ac89-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="9ac89-139">optional</span></span>  <br/> |<span data-ttu-id="9ac89-140">Задает идентификатор таблицы стилей для наследования форматирование линий.</span><span class="sxs-lookup"><span data-stu-id="9ac89-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="9ac89-141">Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.</span><span class="sxs-lookup"><span data-stu-id="9ac89-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="9ac89-142">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ac89-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ac89-143">Стиля текста</span><span class="sxs-lookup"><span data-stu-id="9ac89-143">TextStyle</span></span>  <br/> |<span data-ttu-id="9ac89-144">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ac89-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ac89-145">необязательный</span><span class="sxs-lookup"><span data-stu-id="9ac89-145">optional</span></span>  <br/> |<span data-ttu-id="9ac89-146">Задает идентификатор таблицы стилей для наследования форматирование текста.</span><span class="sxs-lookup"><span data-stu-id="9ac89-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="9ac89-147">Оно должно быть значение атрибута **ID** , связанный с **StyleSheet_Type** в документе.</span><span class="sxs-lookup"><span data-stu-id="9ac89-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="9ac89-148">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ac89-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ac89-149">Уникальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="9ac89-149">UniqueID</span></span>  <br/> |<span data-ttu-id="9ac89-150">XSD:String</span><span class="sxs-lookup"><span data-stu-id="9ac89-150">xsd:string</span></span>  <br/> |<span data-ttu-id="9ac89-151">необязательный</span><span class="sxs-lookup"><span data-stu-id="9ac89-151">optional</span></span>  <br/> |<span data-ttu-id="9ac89-152">Уникальный идентификатор элемента в рамках родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="9ac89-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="9ac89-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9ac89-153">Values of the xsd:string type.</span></span>  <br/> |
   

