---
title: AutoLinkComparison_Type complexType (XML для Visio)
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
# <a name="autolinkcomparison_type-complextype-visio-xml"></a><span data-ttu-id="e8f31-102">AutoLinkComparison_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="e8f31-102">AutoLinkComparison_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e8f31-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e8f31-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8f31-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e8f31-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e8f31-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e8f31-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e8f31-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e8f31-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e8f31-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="e8f31-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e8f31-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="e8f31-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e8f31-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e8f31-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e8f31-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e8f31-110">Elements and attributes</span></span>

<span data-ttu-id="e8f31-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e8f31-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e8f31-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e8f31-112">Child elements</span></span>

<span data-ttu-id="e8f31-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="e8f31-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8f31-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e8f31-114">Attributes</span></span>

|<span data-ttu-id="e8f31-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e8f31-115">**Attribute**</span></span>|<span data-ttu-id="e8f31-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e8f31-116">**Type**</span></span>|<span data-ttu-id="e8f31-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e8f31-117">**Required**</span></span>|<span data-ttu-id="e8f31-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e8f31-118">**Description**</span></span>|<span data-ttu-id="e8f31-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e8f31-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e8f31-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="e8f31-120">ColumnName</span></span>  <br/> |<span data-ttu-id="e8f31-121">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e8f31-121">xsd:string</span></span>  <br/> |<span data-ttu-id="e8f31-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e8f31-122">required</span></span>  <br/> ||<span data-ttu-id="e8f31-123">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e8f31-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e8f31-124">контексттипе</span><span class="sxs-lookup"><span data-stu-id="e8f31-124">ContextType</span></span>  <br/> |<span data-ttu-id="e8f31-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="e8f31-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e8f31-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e8f31-126">required</span></span>  <br/> ||<span data-ttu-id="e8f31-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="e8f31-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e8f31-128">контексттипелабел</span><span class="sxs-lookup"><span data-stu-id="e8f31-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="e8f31-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="e8f31-129">xsd:string</span></span>  <br/> |<span data-ttu-id="e8f31-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="e8f31-130">optional</span></span>  <br/> ||<span data-ttu-id="e8f31-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="e8f31-131">Values of the xsd:string type.</span></span>  <br/> |
   

