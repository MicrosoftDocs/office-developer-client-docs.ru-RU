---
title: Элемент SnapAngle (SnapAngles_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d4f93fc5-80fb-3195-d25b-9a407de7848e
description: Содержит номер плавающей точки, который указывает угол оснастки в градусах.
ms.openlocfilehash: be53b3fdbe7aa04b6bcdf703f1859e866f2af2c2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540457"
---
# <a name="snapangle-element-snapangles_type-complextype-visio-xml"></a><span data-ttu-id="f4e5c-103">Элемент SnapAngle (SnapAngles_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f4e5c-103">SnapAngle element (SnapAngles_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="f4e5c-104">Содержит номер плавающей точки, который указывает угол оснастки в градусах.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-104">Contains a floating point number that specifies a snap angle in degrees.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f4e5c-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f4e5c-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4e5c-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f4e5c-107">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="f4e5c-107">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f4e5c-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f4e5c-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f4e5c-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f4e5c-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f4e5c-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f4e5c-112">document.xml, windows.xml</span><span class="sxs-lookup"><span data-stu-id="f4e5c-112">document.xml, windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f4e5c-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f4e5c-113">Definition</span></span>

```XML
< xs:element name="SnapAngle" type="SnapAngle_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f4e5c-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f4e5c-114">Elements and attributes</span></span>

<span data-ttu-id="f4e5c-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f4e5c-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f4e5c-116">Parent elements</span></span>

|<span data-ttu-id="f4e5c-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-117">**Element**</span></span>|<span data-ttu-id="f4e5c-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-118">**Type**</span></span>|<span data-ttu-id="f4e5c-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f4e5c-120">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="f4e5c-120">SnapAngles</span></span>](snapangles-element-window_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f4e5c-121">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="f4e5c-121">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f4e5c-122">Содержит коллекцию **элементов SnapAngle.**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-122">Contains a collection of **SnapAngle** elements.</span></span>  <br/> |
|[<span data-ttu-id="f4e5c-123">SnapAngles</span><span class="sxs-lookup"><span data-stu-id="f4e5c-123">SnapAngles</span></span>](snapangles-element-documentsettings_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f4e5c-124">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="f4e5c-124">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f4e5c-125">Содержит коллекцию **элементов SnapAngle.**</span><span class="sxs-lookup"><span data-stu-id="f4e5c-125">Contains a collection of **SnapAngle** elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f4e5c-126">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f4e5c-126">Child elements</span></span>

<span data-ttu-id="f4e5c-127">Нет.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-127">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f4e5c-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f4e5c-128">Attributes</span></span>

<span data-ttu-id="f4e5c-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="f4e5c-129">None.</span></span>
  

