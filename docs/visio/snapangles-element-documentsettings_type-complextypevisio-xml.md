---
title: Элемент SnapAngles (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 803ddfc1-b7d3-736f-2d85-7b8780ef9278
description: Содержит коллекцию элементов SnapAngle.
ms.openlocfilehash: d0b2c2a0643b4f3bccd5b450ef0d9c89ce9ab7c2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540394"
---
# <a name="snapangles-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="475f7-103">Элемент SnapAngles (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="475f7-103">SnapAngles element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="475f7-104">Содержит коллекцию элементов **SnapAngle.**</span><span class="sxs-lookup"><span data-stu-id="475f7-104">Contains a collection of **SnapAngle** elements.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="475f7-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="475f7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="475f7-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="475f7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="475f7-107">SnapAngles_Type</span><span class="sxs-lookup"><span data-stu-id="475f7-107">SnapAngles_Type</span></span>](snapangles_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="475f7-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="475f7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="475f7-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="475f7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="475f7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="475f7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="475f7-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="475f7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="475f7-112">document.xml</span><span class="sxs-lookup"><span data-stu-id="475f7-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="475f7-113">Определение</span><span class="sxs-lookup"><span data-stu-id="475f7-113">Definition</span></span>

```XML
< xs:element name="SnapAngles" type="SnapAngles_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="475f7-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="475f7-114">Elements and attributes</span></span>

<span data-ttu-id="475f7-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="475f7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="475f7-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="475f7-116">Parent elements</span></span>

|<span data-ttu-id="475f7-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="475f7-117">**Element**</span></span>|<span data-ttu-id="475f7-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="475f7-118">**Type**</span></span>|<span data-ttu-id="475f7-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="475f7-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="475f7-120">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="475f7-120">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="475f7-121">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="475f7-121">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="475f7-122">Содержит элементы, определяющие параметры документа.</span><span class="sxs-lookup"><span data-stu-id="475f7-122">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="475f7-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="475f7-123">Child elements</span></span>

|<span data-ttu-id="475f7-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="475f7-124">**Element**</span></span>|<span data-ttu-id="475f7-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="475f7-125">**Type**</span></span>|<span data-ttu-id="475f7-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="475f7-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="475f7-127">SnapAngle</span><span class="sxs-lookup"><span data-stu-id="475f7-127">SnapAngle</span></span>](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="475f7-128">SnapAngle_Type</span><span class="sxs-lookup"><span data-stu-id="475f7-128">SnapAngle_Type</span></span>](snapangle_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="475f7-129">Содержит число с плавающей за точкой, указывающей угол прикрепления в градусах.</span><span class="sxs-lookup"><span data-stu-id="475f7-129">Contains a floating point number that specifies a snap angle in degrees.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="475f7-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="475f7-130">Attributes</span></span>

<span data-ttu-id="475f7-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="475f7-131">None.</span></span>
  

