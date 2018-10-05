---
title: Элемент бд2 (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e823797e-dde9-6ee7-b5e4-9e57cef90b08
description: Содержит произвольное строковое значение, которое используется для предоставления дополнительной информации о фигуры.
ms.openlocfilehash: ebd70fc0f83bd7cbf0bd6465c5e06276675a8022
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401715"
---
# <a name="data2-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="b8e56-103">Элемент бд2 (ShapeSheet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b8e56-103">Data2 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b8e56-104">Содержит произвольное строковое значение, которое используется для предоставления дополнительной информации о фигуры.</span><span class="sxs-lookup"><span data-stu-id="b8e56-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b8e56-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b8e56-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8e56-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b8e56-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b8e56-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="b8e56-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b8e56-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b8e56-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b8e56-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b8e56-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b8e56-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b8e56-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b8e56-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b8e56-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b8e56-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="b8e56-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b8e56-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b8e56-113">Definition</span></span>

```XML
< xs:element name="Data2" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b8e56-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b8e56-114">Elements and attributes</span></span>

<span data-ttu-id="b8e56-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b8e56-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b8e56-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b8e56-116">Parent elements</span></span>

|<span data-ttu-id="b8e56-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b8e56-117">**Element**</span></span>|<span data-ttu-id="b8e56-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b8e56-118">**Type**</span></span>|<span data-ttu-id="b8e56-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b8e56-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8e56-120">Фигура</span><span class="sxs-lookup"><span data-stu-id="b8e56-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8e56-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="b8e56-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b8e56-122">Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.</span><span class="sxs-lookup"><span data-stu-id="b8e56-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b8e56-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b8e56-123">Child elements</span></span>

<span data-ttu-id="b8e56-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="b8e56-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b8e56-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b8e56-125">Attributes</span></span>

<span data-ttu-id="b8e56-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="b8e56-126">None.</span></span>
  

