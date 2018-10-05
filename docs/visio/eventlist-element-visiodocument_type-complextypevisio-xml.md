---
title: Элемент EventList (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Содержит элемент EventItem для каждого события, к которому должны отвечать объекта.
ms.openlocfilehash: 5331f1b4a510b05b862f8c7c6306c89c6be4d9f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383977"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="e1e1a-103">Элемент EventList (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e1e1a-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e1e1a-104">Содержит элемент **EventItem** для каждого события, к которому должны отвечать объекта.</span><span class="sxs-lookup"><span data-stu-id="e1e1a-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e1e1a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e1e1a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1e1a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e1e1a-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="e1e1a-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e1e1a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e1e1a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e1e1a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e1e1a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e1e1a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e1e1a-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="e1e1a-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e1e1a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e1e1a-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e1e1a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1e1a-114">Elements and attributes</span></span>

<span data-ttu-id="e1e1a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e1e1a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e1e1a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e1e1a-116">Parent elements</span></span>

|<span data-ttu-id="e1e1a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-117">**Element**</span></span>|<span data-ttu-id="e1e1a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-118">**Type**</span></span>|<span data-ttu-id="e1e1a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1e1a-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="e1e1a-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="e1e1a-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="e1e1a-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e1e1a-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="e1e1a-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e1e1a-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e1e1a-123">Child elements</span></span>

|<span data-ttu-id="e1e1a-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-124">**Element**</span></span>|<span data-ttu-id="e1e1a-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-125">**Type**</span></span>|<span data-ttu-id="e1e1a-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e1e1a-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e1e1a-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="e1e1a-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e1e1a-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="e1e1a-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e1e1a-129">Инкапсулирует код события.</span><span class="sxs-lookup"><span data-stu-id="e1e1a-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e1e1a-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1e1a-130">Attributes</span></span>

<span data-ttu-id="e1e1a-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="e1e1a-131">None.</span></span>
  

