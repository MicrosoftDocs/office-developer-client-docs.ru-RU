---
title: Элемент Data1 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d72dc0e4-4e0f-dd3f-a51a-8486f9ec548e
description: Содержит произвольное строку, используемую для получения дополнительных сведений о фигуре.
ms.openlocfilehash: e4ff724eee51e3a7efe8bc4f270568da066901a5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542487"
---
# <a name="data1-element-shapesheet_type-complextype-visio-xml"></a><span data-ttu-id="98c85-103">Элемент Data1 (ShapeSheet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="98c85-103">Data1 element (ShapeSheet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="98c85-104">Содержит произвольное строку, используемую для получения дополнительных сведений о фигуре.</span><span class="sxs-lookup"><span data-stu-id="98c85-104">Contains an arbitrary string value that is used to supply additional information about a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="98c85-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="98c85-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="98c85-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="98c85-106">**Element type**</span></span> <br/> |[<span data-ttu-id="98c85-107">Data_Type</span><span class="sxs-lookup"><span data-stu-id="98c85-107">Data_Type</span></span>](data_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="98c85-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="98c85-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="98c85-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="98c85-109">**Schema file**</span></span> <br/> |<span data-ttu-id="98c85-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="98c85-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="98c85-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="98c85-111">**Document parts**</span></span> <br/> |<span data-ttu-id="98c85-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="98c85-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="98c85-113">Определение</span><span class="sxs-lookup"><span data-stu-id="98c85-113">Definition</span></span>

```XML
< xs:element name="Data1" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="98c85-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="98c85-114">Elements and attributes</span></span>

<span data-ttu-id="98c85-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="98c85-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="98c85-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="98c85-116">Parent elements</span></span>

|<span data-ttu-id="98c85-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="98c85-117">**Element**</span></span>|<span data-ttu-id="98c85-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="98c85-118">**Type**</span></span>|<span data-ttu-id="98c85-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="98c85-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="98c85-120">Shape</span><span class="sxs-lookup"><span data-stu-id="98c85-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="98c85-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="98c85-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="98c85-122">Содержит элементы, определяющие фигуру в элементе **"Master",** **"Page"** или "group shape".</span><span class="sxs-lookup"><span data-stu-id="98c85-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="98c85-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="98c85-123">Child elements</span></span>

<span data-ttu-id="98c85-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="98c85-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="98c85-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="98c85-125">Attributes</span></span>

<span data-ttu-id="98c85-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="98c85-126">None.</span></span>
  

