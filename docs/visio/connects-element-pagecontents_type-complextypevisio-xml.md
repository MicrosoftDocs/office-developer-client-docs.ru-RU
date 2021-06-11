---
title: Подключает элемент (PageContents_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Содержит элемент Подключение для каждого подключения между двумя фигурами в рисунке.
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538713"
---
# <a name="connects-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="72e76-103">Подключает элемент (PageContents_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="72e76-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="72e76-104">Содержит элемент **Подключение** для каждого подключения между двумя фигурами в рисунке.</span><span class="sxs-lookup"><span data-stu-id="72e76-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="72e76-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="72e76-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72e76-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="72e76-106">**Element type**</span></span> <br/> |[<span data-ttu-id="72e76-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="72e76-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="72e76-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="72e76-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="72e76-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="72e76-109">**Schema file**</span></span> <br/> |<span data-ttu-id="72e76-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="72e76-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="72e76-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="72e76-111">**Document parts**</span></span> <br/> |<span data-ttu-id="72e76-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="72e76-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72e76-113">Определение</span><span class="sxs-lookup"><span data-stu-id="72e76-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="72e76-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="72e76-114">Elements and attributes</span></span>

<span data-ttu-id="72e76-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="72e76-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="72e76-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="72e76-116">Parent elements</span></span>

|<span data-ttu-id="72e76-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="72e76-117">**Element**</span></span>|<span data-ttu-id="72e76-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="72e76-118">**Type**</span></span>|<span data-ttu-id="72e76-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72e76-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="72e76-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="72e76-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="72e76-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="72e76-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="72e76-122">Указывает сведения о фигурах в мастере или на странице рисования рисунка.</span><span class="sxs-lookup"><span data-stu-id="72e76-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="72e76-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="72e76-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="72e76-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="72e76-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="72e76-125">Указывает сведения о фигурах в мастере или на странице рисования рисунка.</span><span class="sxs-lookup"><span data-stu-id="72e76-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="72e76-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="72e76-126">Child elements</span></span>

|<span data-ttu-id="72e76-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="72e76-127">**Element**</span></span>|<span data-ttu-id="72e76-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="72e76-128">**Type**</span></span>|<span data-ttu-id="72e76-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72e76-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="72e76-130">Connect</span><span class="sxs-lookup"><span data-stu-id="72e76-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="72e76-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="72e76-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="72e76-132">Представляет связь между двумя фигурами в рисунке, например строкой и полем в диаграмме организации.</span><span class="sxs-lookup"><span data-stu-id="72e76-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="72e76-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="72e76-133">Attributes</span></span>

<span data-ttu-id="72e76-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="72e76-134">None.</span></span>
  

