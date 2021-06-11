---
title: Элемент Data2 (ShapeSheet_Type Type) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e823797e-dde9-6ee7-b5e4-9e57cef90b08
description: Содержит произвольное значение строки, которое используется для получения дополнительных сведений о фигуре.
ms.openlocfilehash: f76300d67cd973850abc529ed5790b581e8c0ef4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542466"
---
# <a name="data2-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="4d2a5-103">Элемент Data2 (ShapeSheet_Type Type) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4d2a5-103">Data2 element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="4d2a5-104">Содержит произвольное значение строки, которое используется для получения дополнительных сведений о фигуре.</span><span class="sxs-lookup"><span data-stu-id="4d2a5-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4d2a5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4d2a5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d2a5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4d2a5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4d2a5-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="4d2a5-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4d2a5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4d2a5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4d2a5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4d2a5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4d2a5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4d2a5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4d2a5-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="4d2a5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4d2a5-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="4d2a5-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4d2a5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4d2a5-113">Definition</span></span>

```XML
< xs:element name="Data2" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4d2a5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4d2a5-114">Elements and attributes</span></span>

<span data-ttu-id="4d2a5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4d2a5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4d2a5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4d2a5-116">Parent elements</span></span>

|<span data-ttu-id="4d2a5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4d2a5-117">**Element**</span></span>|<span data-ttu-id="4d2a5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4d2a5-118">**Type**</span></span>|<span data-ttu-id="4d2a5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4d2a5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4d2a5-120">Shape</span><span class="sxs-lookup"><span data-stu-id="4d2a5-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4d2a5-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="4d2a5-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4d2a5-122">Содержит элементы, определяющие фигуру в **элементе Master,** **Page** или group shape.</span><span class="sxs-lookup"><span data-stu-id="4d2a5-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4d2a5-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4d2a5-123">Child elements</span></span>

<span data-ttu-id="4d2a5-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="4d2a5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4d2a5-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4d2a5-125">Attributes</span></span>

<span data-ttu-id="4d2a5-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="4d2a5-126">None.</span></span>
  

