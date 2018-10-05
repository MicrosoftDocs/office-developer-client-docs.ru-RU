---
title: Элемент цвета (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Содержит таблицы цветов документа.
ms.openlocfilehash: bd46f58dfbb8a596717662b9a0524d59bb508270
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400532"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="2764b-103">Элемент цвета (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="2764b-103">Colors element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2764b-104">Содержит таблицы цветов документа.</span><span class="sxs-lookup"><span data-stu-id="2764b-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2764b-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2764b-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2764b-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="2764b-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2764b-107">Colors_Type</span><span class="sxs-lookup"><span data-stu-id="2764b-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2764b-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2764b-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2764b-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2764b-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2764b-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2764b-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2764b-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="2764b-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2764b-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="2764b-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2764b-113">Определение</span><span class="sxs-lookup"><span data-stu-id="2764b-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2764b-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2764b-114">Elements and attributes</span></span>

<span data-ttu-id="2764b-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2764b-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2764b-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2764b-116">Parent elements</span></span>

|<span data-ttu-id="2764b-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2764b-117">**Element**</span></span>|<span data-ttu-id="2764b-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2764b-118">**Type**</span></span>|<span data-ttu-id="2764b-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2764b-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2764b-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="2764b-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="2764b-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="2764b-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2764b-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="2764b-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2764b-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2764b-123">Child elements</span></span>

|<span data-ttu-id="2764b-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2764b-124">**Element**</span></span>|<span data-ttu-id="2764b-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2764b-125">**Type**</span></span>|<span data-ttu-id="2764b-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2764b-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2764b-127">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="2764b-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2764b-128">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="2764b-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2764b-129">Содержит запись таблицы цвет.</span><span class="sxs-lookup"><span data-stu-id="2764b-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2764b-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2764b-130">Attributes</span></span>

<span data-ttu-id="2764b-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="2764b-131">None.</span></span>
  

