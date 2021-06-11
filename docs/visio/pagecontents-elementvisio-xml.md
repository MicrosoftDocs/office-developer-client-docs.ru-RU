---
title: Элемент PageContents (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 818793d6-608e-5f23-eca2-55ce6667050b
description: Указывает сведения о фигурах в мастере или на странице рисования рисунка.
ms.openlocfilehash: 23ff6c74007adc5764007e34c1b2ac92c522b121
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537999"
---
# <a name="pagecontents-element-visio-xml"></a><span data-ttu-id="95cfe-103">Элемент PageContents (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="95cfe-103">PageContents element (Visio XML)</span></span>

<span data-ttu-id="95cfe-104">Указывает сведения о фигурах в мастере или на странице рисования рисунка.</span><span class="sxs-lookup"><span data-stu-id="95cfe-104">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95cfe-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="95cfe-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95cfe-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="95cfe-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95cfe-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="95cfe-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95cfe-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="95cfe-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95cfe-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="95cfe-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95cfe-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="95cfe-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95cfe-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="95cfe-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95cfe-112">page#.xml</span><span class="sxs-lookup"><span data-stu-id="95cfe-112">page#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95cfe-113">Определение</span><span class="sxs-lookup"><span data-stu-id="95cfe-113">Definition</span></span>

```XML
< xs:element name="PageContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95cfe-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="95cfe-114">Elements and attributes</span></span>

<span data-ttu-id="95cfe-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="95cfe-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95cfe-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="95cfe-116">Parent elements</span></span>

<span data-ttu-id="95cfe-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="95cfe-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="95cfe-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="95cfe-118">Child elements</span></span>

|<span data-ttu-id="95cfe-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="95cfe-119">**Element**</span></span>|<span data-ttu-id="95cfe-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="95cfe-120">**Type**</span></span>|<span data-ttu-id="95cfe-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="95cfe-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95cfe-122">Connects</span><span class="sxs-lookup"><span data-stu-id="95cfe-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95cfe-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="95cfe-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95cfe-124">Содержит элемент **Подключение** для каждого подключения между двумя фигурами в рисунке.</span><span class="sxs-lookup"><span data-stu-id="95cfe-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="95cfe-125">Фигуры</span><span class="sxs-lookup"><span data-stu-id="95cfe-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95cfe-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="95cfe-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95cfe-127">Указывает коллекцию фигур.</span><span class="sxs-lookup"><span data-stu-id="95cfe-127">Specifies a collection of shapes.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95cfe-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="95cfe-128">Attributes</span></span>

<span data-ttu-id="95cfe-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="95cfe-129">None.</span></span>
  

