---
title: Элемент Masters (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Содержит основные элементы документа.
ms.openlocfilehash: b2506466a5208223e3e7b9668ad6442030ec95c9
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538055"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="e9140-103">Элемент Masters (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e9140-103">Masters element (Visio XML)</span></span>

<span data-ttu-id="e9140-104">Содержит основные элементы документа.</span><span class="sxs-lookup"><span data-stu-id="e9140-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e9140-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e9140-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9140-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e9140-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e9140-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="e9140-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e9140-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e9140-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e9140-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e9140-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e9140-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e9140-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e9140-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="e9140-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e9140-112">masters.xml</span><span class="sxs-lookup"><span data-stu-id="e9140-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e9140-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e9140-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e9140-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e9140-114">Elements and attributes</span></span>

<span data-ttu-id="e9140-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e9140-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e9140-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e9140-116">Parent elements</span></span>

<span data-ttu-id="e9140-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="e9140-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e9140-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e9140-118">Child elements</span></span>

|<span data-ttu-id="e9140-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e9140-119">**Element**</span></span>|<span data-ttu-id="e9140-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e9140-120">**Type**</span></span>|<span data-ttu-id="e9140-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9140-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e9140-122">Master</span><span class="sxs-lookup"><span data-stu-id="e9140-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9140-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="e9140-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e9140-124">Содержит элементы, определяющие мастер документа.</span><span class="sxs-lookup"><span data-stu-id="e9140-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="e9140-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="e9140-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e9140-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="e9140-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e9140-127">Указывает мастер-ярлык, определенный в документе.</span><span class="sxs-lookup"><span data-stu-id="e9140-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="e9140-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e9140-128">Attributes</span></span>

<span data-ttu-id="e9140-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="e9140-129">None.</span></span>
  

