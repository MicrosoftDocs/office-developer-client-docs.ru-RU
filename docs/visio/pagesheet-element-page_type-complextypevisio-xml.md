---
title: Элемент PageSheet (Page_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 99a6549b-099b-1546-cc30-db0010fe3ce1
description: Указывает свойства страницы рисования, связанные со страницей рисования.
ms.openlocfilehash: 2f49d152a0fcb30e3f5aea98cdc251d3b65b8f69
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540625"
---
# <a name="pagesheet-element-page_type-complextype-visio-xml"></a><span data-ttu-id="02089-103">Элемент PageSheet (Page_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="02089-103">PageSheet element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="02089-104">Указывает свойства страницы рисования, связанные со страницей рисования.</span><span class="sxs-lookup"><span data-stu-id="02089-104">Specifies the properties of the drawing page associated with the drawing page.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02089-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="02089-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02089-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="02089-106">**Element type**</span></span> <br/> |[<span data-ttu-id="02089-107">PageSheet_Type</span><span class="sxs-lookup"><span data-stu-id="02089-107">PageSheet_Type</span></span>](pagesheet_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="02089-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="02089-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="02089-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="02089-109">**Schema file**</span></span> <br/> |<span data-ttu-id="02089-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="02089-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="02089-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="02089-111">**Document parts**</span></span> <br/> |<span data-ttu-id="02089-112">pages.xml</span><span class="sxs-lookup"><span data-stu-id="02089-112">pages.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02089-113">Определение</span><span class="sxs-lookup"><span data-stu-id="02089-113">Definition</span></span>

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02089-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="02089-114">Elements and attributes</span></span>

<span data-ttu-id="02089-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="02089-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="02089-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="02089-116">Parent elements</span></span>

|<span data-ttu-id="02089-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="02089-117">**Element**</span></span>|<span data-ttu-id="02089-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="02089-118">**Type**</span></span>|<span data-ttu-id="02089-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02089-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02089-120">Page</span><span class="sxs-lookup"><span data-stu-id="02089-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02089-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="02089-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02089-122">Содержит элементы, определяющие страницу в документе.</span><span class="sxs-lookup"><span data-stu-id="02089-122">Contains elements that define a page in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02089-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="02089-123">Child elements</span></span>

<span data-ttu-id="02089-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="02089-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="02089-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="02089-125">Attributes</span></span>

|<span data-ttu-id="02089-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="02089-126">**Attribute**</span></span>|<span data-ttu-id="02089-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="02089-127">**Type**</span></span>|<span data-ttu-id="02089-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="02089-128">**Required**</span></span>|<span data-ttu-id="02089-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02089-129">**Description**</span></span>|<span data-ttu-id="02089-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="02089-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="02089-131">FillStyle</span><span class="sxs-lookup"><span data-stu-id="02089-131">FillStyle</span></span>  <br/> |<span data-ttu-id="02089-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02089-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02089-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="02089-133">optional</span></span>  <br/> |<span data-ttu-id="02089-134">Указывает ID листа стилей, из которого можно наследовать форматирование заполнения.</span><span class="sxs-lookup"><span data-stu-id="02089-134">Specifies the ID of the style sheet from which to inherit fill formatting.</span></span> <span data-ttu-id="02089-135">Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.</span><span class="sxs-lookup"><span data-stu-id="02089-135">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="02089-136">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="02089-136">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02089-137">LineStyle</span><span class="sxs-lookup"><span data-stu-id="02089-137">LineStyle</span></span>  <br/> |<span data-ttu-id="02089-138">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02089-138">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02089-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="02089-139">optional</span></span>  <br/> |<span data-ttu-id="02089-140">Указывает ID листа стилей, из которого можно наследовать форматирование строки.</span><span class="sxs-lookup"><span data-stu-id="02089-140">Specifies the ID of the style sheet from which to inherit line formatting.</span></span> <span data-ttu-id="02089-141">Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.</span><span class="sxs-lookup"><span data-stu-id="02089-141">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="02089-142">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="02089-142">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02089-143">TextStyle</span><span class="sxs-lookup"><span data-stu-id="02089-143">TextStyle</span></span>  <br/> |<span data-ttu-id="02089-144">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="02089-144">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="02089-145">необязательный</span><span class="sxs-lookup"><span data-stu-id="02089-145">optional</span></span>  <br/> |<span data-ttu-id="02089-146">Указывает ID листа стилей, из которого можно наследовать форматирование текста.</span><span class="sxs-lookup"><span data-stu-id="02089-146">Specifies the ID of the style sheet from which to inherit text formatting.</span></span> <span data-ttu-id="02089-147">Это должно быть значение атрибута **ID,** связанного с StyleSheet_Type **в** рисунке.</span><span class="sxs-lookup"><span data-stu-id="02089-147">It MUST be the value of the **ID** attribute associated with a **StyleSheet_Type** in the drawing.</span></span>  <br/> |<span data-ttu-id="02089-148">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="02089-148">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="02089-149">UniqueID</span><span class="sxs-lookup"><span data-stu-id="02089-149">UniqueID</span></span>  <br/> |<span data-ttu-id="02089-150">xsd:string</span><span class="sxs-lookup"><span data-stu-id="02089-150">xsd:string</span></span>  <br/> |<span data-ttu-id="02089-151">необязательный</span><span class="sxs-lookup"><span data-stu-id="02089-151">optional</span></span>  <br/> |<span data-ttu-id="02089-152">Уникальный ID элемента в родительском элементе.</span><span class="sxs-lookup"><span data-stu-id="02089-152">The unique ID of the element within its parent element.</span></span>  <br/> |<span data-ttu-id="02089-153">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="02089-153">Values of the xsd:string type.</span></span>  <br/> |
   

