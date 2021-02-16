---
title: Элемент FaceName (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Содержит сведения о шрифте.
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541017"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a><span data-ttu-id="00640-103">Элемент FaceName (FaceNames_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="00640-103">FaceName element (FaceNames_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="00640-104">Содержит сведения о шрифте.</span><span class="sxs-lookup"><span data-stu-id="00640-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="00640-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="00640-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00640-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="00640-106">**Element type**</span></span> <br/> |[<span data-ttu-id="00640-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="00640-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="00640-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="00640-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="00640-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="00640-109">**Schema file**</span></span> <br/> |<span data-ttu-id="00640-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="00640-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="00640-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="00640-111">**Document parts**</span></span> <br/> |<span data-ttu-id="00640-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="00640-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="00640-113">Определение</span><span class="sxs-lookup"><span data-stu-id="00640-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="00640-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="00640-114">Elements and attributes</span></span>

<span data-ttu-id="00640-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="00640-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="00640-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="00640-116">Parent elements</span></span>

|<span data-ttu-id="00640-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="00640-117">**Element**</span></span>|<span data-ttu-id="00640-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="00640-118">**Type**</span></span>|<span data-ttu-id="00640-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00640-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="00640-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="00640-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="00640-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="00640-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="00640-122">Содержит коллекцию **элементов FaceName.**</span><span class="sxs-lookup"><span data-stu-id="00640-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="00640-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="00640-123">Child elements</span></span>

<span data-ttu-id="00640-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="00640-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00640-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="00640-125">Attributes</span></span>

|<span data-ttu-id="00640-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="00640-126">**Attribute**</span></span>|<span data-ttu-id="00640-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="00640-127">**Type**</span></span>|<span data-ttu-id="00640-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="00640-128">**Required**</span></span>|<span data-ttu-id="00640-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="00640-129">**Description**</span></span>|<span data-ttu-id="00640-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="00640-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="00640-131">CharSets</span><span class="sxs-lookup"><span data-stu-id="00640-131">CharSets</span></span>  <br/> |<span data-ttu-id="00640-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="00640-132">xsd:string</span></span>  <br/> |<span data-ttu-id="00640-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="00640-133">optional</span></span>  <br/> |<span data-ttu-id="00640-134">Поддерживаемые наборы символов шрифта.</span><span class="sxs-lookup"><span data-stu-id="00640-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="00640-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="00640-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="00640-136">Flags</span><span class="sxs-lookup"><span data-stu-id="00640-136">Flags</span></span>  <br/> |<span data-ttu-id="00640-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="00640-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="00640-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="00640-138">optional</span></span>  <br/> |<span data-ttu-id="00640-139">Флаги, которые указывают следующее: отсутствующий шрифт, шрифт по умолчанию, азиатский шрифт, сложный шрифт, вертикальный шрифт и тип шрифта.</span><span class="sxs-lookup"><span data-stu-id="00640-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="00640-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="00640-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="00640-141">NameU</span><span class="sxs-lookup"><span data-stu-id="00640-141">NameU</span></span>  <br/> |<span data-ttu-id="00640-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="00640-142">xsd:string</span></span>  <br/> |<span data-ttu-id="00640-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="00640-143">required</span></span>  <br/> |<span data-ttu-id="00640-144">Имя шрифта в качестве строки Юникода UTF-16.</span><span class="sxs-lookup"><span data-stu-id="00640-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="00640-145">Panos</span><span class="sxs-lookup"><span data-stu-id="00640-145">Panos</span></span>  <br/> |<span data-ttu-id="00640-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="00640-146">xsd:string</span></span>  <br/> |<span data-ttu-id="00640-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="00640-147">optional</span></span>  <br/> |<span data-ttu-id="00640-148">Подпись области для шрифта.</span><span class="sxs-lookup"><span data-stu-id="00640-148">The panose signature for the font.</span></span> <span data-ttu-id="00640-149">Panose — это система классификации шрифтов, классифицирующая их на основе их визуальных характеристик.</span><span class="sxs-lookup"><span data-stu-id="00640-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="00640-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="00640-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="00640-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="00640-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="00640-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="00640-152">xsd:string</span></span>  <br/> |<span data-ttu-id="00640-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="00640-153">optional</span></span>  <br/> |<span data-ttu-id="00640-154">Поддерживаемые диапазоны Юникод шрифта.</span><span class="sxs-lookup"><span data-stu-id="00640-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="00640-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="00640-155">Values of the xsd:string type.</span></span>  <br/> |
   

