---
title: Элемент Connects (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Содержит элемент Connect для каждого подключения между двумя фигурами в документе.
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538713"
---
# <a name="connects-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="c14d5-103">Элемент Connects (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c14d5-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c14d5-104">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="c14d5-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c14d5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c14d5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c14d5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c14d5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c14d5-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="c14d5-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c14d5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c14d5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c14d5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c14d5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c14d5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c14d5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c14d5-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c14d5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c14d5-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="c14d5-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c14d5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c14d5-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c14d5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c14d5-114">Elements and attributes</span></span>

<span data-ttu-id="c14d5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c14d5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c14d5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c14d5-116">Parent elements</span></span>

|<span data-ttu-id="c14d5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c14d5-117">**Element**</span></span>|<span data-ttu-id="c14d5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c14d5-118">**Type**</span></span>|<span data-ttu-id="c14d5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c14d5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c14d5-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="c14d5-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c14d5-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c14d5-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c14d5-122">Указывает сведения о фигурах в эталме или на странице рисования рисунка.</span><span class="sxs-lookup"><span data-stu-id="c14d5-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="c14d5-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="c14d5-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c14d5-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c14d5-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c14d5-125">Указывает сведения о фигурах в эталме или на странице рисования рисунка.</span><span class="sxs-lookup"><span data-stu-id="c14d5-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c14d5-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c14d5-126">Child elements</span></span>

|<span data-ttu-id="c14d5-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c14d5-127">**Element**</span></span>|<span data-ttu-id="c14d5-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c14d5-128">**Type**</span></span>|<span data-ttu-id="c14d5-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c14d5-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c14d5-130">Connect</span><span class="sxs-lookup"><span data-stu-id="c14d5-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c14d5-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="c14d5-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c14d5-132">Представляет соединение между двумя фигурами в рисунке, например строкой и полем в диаграмме организации.</span><span class="sxs-lookup"><span data-stu-id="c14d5-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c14d5-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c14d5-133">Attributes</span></span>

<span data-ttu-id="c14d5-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="c14d5-134">None.</span></span>
  

