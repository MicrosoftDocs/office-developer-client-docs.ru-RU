---
title: Issue_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: 1cdc38db93da57969230c280a2df24ac3b20ad0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399700"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="60b1f-102">Issue_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="60b1f-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="60b1f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="60b1f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60b1f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="60b1f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="60b1f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="60b1f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="60b1f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="60b1f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="60b1f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="60b1f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="60b1f-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="60b1f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="60b1f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="60b1f-109">Definition</span></span>

```XML
          <xs:complexType name="Issue_Type">
          
          <xs:sequence>
    <xs:element name="IssueTarget"  type="IssueTarget_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleInfo"  type="RuleInfo_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="60b1f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="60b1f-110">Elements and attributes</span></span>

<span data-ttu-id="60b1f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="60b1f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="60b1f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="60b1f-112">Child elements</span></span>

|<span data-ttu-id="60b1f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="60b1f-113">**Element**</span></span>|<span data-ttu-id="60b1f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="60b1f-114">**Type**</span></span>|<span data-ttu-id="60b1f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="60b1f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="60b1f-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="60b1f-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="60b1f-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="60b1f-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="60b1f-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="60b1f-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="60b1f-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="60b1f-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="60b1f-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="60b1f-120">Attributes</span></span>

|<span data-ttu-id="60b1f-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="60b1f-121">**Attribute**</span></span>|<span data-ttu-id="60b1f-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="60b1f-122">**Type**</span></span>|<span data-ttu-id="60b1f-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="60b1f-123">**Required**</span></span>|<span data-ttu-id="60b1f-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="60b1f-124">**Description**</span></span>|<span data-ttu-id="60b1f-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="60b1f-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="60b1f-126">ID</span><span class="sxs-lookup"><span data-stu-id="60b1f-126">ID</span></span>  <br/> |<span data-ttu-id="60b1f-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="60b1f-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="60b1f-128">Обязательный</span><span class="sxs-lookup"><span data-stu-id="60b1f-128">required</span></span>  <br/> ||<span data-ttu-id="60b1f-129">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="60b1f-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="60b1f-130">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="60b1f-130">Ignored</span></span>  <br/> |<span data-ttu-id="60b1f-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="60b1f-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="60b1f-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="60b1f-132">optional</span></span>  <br/> ||<span data-ttu-id="60b1f-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="60b1f-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

