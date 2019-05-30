---
title: Элемент Colors (Висиодокумент_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f439c2d-78be-5f2e-fa5a-f3feb83a0234
description: Содержит таблицу цветов документа.
ms.openlocfilehash: 6f18926961583e09f83dd7921ca140c07a60ecc3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540177"
---
# <a name="colors-element-visiodocumenttype-complextype-visio-xml"></a><span data-ttu-id="de31f-103">Элемент Colors (Висиодокумент_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="de31f-103">Colors element (VisioDocument_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="de31f-104">Содержит таблицу цветов документа.</span><span class="sxs-lookup"><span data-stu-id="de31f-104">Contains the document's color table.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de31f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="de31f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de31f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="de31f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="de31f-107">Колорс_типе</span><span class="sxs-lookup"><span data-stu-id="de31f-107">Colors_Type</span></span>](colors_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="de31f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="de31f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="de31f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="de31f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="de31f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="de31f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="de31f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="de31f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="de31f-112">Document. XML</span><span class="sxs-lookup"><span data-stu-id="de31f-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="de31f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="de31f-113">Definition</span></span>

```XML
< xs:element name="Colors" type="Colors_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="de31f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="de31f-114">Elements and attributes</span></span>

<span data-ttu-id="de31f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="de31f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="de31f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="de31f-116">Parent elements</span></span>

|<span data-ttu-id="de31f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="de31f-117">**Element**</span></span>|<span data-ttu-id="de31f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="de31f-118">**Type**</span></span>|<span data-ttu-id="de31f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de31f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="de31f-120">Висиодокумент</span><span class="sxs-lookup"><span data-stu-id="de31f-120">VisioDocument</span></span>](visiodocument-elementvisio-xml.md) <br/> |[<span data-ttu-id="de31f-121">Висиодокумент_типе</span><span class="sxs-lookup"><span data-stu-id="de31f-121">VisioDocument_Type</span></span>](visiodocument_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="de31f-122">Корневой элемент документа Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="de31f-122">The root element of a Microsoft Visio document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="de31f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="de31f-123">Child elements</span></span>

|<span data-ttu-id="de31f-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="de31f-124">**Element**</span></span>|<span data-ttu-id="de31f-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="de31f-125">**Type**</span></span>|<span data-ttu-id="de31f-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="de31f-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="de31f-127">Колорентри</span><span class="sxs-lookup"><span data-stu-id="de31f-127">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="de31f-128">Колорентри_типе</span><span class="sxs-lookup"><span data-stu-id="de31f-128">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="de31f-129">Содержит запись таблицы цветов.</span><span class="sxs-lookup"><span data-stu-id="de31f-129">Contains a color table entry.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="de31f-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="de31f-130">Attributes</span></span>

<span data-ttu-id="de31f-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="de31f-131">None.</span></span>
  

