---
title: RuleInfo_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382570"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="05820-102">RuleInfo_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="05820-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="05820-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="05820-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05820-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="05820-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="05820-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="05820-105">**Schema file**</span></span> <br/> |<span data-ttu-id="05820-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="05820-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="05820-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="05820-107">**Extension base**</span></span> <br/> |<span data-ttu-id="05820-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="05820-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="05820-109">Определение</span><span class="sxs-lookup"><span data-stu-id="05820-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="05820-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="05820-110">Elements and attributes</span></span>

<span data-ttu-id="05820-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="05820-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="05820-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="05820-112">Child elements</span></span>

<span data-ttu-id="05820-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="05820-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05820-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="05820-114">Attributes</span></span>

|<span data-ttu-id="05820-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="05820-115">**Attribute**</span></span>|<span data-ttu-id="05820-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="05820-116">**Type**</span></span>|<span data-ttu-id="05820-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="05820-117">**Required**</span></span>|<span data-ttu-id="05820-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="05820-118">**Description**</span></span>|<span data-ttu-id="05820-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="05820-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="05820-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="05820-120">RuleID</span></span>  <br/> |<span data-ttu-id="05820-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="05820-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="05820-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="05820-122">required</span></span>  <br/> ||<span data-ttu-id="05820-123">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="05820-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="05820-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="05820-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="05820-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="05820-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="05820-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="05820-126">required</span></span>  <br/> ||<span data-ttu-id="05820-127">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="05820-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

