---
title: Элемент RefBy (Trigger_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Указывает ссылку на страницу в рисунке.
ms.openlocfilehash: 6d081ad1bf9e089a16820db33cec92694db7ac98
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538293"
---
# <a name="refby-element-trigger_type-complextype-visio-xml"></a><span data-ttu-id="c5475-103">Элемент RefBy (Trigger_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c5475-103">RefBy element (Trigger_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c5475-104">Указывает ссылку на страницу в рисунке.</span><span class="sxs-lookup"><span data-stu-id="c5475-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c5475-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c5475-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c5475-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c5475-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c5475-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="c5475-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c5475-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c5475-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c5475-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c5475-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c5475-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c5475-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c5475-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="c5475-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="c5475-112">Определение</span><span class="sxs-lookup"><span data-stu-id="c5475-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c5475-113">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5475-113">Elements and attributes</span></span>

<span data-ttu-id="c5475-114">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c5475-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c5475-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c5475-115">Parent elements</span></span>

|<span data-ttu-id="c5475-116">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c5475-116">**Element**</span></span>|<span data-ttu-id="c5475-117">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5475-117">**Type**</span></span>|<span data-ttu-id="c5475-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5475-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c5475-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="c5475-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="c5475-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="c5475-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c5475-121">Предоставляет инструкции корпорации Майкрософт Visio для пересчета связи между частями документов в Visio файле.</span><span class="sxs-lookup"><span data-stu-id="c5475-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="c5475-122">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c5475-122">Child elements</span></span>

<span data-ttu-id="c5475-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="c5475-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c5475-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5475-124">Attributes</span></span>

|<span data-ttu-id="c5475-125">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c5475-125">**Attribute**</span></span>|<span data-ttu-id="c5475-126">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c5475-126">**Type**</span></span>|<span data-ttu-id="c5475-127">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="c5475-127">**Required**</span></span>|<span data-ttu-id="c5475-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c5475-128">**Description**</span></span>|<span data-ttu-id="c5475-129">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c5475-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c5475-130">ID</span><span class="sxs-lookup"><span data-stu-id="c5475-130">ID</span></span>  <br/> |<span data-ttu-id="c5475-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c5475-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c5475-132">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c5475-132">required</span></span>  <br/> |<span data-ttu-id="c5475-133">Указывает атрибут ID страницы в рисунке.</span><span class="sxs-lookup"><span data-stu-id="c5475-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="c5475-134">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c5475-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c5475-135">T</span><span class="sxs-lookup"><span data-stu-id="c5475-135">T</span></span>  <br/> |<span data-ttu-id="c5475-136">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c5475-136">xsd:string</span></span>  <br/> |<span data-ttu-id="c5475-137">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c5475-137">required</span></span>  <br/> |<span data-ttu-id="c5475-138">Указывает тип ссылки.</span><span class="sxs-lookup"><span data-stu-id="c5475-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="c5475-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="c5475-139">Values of the xsd:string type.</span></span>  <br/> |
   

