---
title: Элемент Пажеконтентс (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Задает сведения о фигурах на главной странице или странице документа в документе.
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537999"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="3ea06-103">Элемент Пажеконтентс (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="3ea06-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="3ea06-104">Задает сведения о фигурах на главной странице или странице документа в документе.</span><span class="sxs-lookup"><span data-stu-id="3ea06-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3ea06-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3ea06-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ea06-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3ea06-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3ea06-107">Пажеконтентс_типе</span><span class="sxs-lookup"><span data-stu-id="3ea06-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3ea06-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3ea06-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3ea06-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3ea06-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3ea06-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3ea06-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3ea06-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3ea06-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3ea06-112">страница #. XML</span><span class="sxs-lookup"><span data-stu-id="3ea06-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ea06-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3ea06-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ea06-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3ea06-114">Elements and attributes</span></span>

<span data-ttu-id="3ea06-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3ea06-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3ea06-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3ea06-116">Parent elements</span></span>

<span data-ttu-id="3ea06-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="3ea06-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3ea06-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3ea06-118">Child elements</span></span>

|<span data-ttu-id="3ea06-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3ea06-119">**Element**</span></span>|<span data-ttu-id="3ea06-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3ea06-120">**Type**</span></span>|<span data-ttu-id="3ea06-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3ea06-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ea06-122">Connects</span><span class="sxs-lookup"><span data-stu-id="3ea06-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ea06-123">Коннектс_типе</span><span class="sxs-lookup"><span data-stu-id="3ea06-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ea06-124">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="3ea06-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="3ea06-125">Фигуры</span><span class="sxs-lookup"><span data-stu-id="3ea06-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ea06-126">Шапес_типе</span><span class="sxs-lookup"><span data-stu-id="3ea06-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3ea06-127">Задает коллекцию фигур.</span><span class="sxs-lookup"><span data-stu-id="3ea06-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3ea06-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3ea06-128">Attributes</span></span>

<span data-ttu-id="3ea06-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="3ea06-129">None.</span></span>
  

