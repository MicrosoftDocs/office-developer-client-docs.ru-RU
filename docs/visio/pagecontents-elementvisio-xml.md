---
title: Элемент PageContents (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Указывает сведения о фигурах в эталме или на странице рисования рисунка.
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537999"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="d9eb5-103">Элемент PageContents (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="d9eb5-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="d9eb5-104">Указывает сведения о фигурах в эталме или на странице рисования рисунка.</span><span class="sxs-lookup"><span data-stu-id="d9eb5-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d9eb5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d9eb5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9eb5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="d9eb5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d9eb5-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="d9eb5-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d9eb5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d9eb5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d9eb5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d9eb5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d9eb5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="d9eb5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d9eb5-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="d9eb5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d9eb5-112">page#.xml</span><span class="sxs-lookup"><span data-stu-id="d9eb5-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d9eb5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="d9eb5-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d9eb5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d9eb5-114">Elements and attributes</span></span>

<span data-ttu-id="d9eb5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d9eb5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d9eb5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d9eb5-116">Parent elements</span></span>

<span data-ttu-id="d9eb5-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="d9eb5-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d9eb5-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d9eb5-118">Child elements</span></span>

|<span data-ttu-id="d9eb5-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d9eb5-119">**Element**</span></span>|<span data-ttu-id="d9eb5-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d9eb5-120">**Type**</span></span>|<span data-ttu-id="d9eb5-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d9eb5-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d9eb5-122">Connects</span><span class="sxs-lookup"><span data-stu-id="d9eb5-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d9eb5-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="d9eb5-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d9eb5-124">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="d9eb5-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="d9eb5-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="d9eb5-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d9eb5-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="d9eb5-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d9eb5-127">Указывает коллекцию фигур.</span><span class="sxs-lookup"><span data-stu-id="d9eb5-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="d9eb5-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d9eb5-128">Attributes</span></span>

<span data-ttu-id="d9eb5-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="d9eb5-129">None.</span></span>
  

