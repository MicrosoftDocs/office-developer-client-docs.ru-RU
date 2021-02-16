---
title: AutoLinkComparison_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: eeb58a0e2f401c0e8a2bcf67147bc300bb8535ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537887"
---
# <a name="autolinkcomparison_type-complextype-visio-xml"></a><span data-ttu-id="a23af-102">AutoLinkComparison_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a23af-102">AutoLinkComparison_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a23af-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a23af-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a23af-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a23af-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a23af-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a23af-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a23af-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a23af-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a23af-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a23af-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a23af-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="a23af-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a23af-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a23af-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a23af-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a23af-110">Elements and attributes</span></span>

<span data-ttu-id="a23af-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a23af-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a23af-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a23af-112">Child elements</span></span>

<span data-ttu-id="a23af-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="a23af-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a23af-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a23af-114">Attributes</span></span>

|<span data-ttu-id="a23af-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="a23af-115">**Attribute**</span></span>|<span data-ttu-id="a23af-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a23af-116">**Type**</span></span>|<span data-ttu-id="a23af-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="a23af-117">**Required**</span></span>|<span data-ttu-id="a23af-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a23af-118">**Description**</span></span>|<span data-ttu-id="a23af-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="a23af-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a23af-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="a23af-120">ColumnName</span></span>  <br/> |<span data-ttu-id="a23af-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a23af-121">xsd:string</span></span>  <br/> |<span data-ttu-id="a23af-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a23af-122">required</span></span>  <br/> ||<span data-ttu-id="a23af-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a23af-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="a23af-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="a23af-124">ContextType</span></span>  <br/> |<span data-ttu-id="a23af-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="a23af-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="a23af-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a23af-126">required</span></span>  <br/> ||<span data-ttu-id="a23af-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="a23af-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="a23af-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="a23af-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="a23af-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="a23af-129">xsd:string</span></span>  <br/> |<span data-ttu-id="a23af-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="a23af-130">optional</span></span>  <br/> ||<span data-ttu-id="a23af-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="a23af-131">Values of the xsd:string type.</span></span>  <br/> |
   

