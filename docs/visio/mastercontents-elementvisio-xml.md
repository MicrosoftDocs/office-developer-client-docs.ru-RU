---
title: Элемент Мастерконтентс (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Задает сведения о фигурах в образце в документе.
ms.openlocfilehash: 26bc86aedeb96544f61f53052ab723b13b29500d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538041"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="67f2f-103">Элемент Мастерконтентс (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="67f2f-103">MasterContents element (Visio XML)</span></span>

<span data-ttu-id="67f2f-104">Задает сведения о фигурах в образце в документе.</span><span class="sxs-lookup"><span data-stu-id="67f2f-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="67f2f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="67f2f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67f2f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="67f2f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="67f2f-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="67f2f-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="67f2f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="67f2f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="67f2f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="67f2f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="67f2f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="67f2f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="67f2f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="67f2f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="67f2f-112">Master #. XML</span><span class="sxs-lookup"><span data-stu-id="67f2f-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="67f2f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="67f2f-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="67f2f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="67f2f-114">Elements and attributes</span></span>

<span data-ttu-id="67f2f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="67f2f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="67f2f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="67f2f-116">Parent elements</span></span>

<span data-ttu-id="67f2f-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="67f2f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="67f2f-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="67f2f-118">Child elements</span></span>

|<span data-ttu-id="67f2f-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="67f2f-119">**Element**</span></span>|<span data-ttu-id="67f2f-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="67f2f-120">**Type**</span></span>|<span data-ttu-id="67f2f-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="67f2f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="67f2f-122">Connects</span><span class="sxs-lookup"><span data-stu-id="67f2f-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67f2f-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="67f2f-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67f2f-124">Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.</span><span class="sxs-lookup"><span data-stu-id="67f2f-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="67f2f-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="67f2f-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="67f2f-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="67f2f-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="67f2f-127">Содержит коллекцию элементов **Shape** .</span><span class="sxs-lookup"><span data-stu-id="67f2f-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="67f2f-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="67f2f-128">Attributes</span></span>

<span data-ttu-id="67f2f-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="67f2f-129">None.</span></span>
  

