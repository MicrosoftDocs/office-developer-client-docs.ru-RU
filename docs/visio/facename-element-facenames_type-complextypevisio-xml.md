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
# <a name="facename-element-facenames_type-complextype-visio-xml"></a><span data-ttu-id="cb5cd-103">Элемент FaceName (FaceNames_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="cb5cd-103">FaceName element (FaceNames_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="cb5cd-104">Содержит сведения о шрифте.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-104">Contains information about a font.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cb5cd-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cb5cd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb5cd-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cb5cd-107">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="cb5cd-107">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cb5cd-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cb5cd-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cb5cd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cb5cd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cb5cd-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cb5cd-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="cb5cd-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cb5cd-113">Определение</span><span class="sxs-lookup"><span data-stu-id="cb5cd-113">Definition</span></span>

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cb5cd-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="cb5cd-114">Elements and attributes</span></span>

<span data-ttu-id="cb5cd-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cb5cd-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="cb5cd-116">Parent elements</span></span>

|<span data-ttu-id="cb5cd-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-117">**Element**</span></span>|<span data-ttu-id="cb5cd-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-118">**Type**</span></span>|<span data-ttu-id="cb5cd-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cb5cd-120">FaceNames</span><span class="sxs-lookup"><span data-stu-id="cb5cd-120">FaceNames</span></span>](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cb5cd-121">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="cb5cd-121">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cb5cd-122">Содержит коллекцию **элементов FaceName.**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-122">Contains a collection of **FaceName** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cb5cd-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cb5cd-123">Child elements</span></span>

<span data-ttu-id="cb5cd-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb5cd-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cb5cd-125">Attributes</span></span>

|<span data-ttu-id="cb5cd-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-126">**Attribute**</span></span>|<span data-ttu-id="cb5cd-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-127">**Type**</span></span>|<span data-ttu-id="cb5cd-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-128">**Required**</span></span>|<span data-ttu-id="cb5cd-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-129">**Description**</span></span>|<span data-ttu-id="cb5cd-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="cb5cd-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cb5cd-131">CharSets</span><span class="sxs-lookup"><span data-stu-id="cb5cd-131">CharSets</span></span>  <br/> |<span data-ttu-id="cb5cd-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb5cd-132">xsd:string</span></span>  <br/> |<span data-ttu-id="cb5cd-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="cb5cd-133">optional</span></span>  <br/> |<span data-ttu-id="cb5cd-134">Поддерживаемые наборы символов шрифта.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-134">The supported character sets of the font.</span></span>  <br/> |<span data-ttu-id="cb5cd-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb5cd-136">Flags</span><span class="sxs-lookup"><span data-stu-id="cb5cd-136">Flags</span></span>  <br/> |<span data-ttu-id="cb5cd-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cb5cd-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cb5cd-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="cb5cd-138">optional</span></span>  <br/> |<span data-ttu-id="cb5cd-139">Флаги, которые указывают на следующее: отсутствующий шрифт, шрифт по умолчанию, азиатский шрифт, сложный шрифт, вертикальный шрифт и тип шрифта.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-139">Flags that indicate the following: missing font, default font, asian font, complex font, vertical font, and font type.</span></span>  <br/> |<span data-ttu-id="cb5cd-140">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cb5cd-141">NameU</span><span class="sxs-lookup"><span data-stu-id="cb5cd-141">NameU</span></span>  <br/> |<span data-ttu-id="cb5cd-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb5cd-142">xsd:string</span></span>  <br/> |<span data-ttu-id="cb5cd-143">Обязательный</span><span class="sxs-lookup"><span data-stu-id="cb5cd-143">required</span></span>  <br/> |<span data-ttu-id="cb5cd-144">Имя шрифта в качестве строки UTF-16 Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-144">The name of the font as a UTF-16 Unicode string.</span></span>  <br/> ||
|<span data-ttu-id="cb5cd-145">Panos</span><span class="sxs-lookup"><span data-stu-id="cb5cd-145">Panos</span></span>  <br/> |<span data-ttu-id="cb5cd-146">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb5cd-146">xsd:string</span></span>  <br/> |<span data-ttu-id="cb5cd-147">необязательный</span><span class="sxs-lookup"><span data-stu-id="cb5cd-147">optional</span></span>  <br/> |<span data-ttu-id="cb5cd-148">Панацея для шрифта.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-148">The panose signature for the font.</span></span> <span data-ttu-id="cb5cd-149">Panose — это система классификации шрифтов, классифицирующая их в зависимости от их визуальных характеристик.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-149">Panose is a classification system for typefaces that categorizes them based upon their visual characteristics.</span></span>  <br/> |<span data-ttu-id="cb5cd-150">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-150">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="cb5cd-151">UnicodeRanges</span><span class="sxs-lookup"><span data-stu-id="cb5cd-151">UnicodeRanges</span></span>  <br/> |<span data-ttu-id="cb5cd-152">xsd:string</span><span class="sxs-lookup"><span data-stu-id="cb5cd-152">xsd:string</span></span>  <br/> |<span data-ttu-id="cb5cd-153">необязательный</span><span class="sxs-lookup"><span data-stu-id="cb5cd-153">optional</span></span>  <br/> |<span data-ttu-id="cb5cd-154">Поддерживаемые диапазоны Юникод шрифта.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-154">The supported Unicode ranges of the font.</span></span>  <br/> |<span data-ttu-id="cb5cd-155">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="cb5cd-155">Values of the xsd:string type.</span></span>  <br/> |
   

