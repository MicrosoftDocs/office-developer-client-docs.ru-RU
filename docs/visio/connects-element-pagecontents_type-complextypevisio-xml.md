---
title: Подключается элемент (PageContents_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Содержит элемент подключение для каждого подключения между двумя фигурами в документе.
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399958"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="c1f70-103">Подключается элемент (PageContents_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c1f70-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c1f70-104">Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="c1f70-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c1f70-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c1f70-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1f70-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c1f70-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c1f70-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="c1f70-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c1f70-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c1f70-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c1f70-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c1f70-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c1f70-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c1f70-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c1f70-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c1f70-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c1f70-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="c1f70-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c1f70-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c1f70-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c1f70-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c1f70-114">Elements and attributes</span></span>

<span data-ttu-id="c1f70-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c1f70-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c1f70-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c1f70-116">Parent elements</span></span>

|<span data-ttu-id="c1f70-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c1f70-117">**Element**</span></span>|<span data-ttu-id="c1f70-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c1f70-118">**Type**</span></span>|<span data-ttu-id="c1f70-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c1f70-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1f70-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="c1f70-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c1f70-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c1f70-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1f70-122">Задает сведения о фигурах в основной или рисования на странице рисунка.</span><span class="sxs-lookup"><span data-stu-id="c1f70-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="c1f70-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="c1f70-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c1f70-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c1f70-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1f70-125">Задает сведения о фигурах в основной или рисования на странице рисунка.</span><span class="sxs-lookup"><span data-stu-id="c1f70-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c1f70-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c1f70-126">Child elements</span></span>

|<span data-ttu-id="c1f70-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c1f70-127">**Element**</span></span>|<span data-ttu-id="c1f70-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c1f70-128">**Type**</span></span>|<span data-ttu-id="c1f70-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c1f70-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c1f70-130">Подключение</span><span class="sxs-lookup"><span data-stu-id="c1f70-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c1f70-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="c1f70-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c1f70-132">Представляет подключение между двумя фигурами в документе, такие как строку и поле в организационной диаграммы.</span><span class="sxs-lookup"><span data-stu-id="c1f70-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c1f70-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c1f70-133">Attributes</span></span>

<span data-ttu-id="c1f70-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="c1f70-134">None.</span></span>
  

