---
title: Элемент образцов ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: eb90df82-58b6-5d0b-6b7d-826c5c27c755
description: Содержит основной элементов для документа.
ms.openlocfilehash: d40071c64dc454eeb92f8518f89ef4de8b3b0cb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814200"
---
# <a name="masters-element-visio-xml"></a><span data-ttu-id="19372-103">Элемент образцов ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="19372-103">Masters element ('Visio XML')</span></span>

<span data-ttu-id="19372-104">Содержит основной элементов для документа.</span><span class="sxs-lookup"><span data-stu-id="19372-104">Contains the Master elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="19372-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="19372-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="19372-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="19372-106">**Element type**</span></span> <br/> |[<span data-ttu-id="19372-107">Masters_Type</span><span class="sxs-lookup"><span data-stu-id="19372-107">Masters_Type</span></span>](masters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="19372-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="19372-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="19372-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="19372-109">**Schema file**</span></span> <br/> |<span data-ttu-id="19372-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="19372-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="19372-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="19372-111">**Document parts**</span></span> <br/> |<span data-ttu-id="19372-112">Masters.XML</span><span class="sxs-lookup"><span data-stu-id="19372-112">masters.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="19372-113">Определение</span><span class="sxs-lookup"><span data-stu-id="19372-113">Definition</span></span>

```XML
< xs:element name="Masters" type="Masters_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="19372-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="19372-114">Elements and attributes</span></span>

<span data-ttu-id="19372-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="19372-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="19372-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="19372-116">Parent elements</span></span>

<span data-ttu-id="19372-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="19372-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="19372-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="19372-118">Child elements</span></span>

|<span data-ttu-id="19372-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="19372-119">**Element**</span></span>|<span data-ttu-id="19372-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="19372-120">**Type**</span></span>|<span data-ttu-id="19372-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="19372-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="19372-122">Образец</span><span class="sxs-lookup"><span data-stu-id="19372-122">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19372-123">Master_Type</span><span class="sxs-lookup"><span data-stu-id="19372-123">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="19372-124">Содержит элементы, определяющие шаблона для документа.</span><span class="sxs-lookup"><span data-stu-id="19372-124">Contains elements that define a master for the document.</span></span>  <br/> |
|[<span data-ttu-id="19372-125">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="19372-125">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="19372-126">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="19372-126">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="19372-127">Задает ярлыка образца, определенным в документе.</span><span class="sxs-lookup"><span data-stu-id="19372-127">Specifies a master shortcut defined in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="19372-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="19372-128">Attributes</span></span>

<span data-ttu-id="19372-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="19372-129">None.</span></span>
  

