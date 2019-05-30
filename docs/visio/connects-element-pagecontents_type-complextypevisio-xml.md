---
title: Элемент connects (Пажеконтентс_типе complexType) (XML для Visio)
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
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="4783a-103">Элемент connects (Пажеконтентс_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="4783a-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4783a-104">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="4783a-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4783a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4783a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4783a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4783a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4783a-107">Коннектс_типе</span><span class="sxs-lookup"><span data-stu-id="4783a-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4783a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4783a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4783a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4783a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4783a-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="4783a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4783a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4783a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4783a-112">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="4783a-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4783a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4783a-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4783a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4783a-114">Elements and attributes</span></span>

<span data-ttu-id="4783a-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4783a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4783a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4783a-116">Parent elements</span></span>

|<span data-ttu-id="4783a-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4783a-117">**Element**</span></span>|<span data-ttu-id="4783a-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4783a-118">**Type**</span></span>|<span data-ttu-id="4783a-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4783a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4783a-120">Мастерконтентс</span><span class="sxs-lookup"><span data-stu-id="4783a-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="4783a-121">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="4783a-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4783a-122">Задает сведения о фигурах на главной странице или странице документа в документе.</span><span class="sxs-lookup"><span data-stu-id="4783a-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="4783a-123">Пажеконтентс</span><span class="sxs-lookup"><span data-stu-id="4783a-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="4783a-124">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="4783a-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4783a-125">Задает сведения о фигурах на главной странице или странице документа в документе.</span><span class="sxs-lookup"><span data-stu-id="4783a-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4783a-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4783a-126">Child elements</span></span>

|<span data-ttu-id="4783a-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4783a-127">**Element**</span></span>|<span data-ttu-id="4783a-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4783a-128">**Type**</span></span>|<span data-ttu-id="4783a-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4783a-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4783a-130">Connect</span><span class="sxs-lookup"><span data-stu-id="4783a-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4783a-131">Коннект_типе</span><span class="sxs-lookup"><span data-stu-id="4783a-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4783a-132">Представляет соединение между двумя фигурами в документе, например линии и поле на организационной диаграмме.</span><span class="sxs-lookup"><span data-stu-id="4783a-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4783a-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4783a-133">Attributes</span></span>

<span data-ttu-id="4783a-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="4783a-134">None.</span></span>
  

