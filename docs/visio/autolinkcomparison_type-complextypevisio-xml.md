---
title: AutoLinkComparison_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: bb1b07a59fbe3fc706bc67db58e67c5b0ec14033
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813165"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="bf49f-102">AutoLinkComparison_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="bf49f-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bf49f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="bf49f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf49f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bf49f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bf49f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bf49f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bf49f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bf49f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bf49f-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="bf49f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bf49f-108">Нет</span><span class="sxs-lookup"><span data-stu-id="bf49f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf49f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="bf49f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bf49f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bf49f-110">Elements and attributes</span></span>

<span data-ttu-id="bf49f-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="bf49f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bf49f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bf49f-112">Child elements</span></span>

<span data-ttu-id="bf49f-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="bf49f-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bf49f-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bf49f-114">Attributes</span></span>

|<span data-ttu-id="bf49f-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="bf49f-115">**Attribute**</span></span>|<span data-ttu-id="bf49f-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bf49f-116">**Type**</span></span>|<span data-ttu-id="bf49f-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="bf49f-117">**Required**</span></span>|<span data-ttu-id="bf49f-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bf49f-118">**Description**</span></span>|<span data-ttu-id="bf49f-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="bf49f-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bf49f-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="bf49f-120">ColumnName</span></span>  <br/> |<span data-ttu-id="bf49f-121">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bf49f-121">xsd:string</span></span>  <br/> |<span data-ttu-id="bf49f-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf49f-122">required</span></span>  <br/> ||<span data-ttu-id="bf49f-123">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bf49f-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="bf49f-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="bf49f-124">ContextType</span></span>  <br/> |<span data-ttu-id="bf49f-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bf49f-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bf49f-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="bf49f-126">required</span></span>  <br/> ||<span data-ttu-id="bf49f-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bf49f-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bf49f-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="bf49f-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="bf49f-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="bf49f-129">xsd:string</span></span>  <br/> |<span data-ttu-id="bf49f-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="bf49f-130">optional</span></span>  <br/> ||<span data-ttu-id="bf49f-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="bf49f-131">Values of the xsd:string type.</span></span>  <br/> |
   

