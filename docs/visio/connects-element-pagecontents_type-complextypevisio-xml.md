---
title: Элемент Connects (Пажеконтентс_типе complexType) (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Содержит элемент Connect для каждого подключения между двумя фигурами в документе.
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318965"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="164b9-103">Элемент Connects (Пажеконтентс_типе complexType) (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="164b9-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="164b9-104">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="164b9-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="164b9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="164b9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="164b9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="164b9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="164b9-107">Коннектс_типе</span><span class="sxs-lookup"><span data-stu-id="164b9-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="164b9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="164b9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="164b9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="164b9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="164b9-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="164b9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="164b9-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="164b9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="164b9-112">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="164b9-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="164b9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="164b9-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="164b9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="164b9-114">Elements and attributes</span></span>

<span data-ttu-id="164b9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="164b9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="164b9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="164b9-116">Parent elements</span></span>

|<span data-ttu-id="164b9-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="164b9-117">**Element**</span></span>|<span data-ttu-id="164b9-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="164b9-118">**Type**</span></span>|<span data-ttu-id="164b9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="164b9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="164b9-120">Мастерконтентс</span><span class="sxs-lookup"><span data-stu-id="164b9-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="164b9-121">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="164b9-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="164b9-122">Задает сведения о фигурах на главной странице или странице документа в документе.</span><span class="sxs-lookup"><span data-stu-id="164b9-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="164b9-123">Пажеконтентс</span><span class="sxs-lookup"><span data-stu-id="164b9-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="164b9-124">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="164b9-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="164b9-125">Задает сведения о фигурах на главной странице или странице документа в документе.</span><span class="sxs-lookup"><span data-stu-id="164b9-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="164b9-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="164b9-126">Child elements</span></span>

|<span data-ttu-id="164b9-127">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="164b9-127">**Element**</span></span>|<span data-ttu-id="164b9-128">**Тип**</span><span class="sxs-lookup"><span data-stu-id="164b9-128">**Type**</span></span>|<span data-ttu-id="164b9-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="164b9-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="164b9-130">Connect</span><span class="sxs-lookup"><span data-stu-id="164b9-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="164b9-131">Коннект_типе</span><span class="sxs-lookup"><span data-stu-id="164b9-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="164b9-132">Представляет соединение между двумя фигурами в документе, например линии и поле на организационной диаграмме.</span><span class="sxs-lookup"><span data-stu-id="164b9-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="164b9-133">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="164b9-133">Attributes</span></span>

<span data-ttu-id="164b9-134">Нет.</span><span class="sxs-lookup"><span data-stu-id="164b9-134">None.</span></span>
  

