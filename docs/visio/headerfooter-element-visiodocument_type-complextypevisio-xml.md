---
title: Элемент HeaderFooter (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Содержит элементы для колонтитулов документа.
ms.openlocfilehash: eabb19100c4b37a546c0a271cfba5a0c865a7e83
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384446"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="192d5-103">Элемент HeaderFooter (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="192d5-103">HeaderFooter element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="192d5-104">Содержит элементы для колонтитулов документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="192d5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="192d5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="192d5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="192d5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="192d5-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="192d5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="192d5-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="192d5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="192d5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="192d5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="192d5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="192d5-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="192d5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="192d5-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="192d5-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="192d5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="192d5-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="192d5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="192d5-114">Elements and attributes</span></span>

<span data-ttu-id="192d5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="192d5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="192d5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="192d5-116">Parent elements</span></span>

|<span data-ttu-id="192d5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="192d5-117">**Element**</span></span>|<span data-ttu-id="192d5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="192d5-118">**Type**</span></span>|<span data-ttu-id="192d5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="192d5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="192d5-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="192d5-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="192d5-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="192d5-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="192d5-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="192d5-123">Child elements</span></span>

|<span data-ttu-id="192d5-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="192d5-124">**Element**</span></span>|<span data-ttu-id="192d5-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="192d5-125">**Type**</span></span>|<span data-ttu-id="192d5-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="192d5-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="192d5-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="192d5-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-129">Содержит строку текста, который отображается в центре части нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="192d5-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="192d5-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-132">Содержит текстовую строку, которая находится в левой части нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="192d5-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="192d5-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-135">Задает поле нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="192d5-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="192d5-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-138">Содержит строку текста, который отображается в правой части нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="192d5-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="192d5-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-141">Содержит строку текста, который отображается в центре части заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="192d5-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="192d5-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-144">Задает шрифт, используемый для текста верхнего и нижнего колонтитулов.</span><span class="sxs-lookup"><span data-stu-id="192d5-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="192d5-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="192d5-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-147">Содержит текстовую строку, которая находится в левой части заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="192d5-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="192d5-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-150">Задает поле заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="192d5-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="192d5-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="192d5-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="192d5-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="192d5-153">Содержит строку текста, который отображается в правой части заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="192d5-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="192d5-154">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="192d5-154">Attributes</span></span>

|<span data-ttu-id="192d5-155">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="192d5-155">**Attribute**</span></span>|<span data-ttu-id="192d5-156">**Тип**</span><span class="sxs-lookup"><span data-stu-id="192d5-156">**Type**</span></span>|<span data-ttu-id="192d5-157">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="192d5-157">**Required**</span></span>|<span data-ttu-id="192d5-158">**Описание**</span><span class="sxs-lookup"><span data-stu-id="192d5-158">**Description**</span></span>|<span data-ttu-id="192d5-159">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="192d5-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="192d5-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="192d5-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="192d5-161">XSD:String</span><span class="sxs-lookup"><span data-stu-id="192d5-161">xsd:string</span></span>  <br/> |<span data-ttu-id="192d5-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="192d5-162">optional</span></span>  <br/> |<span data-ttu-id="192d5-163">Значение RGB цвет текста для верхнего и нижнего колонтитулов в шестнадцатеричном формате; Например #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="192d5-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="192d5-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="192d5-164">Values of the xsd:string type.</span></span>  <br/> |
   

