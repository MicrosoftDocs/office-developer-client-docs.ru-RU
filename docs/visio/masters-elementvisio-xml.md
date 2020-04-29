---
title: Элемент хозяев (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Содержит элементы Master для документа.
ms.openlocfilehash: b2506466a5208223e3e7b9668ad6442030ec95c9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538055"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="3b045-103">Элемент хозяев (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="3b045-103">Masters element (Visio XML)</span></span>

<span data-ttu-id="3b045-104">Содержит элементы Master для документа.</span><span class="sxs-lookup"><span data-stu-id="3b045-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b045-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="3b045-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b045-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="3b045-106">**Element type**</span></span> <br/> |[<span data-ttu-id="3b045-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="3b045-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="3b045-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="3b045-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="3b045-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="3b045-109">**Schema file**</span></span> <br/> |<span data-ttu-id="3b045-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="3b045-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="3b045-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="3b045-111">**Document parts**</span></span> <br/> |<span data-ttu-id="3b045-112">Главные. XML</span><span class="sxs-lookup"><span data-stu-id="3b045-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3b045-113">Определение</span><span class="sxs-lookup"><span data-stu-id="3b045-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3b045-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="3b045-114">Elements and attributes</span></span>

<span data-ttu-id="3b045-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="3b045-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="3b045-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="3b045-116">Parent elements</span></span>

<span data-ttu-id="3b045-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="3b045-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b045-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3b045-118">Child elements</span></span>

|<span data-ttu-id="3b045-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="3b045-119">**Element**</span></span>|<span data-ttu-id="3b045-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="3b045-120">**Type**</span></span>|<span data-ttu-id="3b045-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3b045-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3b045-122">Master</span><span class="sxs-lookup"><span data-stu-id="3b045-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3b045-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="3b045-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3b045-124">Содержит элементы, определяющие шаблон для документа.</span><span class="sxs-lookup"><span data-stu-id="3b045-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="3b045-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="3b045-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3b045-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="3b045-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="3b045-127">Задает ярлык образца, определенный в документе.</span><span class="sxs-lookup"><span data-stu-id="3b045-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="3b045-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3b045-128">Attributes</span></span>

<span data-ttu-id="3b045-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="3b045-129">None.</span></span>
  

