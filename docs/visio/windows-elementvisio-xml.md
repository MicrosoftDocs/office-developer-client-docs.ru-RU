---
title: Элемент Windows (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Содержит элементы Window для документа.
ms.openlocfilehash: fcffcd5257b14c0ae0203a41f369536e583c1798
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538447"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="fa29d-103">Элемент Windows (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fa29d-103">Windows element (Visio XML)</span></span>

<span data-ttu-id="fa29d-104">Содержит элементы **Window** для документа.</span><span class="sxs-lookup"><span data-stu-id="fa29d-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="fa29d-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fa29d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fa29d-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="fa29d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fa29d-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="fa29d-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fa29d-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fa29d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fa29d-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fa29d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fa29d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fa29d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fa29d-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="fa29d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fa29d-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="fa29d-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fa29d-113">Определение</span><span class="sxs-lookup"><span data-stu-id="fa29d-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fa29d-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fa29d-114">Elements and attributes</span></span>

<span data-ttu-id="fa29d-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="fa29d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fa29d-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fa29d-116">Parent elements</span></span>

<span data-ttu-id="fa29d-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="fa29d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fa29d-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fa29d-118">Child elements</span></span>

|<span data-ttu-id="fa29d-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fa29d-119">**Element**</span></span>|<span data-ttu-id="fa29d-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fa29d-120">**Type**</span></span>|<span data-ttu-id="fa29d-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fa29d-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fa29d-122">Window</span><span class="sxs-lookup"><span data-stu-id="fa29d-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fa29d-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="fa29d-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fa29d-124">Представляет открытое окно в экземпляре Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="fa29d-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fa29d-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fa29d-125">Attributes</span></span>

|<span data-ttu-id="fa29d-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fa29d-126">**Attribute**</span></span>|<span data-ttu-id="fa29d-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fa29d-127">**Type**</span></span>|<span data-ttu-id="fa29d-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="fa29d-128">**Required**</span></span>|<span data-ttu-id="fa29d-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fa29d-129">**Description**</span></span>|<span data-ttu-id="fa29d-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fa29d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fa29d-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="fa29d-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="fa29d-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fa29d-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fa29d-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="fa29d-133">optional</span></span>  <br/> |<span data-ttu-id="fa29d-134">Представляет измерение высоты области отображения</span><span class="sxs-lookup"><span data-stu-id="fa29d-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="fa29d-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fa29d-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="fa29d-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="fa29d-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="fa29d-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="fa29d-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="fa29d-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="fa29d-138">optional</span></span>  <br/> |<span data-ttu-id="fa29d-139">Представляет размер ширины области отображения</span><span class="sxs-lookup"><span data-stu-id="fa29d-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="fa29d-140">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="fa29d-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

