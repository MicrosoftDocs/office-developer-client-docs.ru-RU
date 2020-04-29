---
title: RuleInfo_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 8e7b04e938997786cf0dc99e92057f77cfe0cf76
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541647"
---
# <a name="ruleinfo_type-complextype-visio-xml"></a><span data-ttu-id="b4a70-102">RuleInfo_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="b4a70-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b4a70-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b4a70-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4a70-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b4a70-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b4a70-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b4a70-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b4a70-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b4a70-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b4a70-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b4a70-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b4a70-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b4a70-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4a70-109">Определение</span><span class="sxs-lookup"><span data-stu-id="b4a70-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b4a70-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b4a70-110">Elements and attributes</span></span>

<span data-ttu-id="b4a70-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b4a70-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b4a70-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b4a70-112">Child elements</span></span>

<span data-ttu-id="b4a70-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="b4a70-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4a70-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b4a70-114">Attributes</span></span>

|<span data-ttu-id="b4a70-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b4a70-115">**Attribute**</span></span>|<span data-ttu-id="b4a70-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b4a70-116">**Type**</span></span>|<span data-ttu-id="b4a70-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b4a70-117">**Required**</span></span>|<span data-ttu-id="b4a70-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b4a70-118">**Description**</span></span>|<span data-ttu-id="b4a70-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b4a70-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b4a70-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="b4a70-120">RuleID</span></span>  <br/> |<span data-ttu-id="b4a70-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="b4a70-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b4a70-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b4a70-122">required</span></span>  <br/> ||<span data-ttu-id="b4a70-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="b4a70-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b4a70-124">рулесетид</span><span class="sxs-lookup"><span data-stu-id="b4a70-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="b4a70-125">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="b4a70-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b4a70-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b4a70-126">required</span></span>  <br/> ||<span data-ttu-id="b4a70-127">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="b4a70-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

