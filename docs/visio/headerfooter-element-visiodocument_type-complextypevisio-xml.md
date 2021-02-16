---
title: Элемент HeaderFooter (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Содержит элементы для опорного и footer-элементов документа.
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541108"
---
# <a name="headerfooter-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="8ed88-103">Элемент HeaderFooter (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8ed88-103">HeaderFooter element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8ed88-104">Содержит элементы для опорного и footer-элементов документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8ed88-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8ed88-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8ed88-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="8ed88-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8ed88-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8ed88-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8ed88-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8ed88-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8ed88-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8ed88-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="8ed88-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8ed88-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="8ed88-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8ed88-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="8ed88-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8ed88-113">Определение</span><span class="sxs-lookup"><span data-stu-id="8ed88-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8ed88-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8ed88-114">Elements and attributes</span></span>

<span data-ttu-id="8ed88-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8ed88-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8ed88-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8ed88-116">Parent elements</span></span>

|<span data-ttu-id="8ed88-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8ed88-117">**Element**</span></span>|<span data-ttu-id="8ed88-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8ed88-118">**Type**</span></span>|<span data-ttu-id="8ed88-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ed88-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ed88-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="8ed88-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="8ed88-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="8ed88-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8ed88-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8ed88-123">Child elements</span></span>

|<span data-ttu-id="8ed88-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8ed88-124">**Element**</span></span>|<span data-ttu-id="8ed88-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8ed88-125">**Type**</span></span>|<span data-ttu-id="8ed88-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ed88-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8ed88-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="8ed88-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-129">Содержит текстовую строку, которая отображается в центральной части footer документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="8ed88-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-132">Содержит текстовую строку, которая отображается в левой части footer документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="8ed88-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-135">Указывает поле для footer документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="8ed88-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-138">Содержит текстовую строку, которая отображается в правой части footer документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="8ed88-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-141">Содержит текстовую строку, которая отображается в центральной части загона документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="8ed88-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-144">Указывает шрифт, используемый для текста в окне и в конце.</span><span class="sxs-lookup"><span data-stu-id="8ed88-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="8ed88-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-147">Содержит текстовую строку, которая отображается в левой части загона документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="8ed88-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-150">Указывает поле для загона документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="8ed88-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="8ed88-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8ed88-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="8ed88-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8ed88-153">Содержит текстовую строку, которая отображается в правой части загона документа.</span><span class="sxs-lookup"><span data-stu-id="8ed88-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8ed88-154">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8ed88-154">Attributes</span></span>

|<span data-ttu-id="8ed88-155">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8ed88-155">**Attribute**</span></span>|<span data-ttu-id="8ed88-156">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8ed88-156">**Type**</span></span>|<span data-ttu-id="8ed88-157">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8ed88-157">**Required**</span></span>|<span data-ttu-id="8ed88-158">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8ed88-158">**Description**</span></span>|<span data-ttu-id="8ed88-159">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8ed88-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8ed88-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="8ed88-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="8ed88-161">xsd:string</span><span class="sxs-lookup"><span data-stu-id="8ed88-161">xsd:string</span></span>  <br/> |<span data-ttu-id="8ed88-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="8ed88-162">optional</span></span>  <br/> |<span data-ttu-id="8ed88-163">RGB-значение цвета текста для опорного и footer в виде гистистических нотации; например, #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="8ed88-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="8ed88-164">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="8ed88-164">Values of the xsd:string type.</span></span>  <br/> |
   

