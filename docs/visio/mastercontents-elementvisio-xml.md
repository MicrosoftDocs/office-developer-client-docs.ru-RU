---
title: Элемент Мастерконтентс (' XML ' Visio ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Задает сведения о фигурах в образце в документе.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341358"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="3c966-103">Элемент Мастерконтентс (' XML ' Visio ')</span><span class="sxs-lookup"><span data-stu-id="3c966-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="3c966-104">Задает сведения о фигурах в образце в документе.</span><span class="sxs-lookup"><span data-stu-id="3c966-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="3c966-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3c966-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c966-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3c966-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3c966-107">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="3c966-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3c966-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3c966-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3c966-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3c966-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3c966-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3c966-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3c966-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3c966-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3c966-112">Master #. XML</span><span class="sxs-lookup"><span data-stu-id="3c966-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3c966-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3c966-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3c966-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3c966-114">Elements and attributes</span></span>

<span data-ttu-id="3c966-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3c966-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3c966-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3c966-116">Parent elements</span></span>

<span data-ttu-id="3c966-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="3c966-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c966-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3c966-118">Child elements</span></span>

|<span data-ttu-id="3c966-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3c966-119">**Element**</span></span>|<span data-ttu-id="3c966-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3c966-120">**Type**</span></span>|<span data-ttu-id="3c966-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3c966-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3c966-122">Connects</span><span class="sxs-lookup"><span data-stu-id="3c966-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c966-123">Коннектс_типе</span><span class="sxs-lookup"><span data-stu-id="3c966-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c966-124">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="3c966-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="3c966-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="3c966-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3c966-126">Шапес_типе</span><span class="sxs-lookup"><span data-stu-id="3c966-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3c966-127">Содержит коллекцию элементов **Shape** .</span><span class="sxs-lookup"><span data-stu-id="3c966-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3c966-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3c966-128">Attributes</span></span>

<span data-ttu-id="3c966-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="3c966-129">None.</span></span>
  

