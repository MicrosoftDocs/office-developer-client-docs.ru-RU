---
title: RuleInfo_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0a0ac32729b83a5d648b2826bffe5a9df4d9fc0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814693"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="c509b-102">RuleInfo_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c509b-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c509b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c509b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c509b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c509b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c509b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c509b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c509b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c509b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c509b-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="c509b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c509b-108">Нет</span><span class="sxs-lookup"><span data-stu-id="c509b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c509b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c509b-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c509b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c509b-110">Elements and attributes</span></span>

<span data-ttu-id="c509b-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="c509b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c509b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c509b-112">Child elements</span></span>

<span data-ttu-id="c509b-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="c509b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c509b-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c509b-114">Attributes</span></span>

|<span data-ttu-id="c509b-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="c509b-115">**Attribute**</span></span>|<span data-ttu-id="c509b-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c509b-116">**Type**</span></span>|<span data-ttu-id="c509b-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="c509b-117">**Required**</span></span>|<span data-ttu-id="c509b-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c509b-118">**Description**</span></span>|<span data-ttu-id="c509b-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="c509b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c509b-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="c509b-120">RuleID</span></span>  <br/> |<span data-ttu-id="c509b-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c509b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c509b-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c509b-122">required</span></span>  <br/> ||<span data-ttu-id="c509b-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c509b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c509b-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="c509b-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="c509b-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c509b-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c509b-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c509b-126">required</span></span>  <br/> ||<span data-ttu-id="c509b-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c509b-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

