---
title: Элемент HeaderFooter (VisioDocument_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: Содержит элементы для верхнего и нижнего колонтитулов документа.
ms.openlocfilehash: c3c2f0adab4448ca88e5f2cca5605f397c48bd98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541108"
---
# <a name="headerfooter-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="8a361-103">Элемент HeaderFooter (VisioDocument_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8a361-103">HeaderFooter element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="8a361-104">Содержит элементы для верхнего и нижнего колонтитулов документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-104">Contains elements for a document's header and footer.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8a361-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8a361-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8a361-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="8a361-106">**Element type**</span></span> <br/> |[<span data-ttu-id="8a361-107">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-107">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="8a361-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8a361-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="8a361-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8a361-109">**Schema file**</span></span> <br/> |<span data-ttu-id="8a361-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="8a361-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="8a361-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="8a361-111">**Document parts**</span></span> <br/> |<span data-ttu-id="8a361-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="8a361-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8a361-113">Определение</span><span class="sxs-lookup"><span data-stu-id="8a361-113">Definition</span></span>

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8a361-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8a361-114">Elements and attributes</span></span>

<span data-ttu-id="8a361-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8a361-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="8a361-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="8a361-116">Parent elements</span></span>

|<span data-ttu-id="8a361-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8a361-117">**Element**</span></span>|<span data-ttu-id="8a361-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8a361-118">**Type**</span></span>|<span data-ttu-id="8a361-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8a361-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8a361-120">висиодокумент</span><span class="sxs-lookup"><span data-stu-id="8a361-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="8a361-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="8a361-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8a361-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8a361-123">Child elements</span></span>

|<span data-ttu-id="8a361-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8a361-124">**Element**</span></span>|<span data-ttu-id="8a361-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8a361-125">**Type**</span></span>|<span data-ttu-id="8a361-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8a361-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8a361-127">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="8a361-127">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-128">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-128">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-129">Содержит текстовую строку, которая отображается в центральной части нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-129">Contains the text string that appears in the center portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8a361-130">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="8a361-130">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-131">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-131">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-132">Содержит текстовую строку, которая отображается в левой части нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-132">Contains the text string that appears in the left portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8a361-133">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="8a361-133">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-134">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-134">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-135">Задает поля нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-135">Specifies the margin of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8a361-136">FooterRight</span><span class="sxs-lookup"><span data-stu-id="8a361-136">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-137">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-137">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-138">Содержит текстовую строку, которая отображается в правой части нижнего колонтитула документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-138">Contains the text string that appears in the right portion of a document's footer.</span></span>  <br/> |
|[<span data-ttu-id="8a361-139">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="8a361-139">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-140">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-140">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-141">Содержит текстовую строку, которая отображается в центральной части заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-141">Contains the text string that appears in the center portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="8a361-142">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="8a361-142">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-143">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-143">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-144">Задает шрифт, используемый для текста верхнего и нижнего колонтитулов.</span><span class="sxs-lookup"><span data-stu-id="8a361-144">Specifies the font used for the header and footer text.</span></span>  <br/> |
|[<span data-ttu-id="8a361-145">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="8a361-145">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-146">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-146">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-147">Содержит текстовую строку, которая отображается в левой части заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-147">Contains the text string that appears in the left portion of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="8a361-148">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="8a361-148">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-149">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-149">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-150">Задает поле заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-150">Specifies the margin of a document's header.</span></span>  <br/> |
|[<span data-ttu-id="8a361-151">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="8a361-151">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8a361-152">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="8a361-152">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="8a361-153">Содержит текстовую строку, которая отображается в правой части заголовка документа.</span><span class="sxs-lookup"><span data-stu-id="8a361-153">Contains the text string that appears in the right portion of a document's header.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="8a361-154">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8a361-154">Attributes</span></span>

|<span data-ttu-id="8a361-155">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8a361-155">**Attribute**</span></span>|<span data-ttu-id="8a361-156">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8a361-156">**Type**</span></span>|<span data-ttu-id="8a361-157">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8a361-157">**Required**</span></span>|<span data-ttu-id="8a361-158">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8a361-158">**Description**</span></span>|<span data-ttu-id="8a361-159">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8a361-159">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8a361-160">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="8a361-160">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="8a361-161">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="8a361-161">xsd:string</span></span>  <br/> |<span data-ttu-id="8a361-162">необязательный</span><span class="sxs-lookup"><span data-stu-id="8a361-162">optional</span></span>  <br/> |<span data-ttu-id="8a361-163">Значение RGB цвета текста для верхнего и нижнего колонтитулов в шестнадцатеричной нотации; Например, #rrggbb.</span><span class="sxs-lookup"><span data-stu-id="8a361-163">The RGB value of the text color for the header and footer in hexadecimal notation; for example, #rrggbb.</span></span>  <br/> |<span data-ttu-id="8a361-164">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="8a361-164">Values of the xsd:string type.</span></span>  <br/> |
   

