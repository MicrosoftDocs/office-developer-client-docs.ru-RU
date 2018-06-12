---
title: Элемент PageContents ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Задает сведения о фигурах в основной или рисования на странице рисунка.
ms.openlocfilehash: 0ca705081ad42d799a0155b26eb42ff0b64cd7d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814328"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="4c557-103">Элемент PageContents ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="4c557-103">PageContents element ('Visio XML')</span></span>

<span data-ttu-id="4c557-104">Задает сведения о фигурах в основной или рисования на странице рисунка.</span><span class="sxs-lookup"><span data-stu-id="4c557-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4c557-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4c557-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4c557-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4c557-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4c557-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="4c557-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4c557-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4c557-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4c557-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4c557-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4c557-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4c557-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4c557-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4c557-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4c557-112">страница # .xml</span><span class="sxs-lookup"><span data-stu-id="4c557-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4c557-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4c557-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4c557-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4c557-114">Elements and attributes</span></span>

<span data-ttu-id="4c557-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="4c557-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4c557-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4c557-116">Parent elements</span></span>

<span data-ttu-id="4c557-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="4c557-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4c557-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4c557-118">Child elements</span></span>

|<span data-ttu-id="4c557-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4c557-119">**Element**</span></span>|<span data-ttu-id="4c557-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4c557-120">**Type**</span></span>|<span data-ttu-id="4c557-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4c557-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4c557-122">Осуществляет подключение</span><span class="sxs-lookup"><span data-stu-id="4c557-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4c557-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="4c557-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4c557-124">Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="4c557-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="4c557-125">Фигур</span><span class="sxs-lookup"><span data-stu-id="4c557-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4c557-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="4c557-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4c557-127">Задает коллекцию фигур.</span><span class="sxs-lookup"><span data-stu-id="4c557-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4c557-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4c557-128">Attributes</span></span>

<span data-ttu-id="4c557-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="4c557-129">None.</span></span>
  

