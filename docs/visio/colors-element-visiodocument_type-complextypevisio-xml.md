---
title: Элемент цвета (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Содержит таблицы цветов документа.
ms.openlocfilehash: d13690ce6e1772ab1a43e697e8b99c0776a204b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813406"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="020c3-103">Элемент цвета (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="020c3-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="020c3-104">Содержит таблицы цветов документа.</span><span class="sxs-lookup"><span data-stu-id="020c3-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="020c3-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="020c3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="020c3-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="020c3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="020c3-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="020c3-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="020c3-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="020c3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="020c3-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="020c3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="020c3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="020c3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="020c3-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="020c3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="020c3-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="020c3-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="020c3-113">Определение</span><span class="sxs-lookup"><span data-stu-id="020c3-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="020c3-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="020c3-114">Elements and attributes</span></span>

<span data-ttu-id="020c3-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="020c3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="020c3-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="020c3-116">Parent elements</span></span>

|<span data-ttu-id="020c3-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="020c3-117">**Element**</span></span>|<span data-ttu-id="020c3-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="020c3-118">**Type**</span></span>|<span data-ttu-id="020c3-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="020c3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="020c3-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="020c3-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="020c3-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="020c3-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="020c3-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="020c3-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="020c3-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="020c3-123">Child elements</span></span>

|<span data-ttu-id="020c3-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="020c3-124">**Element**</span></span>|<span data-ttu-id="020c3-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="020c3-125">**Type**</span></span>|<span data-ttu-id="020c3-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="020c3-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="020c3-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="020c3-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="020c3-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="020c3-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="020c3-129">Содержит запись таблицы цвет.</span><span class="sxs-lookup"><span data-stu-id="020c3-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="020c3-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="020c3-130">Attributes</span></span>

<span data-ttu-id="020c3-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="020c3-131">None.</span></span>
  

