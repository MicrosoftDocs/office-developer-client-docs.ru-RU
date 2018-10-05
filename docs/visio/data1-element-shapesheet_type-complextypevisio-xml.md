---
title: Элемент бд1 (ShapeSheet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d72dc0e4-4e0f-dd3f-a51a-8486f9ec548e
description: Содержит произвольное строковое значение, которое используется для предоставления дополнительной информации о фигуры.
ms.openlocfilehash: a203f915e9a5ff86e7cf75d96639157f76d3c151
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390970"
---
# <a name="data1-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="10b46-103">Элемент бд1 (ShapeSheet_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="10b46-103">Data1 element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="10b46-104">Содержит произвольное строковое значение, которое используется для предоставления дополнительной информации о фигуры.</span><span class="sxs-lookup"><span data-stu-id="10b46-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="10b46-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="10b46-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="10b46-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="10b46-106">**Element type**</span></span> <br/> |[<span data-ttu-id="10b46-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="10b46-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="10b46-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="10b46-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="10b46-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="10b46-109">**Schema file**</span></span> <br/> |<span data-ttu-id="10b46-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="10b46-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="10b46-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="10b46-111">**Document parts**</span></span> <br/> |<span data-ttu-id="10b46-112">страницы # .xml, главные # .xml</span><span class="sxs-lookup"><span data-stu-id="10b46-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="10b46-113">Определение</span><span class="sxs-lookup"><span data-stu-id="10b46-113">Definition</span></span>

```XML
< xs:element name="Data1" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="10b46-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="10b46-114">Elements and attributes</span></span>

<span data-ttu-id="10b46-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="10b46-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="10b46-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="10b46-116">Parent elements</span></span>

|<span data-ttu-id="10b46-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="10b46-117">**Element**</span></span>|<span data-ttu-id="10b46-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="10b46-118">**Type**</span></span>|<span data-ttu-id="10b46-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10b46-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="10b46-120">Фигура</span><span class="sxs-lookup"><span data-stu-id="10b46-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="10b46-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="10b46-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="10b46-122">Содержит элементы, определяющие фигуры в **Образец**, **страница**или элемент группы фигур.</span><span class="sxs-lookup"><span data-stu-id="10b46-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="10b46-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="10b46-123">Child elements</span></span>

<span data-ttu-id="10b46-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="10b46-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="10b46-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="10b46-125">Attributes</span></span>

<span data-ttu-id="10b46-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="10b46-126">None.</span></span>
  

