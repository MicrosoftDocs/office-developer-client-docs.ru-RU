---
title: Элемент FaceNames (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Содержит коллекцию элементов название значка.
ms.openlocfilehash: 1c031d589883f34bbf9d69a3d537b82e1ecf3129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813738"
---
# <a name="facenames-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="313bc-103">Элемент FaceNames (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="313bc-103">FaceNames element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="313bc-104">Содержит коллекцию элементов **Название значка** .</span><span class="sxs-lookup"><span data-stu-id="313bc-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="313bc-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="313bc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="313bc-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="313bc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="313bc-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="313bc-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="313bc-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="313bc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="313bc-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="313bc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="313bc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="313bc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="313bc-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="313bc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="313bc-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="313bc-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="313bc-113">Определение</span><span class="sxs-lookup"><span data-stu-id="313bc-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="313bc-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="313bc-114">Elements and attributes</span></span>

<span data-ttu-id="313bc-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="313bc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="313bc-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="313bc-116">Parent elements</span></span>

|<span data-ttu-id="313bc-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="313bc-117">**Element**</span></span>|<span data-ttu-id="313bc-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="313bc-118">**Type**</span></span>|<span data-ttu-id="313bc-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="313bc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="313bc-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="313bc-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="313bc-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="313bc-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="313bc-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="313bc-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="313bc-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="313bc-123">Child elements</span></span>

|<span data-ttu-id="313bc-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="313bc-124">**Element**</span></span>|<span data-ttu-id="313bc-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="313bc-125">**Type**</span></span>|<span data-ttu-id="313bc-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="313bc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="313bc-127">Название значка</span><span class="sxs-lookup"><span data-stu-id="313bc-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="313bc-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="313bc-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="313bc-129">Содержит сведения о шрифта.</span><span class="sxs-lookup"><span data-stu-id="313bc-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="313bc-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="313bc-130">Attributes</span></span>

<span data-ttu-id="313bc-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="313bc-131">None.</span></span>
  

