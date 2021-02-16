---
title: Элемент FaceNames (VisioDocument_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 61e30f57-abd6-9378-45ed-51236ab3d3ee
description: Содержит коллекцию элементов FaceName.
ms.openlocfilehash: ce18847fdd46a0c703a0df5e8d8c7a877f864d35
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539715"
---
# <a name="facenames-element-visiodocument_type-complextype-visio-xml"></a><span data-ttu-id="4b496-103">Элемент FaceNames (VisioDocument_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4b496-103">FaceNames element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4b496-104">Содержит коллекцию **элементов FaceName.**</span><span class="sxs-lookup"><span data-stu-id="4b496-104">Contains a collection of **FaceName** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4b496-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4b496-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b496-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4b496-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4b496-107">FaceNames_Type</span><span class="sxs-lookup"><span data-stu-id="4b496-107">FaceNames_Type</span></span>](facenames_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4b496-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4b496-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4b496-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4b496-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4b496-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4b496-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4b496-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4b496-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4b496-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="4b496-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4b496-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4b496-113">Definition</span></span>

```XML
< xs:element name="FaceNames" type="FaceNames_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4b496-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4b496-114">Elements and attributes</span></span>

<span data-ttu-id="4b496-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4b496-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4b496-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4b496-116">Parent elements</span></span>

|<span data-ttu-id="4b496-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4b496-117">**Element**</span></span>|<span data-ttu-id="4b496-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4b496-118">**Type**</span></span>|<span data-ttu-id="4b496-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b496-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b496-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="4b496-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="4b496-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="4b496-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b496-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="4b496-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4b496-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4b496-123">Child elements</span></span>

|<span data-ttu-id="4b496-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4b496-124">**Element**</span></span>|<span data-ttu-id="4b496-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4b496-125">**Type**</span></span>|<span data-ttu-id="4b496-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4b496-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4b496-127">FaceName</span><span class="sxs-lookup"><span data-stu-id="4b496-127">FaceName</span></span>](facename-element-facenames_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4b496-128">FaceName_Type</span><span class="sxs-lookup"><span data-stu-id="4b496-128">FaceName_Type</span></span>](facename_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4b496-129">Содержит сведения о шрифте.</span><span class="sxs-lookup"><span data-stu-id="4b496-129">Contains information about a font.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4b496-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4b496-130">Attributes</span></span>

<span data-ttu-id="4b496-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="4b496-131">None.</span></span>
  

