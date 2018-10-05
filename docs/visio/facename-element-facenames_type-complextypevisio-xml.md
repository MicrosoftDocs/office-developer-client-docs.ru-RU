---
title: Элемент название значка (FaceNames_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Содержит сведения о шрифта.
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389780"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a><span data-ttu-id="f3570-103">Элемент название значка (FaceNames_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f3570-103">FaceName element (FaceNames_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f3570-104">Содержит сведения о шрифта.</span><span class="sxs-lookup"><span data-stu-id="f3570-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f3570-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f3570-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f3570-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f3570-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f3570-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="f3570-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f3570-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f3570-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f3570-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f3570-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f3570-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f3570-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f3570-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f3570-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f3570-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="f3570-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f3570-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f3570-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f3570-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f3570-114">Elements and attributes</span></span>

<span data-ttu-id="f3570-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f3570-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f3570-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f3570-116">Parent elements</span></span>

|<span data-ttu-id="f3570-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f3570-117">**Element**</span></span>|<span data-ttu-id="f3570-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f3570-118">**Type**</span></span>|<span data-ttu-id="f3570-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f3570-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f3570-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="f3570-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f3570-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="f3570-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f3570-122">Содержит коллекцию элементов **Название значка** .</span><span class="sxs-lookup"><span data-stu-id="f3570-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f3570-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f3570-123">Child elements</span></span>

<span data-ttu-id="f3570-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="f3570-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f3570-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f3570-125">Attributes</span></span>

|<span data-ttu-id="f3570-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f3570-126">**Attribute**</span></span>|<span data-ttu-id="f3570-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f3570-127">**Type**</span></span>|<span data-ttu-id="f3570-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f3570-128">**Required**</span></span>|<span data-ttu-id="f3570-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f3570-129">**Description**</span></span>|<span data-ttu-id="f3570-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f3570-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f3570-131">Наборов символов</span><span class="sxs-lookup"><span data-stu-id="f3570-131">CharSets</span></span>  <br/> |<span data-ttu-id="f3570-132">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f3570-132">xsd:string</span></span>  <br/> |<span data-ttu-id="f3570-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="f3570-133">optional</span></span>  <br/> |<span data-ttu-id="f3570-134">Поддерживаемые кодировки шрифта.</span><span class="sxs-lookup"><span data-stu-id="f3570-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="f3570-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f3570-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3570-136">Флаги</span><span class="sxs-lookup"><span data-stu-id="f3570-136">Flags</span></span>  <br/> |<span data-ttu-id="f3570-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f3570-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f3570-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="f3570-138">optional</span></span>  <br/> |<span data-ttu-id="f3570-139">Флаги, указывающие следующее: отсутствующие шрифта, шрифта по умолчанию, азиатских шрифтов, сложных шрифтов, вертикальной шрифт и тип шрифта.</span><span class="sxs-lookup"><span data-stu-id="f3570-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="f3570-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f3570-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f3570-141">NameU</span><span class="sxs-lookup"><span data-stu-id="f3570-141">NameU</span></span>  <br/> |<span data-ttu-id="f3570-142">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f3570-142">xsd:string</span></span>  <br/> |<span data-ttu-id="f3570-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f3570-143">required</span></span>  <br/> |<span data-ttu-id="f3570-144">Имя шрифта строки Юникод UTF-16.</span><span class="sxs-lookup"><span data-stu-id="f3570-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="f3570-145">Panos</span><span class="sxs-lookup"><span data-stu-id="f3570-145">Panos</span></span>  <br/> |<span data-ttu-id="f3570-146">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f3570-146">xsd:string</span></span>  <br/> |<span data-ttu-id="f3570-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="f3570-147">optional</span></span>  <br/> |<span data-ttu-id="f3570-148">Подпись сходстве для шрифта.</span><span class="sxs-lookup"><span data-stu-id="f3570-148">The panose signature for the font.</span></span> <span data-ttu-id="f3570-149">Сходстве — это система классификации для гарнитуры, разделяет на их основе своих визуальных характеристик категории.</span><span class="sxs-lookup"><span data-stu-id="f3570-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="f3570-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f3570-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="f3570-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="f3570-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="f3570-152">XSD:String</span><span class="sxs-lookup"><span data-stu-id="f3570-152">xsd:string</span></span>  <br/> |<span data-ttu-id="f3570-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="f3570-153">optional</span></span>  <br/> |<span data-ttu-id="f3570-154">Поддерживаемые Диапазоны Юникода шрифта.</span><span class="sxs-lookup"><span data-stu-id="f3570-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="f3570-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="f3570-155">Values of the xsd:string type.</span></span>  <br/> |
   

