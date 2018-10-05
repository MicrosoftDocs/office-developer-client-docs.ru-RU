---
title: Элемент FaceNames (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Содержит коллекцию элементов название значка.
ms.openlocfilehash: 5d6f2ffbf54dd04e744e85909fbc8a6bd4a387a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386819"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="263a0-103">Элемент FaceNames (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="263a0-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="263a0-104">Содержит коллекцию элементов **Название значка** .</span><span class="sxs-lookup"><span data-stu-id="263a0-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="263a0-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="263a0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="263a0-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="263a0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="263a0-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="263a0-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="263a0-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="263a0-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="263a0-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="263a0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="263a0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="263a0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="263a0-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="263a0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="263a0-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="263a0-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="263a0-113">Определение</span><span class="sxs-lookup"><span data-stu-id="263a0-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="263a0-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="263a0-114">Elements and attributes</span></span>

<span data-ttu-id="263a0-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="263a0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="263a0-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="263a0-116">Parent elements</span></span>

|<span data-ttu-id="263a0-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="263a0-117">**Element**</span></span>|<span data-ttu-id="263a0-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="263a0-118">**Type**</span></span>|<span data-ttu-id="263a0-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="263a0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="263a0-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="263a0-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="263a0-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="263a0-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="263a0-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="263a0-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="263a0-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="263a0-123">Child elements</span></span>

|<span data-ttu-id="263a0-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="263a0-124">**Element**</span></span>|<span data-ttu-id="263a0-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="263a0-125">**Type**</span></span>|<span data-ttu-id="263a0-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="263a0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="263a0-127">Название значка</span><span class="sxs-lookup"><span data-stu-id="263a0-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="263a0-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="263a0-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="263a0-129">Содержит сведения о шрифта.</span><span class="sxs-lookup"><span data-stu-id="263a0-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="263a0-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="263a0-130">Attributes</span></span>

<span data-ttu-id="263a0-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="263a0-131">None.</span></span>
  

