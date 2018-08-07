---
title: Подключается элемент (PageContents_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Содержит элемент подключение для каждого подключения между двумя фигурами в документе.
ms.openlocfilehash: 93930a8f21f9d250bf24d821b0eeb4036f6fe187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813476"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="f1a27-103">Подключается элемент (PageContents_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f1a27-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f1a27-104">Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="f1a27-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f1a27-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f1a27-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1a27-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f1a27-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f1a27-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="f1a27-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f1a27-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f1a27-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f1a27-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f1a27-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f1a27-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f1a27-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f1a27-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f1a27-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f1a27-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="f1a27-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f1a27-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f1a27-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f1a27-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1a27-114">Elements and attributes</span></span>

<span data-ttu-id="f1a27-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="f1a27-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f1a27-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f1a27-116">Parent elements</span></span>

|<span data-ttu-id="f1a27-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f1a27-117">**Element**</span></span>|<span data-ttu-id="f1a27-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f1a27-118">**Type**</span></span>|<span data-ttu-id="f1a27-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1a27-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1a27-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="f1a27-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="f1a27-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="f1a27-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1a27-122">Задает сведения о фигурах в основной или рисования на странице рисунка.</span><span class="sxs-lookup"><span data-stu-id="f1a27-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="f1a27-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="f1a27-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="f1a27-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="f1a27-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1a27-125">Задает сведения о фигурах в основной или рисования на странице рисунка.</span><span class="sxs-lookup"><span data-stu-id="f1a27-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f1a27-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f1a27-126">Child elements</span></span>

|<span data-ttu-id="f1a27-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f1a27-127">**Element**</span></span>|<span data-ttu-id="f1a27-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f1a27-128">**Type**</span></span>|<span data-ttu-id="f1a27-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f1a27-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f1a27-130">Подключение</span><span class="sxs-lookup"><span data-stu-id="f1a27-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f1a27-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="f1a27-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f1a27-132">Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.</span><span class="sxs-lookup"><span data-stu-id="f1a27-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f1a27-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f1a27-133">Attributes</span></span>

<span data-ttu-id="f1a27-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="f1a27-134">None.</span></span>
  

