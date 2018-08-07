---
title: Элемент MasterContents ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Задает сведения о фигурах в главный в документе.
ms.openlocfilehash: d1ba67a414ac80be9da2beebb93acc89faf71172
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814203"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="02e01-103">Элемент MasterContents ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="02e01-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="02e01-104">Задает сведения о фигурах в главный в документе.</span><span class="sxs-lookup"><span data-stu-id="02e01-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="02e01-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="02e01-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02e01-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="02e01-106">**Element type**</span></span> <br/> |[<span data-ttu-id="02e01-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="02e01-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="02e01-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="02e01-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="02e01-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="02e01-109">**Schema file**</span></span> <br/> |<span data-ttu-id="02e01-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="02e01-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="02e01-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="02e01-111">**Document parts**</span></span> <br/> |<span data-ttu-id="02e01-112">главные # .xml</span><span class="sxs-lookup"><span data-stu-id="02e01-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02e01-113">Определение</span><span class="sxs-lookup"><span data-stu-id="02e01-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02e01-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="02e01-114">Elements and attributes</span></span>

<span data-ttu-id="02e01-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="02e01-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="02e01-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="02e01-116">Parent elements</span></span>

<span data-ttu-id="02e01-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="02e01-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="02e01-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="02e01-118">Child elements</span></span>

|<span data-ttu-id="02e01-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="02e01-119">**Element**</span></span>|<span data-ttu-id="02e01-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="02e01-120">**Type**</span></span>|<span data-ttu-id="02e01-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02e01-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02e01-122">Осуществляет подключение</span><span class="sxs-lookup"><span data-stu-id="02e01-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02e01-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="02e01-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02e01-124">Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="02e01-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="02e01-125">Фигур</span><span class="sxs-lookup"><span data-stu-id="02e01-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02e01-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="02e01-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02e01-127">Содержит коллекцию элементов **фигуры** .</span><span class="sxs-lookup"><span data-stu-id="02e01-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="02e01-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="02e01-128">Attributes</span></span>

<span data-ttu-id="02e01-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="02e01-129">None.</span></span>
  

