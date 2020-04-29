---
title: Элемент data3 (ShapeSheet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 63493467-af55-fa62-6c39-6b5896895952
description: Содержит произвольное строковое значение, которое используется для предоставления дополнительных сведений о фигуре.
ms.openlocfilehash: 1ce286c0c8db53305f78def465ac31a3ef3afdec
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541255"
---
# <a name="data3-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="6e8a6-103">Элемент data3 (ShapeSheet_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="6e8a6-103">Data3 element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6e8a6-104">Содержит произвольное строковое значение, которое используется для предоставления дополнительных сведений о фигуре.</span><span class="sxs-lookup"><span data-stu-id="6e8a6-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6e8a6-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6e8a6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e8a6-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6e8a6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6e8a6-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="6e8a6-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6e8a6-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6e8a6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6e8a6-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6e8a6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6e8a6-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6e8a6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6e8a6-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="6e8a6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6e8a6-112">страница #. XML, Master #. XML</span><span class="sxs-lookup"><span data-stu-id="6e8a6-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e8a6-113">Определение</span><span class="sxs-lookup"><span data-stu-id="6e8a6-113">Definition</span></span>

```XML
< xs:element name="Data3" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6e8a6-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e8a6-114">Elements and attributes</span></span>

<span data-ttu-id="6e8a6-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6e8a6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6e8a6-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6e8a6-116">Parent elements</span></span>

|<span data-ttu-id="6e8a6-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6e8a6-117">**Element**</span></span>|<span data-ttu-id="6e8a6-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6e8a6-118">**Type**</span></span>|<span data-ttu-id="6e8a6-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e8a6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e8a6-120">Shape</span><span class="sxs-lookup"><span data-stu-id="6e8a6-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6e8a6-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="6e8a6-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6e8a6-122">Содержит элементы, определяющие фигуру в **главной**, **странице**или элементе фигуры группы.</span><span class="sxs-lookup"><span data-stu-id="6e8a6-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6e8a6-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6e8a6-123">Child elements</span></span>

<span data-ttu-id="6e8a6-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="6e8a6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6e8a6-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e8a6-125">Attributes</span></span>

<span data-ttu-id="6e8a6-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="6e8a6-126">None.</span></span>
  

