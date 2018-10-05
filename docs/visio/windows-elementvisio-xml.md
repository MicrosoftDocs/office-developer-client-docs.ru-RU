---
title: Элемент Windows ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Содержит элементы окна документа.
ms.openlocfilehash: df4d4bc48db157bd05fd39177975c9dbeaa5de52
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386805"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="83b11-103">Элемент Windows ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="83b11-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="83b11-104">Содержит элементы **окна** документа.</span><span class="sxs-lookup"><span data-stu-id="83b11-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="83b11-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="83b11-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="83b11-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="83b11-106">**Element type**</span></span> <br/> |[<span data-ttu-id="83b11-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="83b11-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="83b11-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="83b11-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="83b11-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="83b11-109">**Schema file**</span></span> <br/> |<span data-ttu-id="83b11-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="83b11-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="83b11-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="83b11-111">**Document parts**</span></span> <br/> |<span data-ttu-id="83b11-112">Windows.XML</span><span class="sxs-lookup"><span data-stu-id="83b11-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="83b11-113">Определение</span><span class="sxs-lookup"><span data-stu-id="83b11-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="83b11-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="83b11-114">Elements and attributes</span></span>

<span data-ttu-id="83b11-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="83b11-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="83b11-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="83b11-116">Parent elements</span></span>

<span data-ttu-id="83b11-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="83b11-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="83b11-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="83b11-118">Child elements</span></span>

|<span data-ttu-id="83b11-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="83b11-119">**Element**</span></span>|<span data-ttu-id="83b11-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="83b11-120">**Type**</span></span>|<span data-ttu-id="83b11-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="83b11-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="83b11-122">Window</span><span class="sxs-lookup"><span data-stu-id="83b11-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="83b11-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="83b11-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="83b11-124">Представляет окно в экземпляре Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="83b11-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="83b11-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="83b11-125">Attributes</span></span>

|<span data-ttu-id="83b11-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="83b11-126">**Attribute**</span></span>|<span data-ttu-id="83b11-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="83b11-127">**Type**</span></span>|<span data-ttu-id="83b11-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="83b11-128">**Required**</span></span>|<span data-ttu-id="83b11-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="83b11-129">**Description**</span></span>|<span data-ttu-id="83b11-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="83b11-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="83b11-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="83b11-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="83b11-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="83b11-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="83b11-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="83b11-133">optional</span></span>  <br/> |<span data-ttu-id="83b11-134">Представляет значение высоты области отображения</span><span class="sxs-lookup"><span data-stu-id="83b11-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="83b11-135">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="83b11-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="83b11-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="83b11-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="83b11-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="83b11-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="83b11-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="83b11-138">optional</span></span>  <br/> |<span data-ttu-id="83b11-139">Представляет ширины области отображения</span><span class="sxs-lookup"><span data-stu-id="83b11-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="83b11-140">Значения для типа xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="83b11-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

