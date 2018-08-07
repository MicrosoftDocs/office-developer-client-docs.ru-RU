---
title: Элемент EventList (VisioDocument_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40bb8c7c-89ef-22e1-5edf-e2423fc89660
description: Содержит элемент EventItem для каждого события, к которому должны отвечать объекта.
ms.openlocfilehash: e1033ae93ca272b8ea1d9855d08ad13a444612db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813699"
---
# <a name="eventlist-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="86a16-103">Элемент EventList (VisioDocument_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="86a16-103">EventList element (VisioDocument_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="86a16-104">Содержит элемент **EventItem** для каждого события, к которому должны отвечать объекта.</span><span class="sxs-lookup"><span data-stu-id="86a16-104">Contains an **EventItem** element for each event to which an object should respond.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="86a16-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="86a16-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86a16-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="86a16-106">**Element type**</span></span> <br/> |[<span data-ttu-id="86a16-107">EventList_Type</span><span class="sxs-lookup"><span data-stu-id="86a16-107">EventList_Type</span></span>](eventlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="86a16-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="86a16-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="86a16-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="86a16-109">**Schema file**</span></span> <br/> |<span data-ttu-id="86a16-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="86a16-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="86a16-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="86a16-111">**Document parts**</span></span> <br/> |<span data-ttu-id="86a16-112">Document.XML</span><span class="sxs-lookup"><span data-stu-id="86a16-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86a16-113">Определение</span><span class="sxs-lookup"><span data-stu-id="86a16-113">Definition</span></span>

```XML
< xs:element name="EventList" type="EventList_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="86a16-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="86a16-114">Elements and attributes</span></span>

<span data-ttu-id="86a16-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="86a16-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="86a16-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="86a16-116">Parent elements</span></span>

|<span data-ttu-id="86a16-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="86a16-117">**Element**</span></span>|<span data-ttu-id="86a16-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="86a16-118">**Type**</span></span>|<span data-ttu-id="86a16-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="86a16-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86a16-120">VisioDocument</span><span class="sxs-lookup"><span data-stu-id="86a16-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="86a16-121">VisioDocument_Type</span><span class="sxs-lookup"><span data-stu-id="86a16-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86a16-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="86a16-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="86a16-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="86a16-123">Child elements</span></span>

|<span data-ttu-id="86a16-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="86a16-124">**Element**</span></span>|<span data-ttu-id="86a16-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="86a16-125">**Type**</span></span>|<span data-ttu-id="86a16-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="86a16-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="86a16-127">EventItem</span><span class="sxs-lookup"><span data-stu-id="86a16-127">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="86a16-128">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="86a16-128">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="86a16-129">Инкапсулирует код события.</span><span class="sxs-lookup"><span data-stu-id="86a16-129">Encapsulates an event code.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="86a16-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="86a16-130">Attributes</span></span>

<span data-ttu-id="86a16-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="86a16-131">None.</span></span>
  

