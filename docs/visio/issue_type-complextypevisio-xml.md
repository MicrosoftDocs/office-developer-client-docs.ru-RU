---
title: Issue_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: b351554fe7919cada99172f721f5dbe2fd8f243a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542963"
---
# <a name="issue_type-complextype-visio-xml"></a><span data-ttu-id="31c3e-102">Issue_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="31c3e-102">Issue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="31c3e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="31c3e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31c3e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="31c3e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="31c3e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="31c3e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="31c3e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="31c3e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="31c3e-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="31c3e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="31c3e-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="31c3e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31c3e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="31c3e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="31c3e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="31c3e-110">Elements and attributes</span></span>

<span data-ttu-id="31c3e-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="31c3e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="31c3e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="31c3e-112">Child elements</span></span>

|<span data-ttu-id="31c3e-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="31c3e-113">**Element**</span></span>|<span data-ttu-id="31c3e-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="31c3e-114">**Type**</span></span>|<span data-ttu-id="31c3e-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="31c3e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="31c3e-116">иссуетаржет</span><span class="sxs-lookup"><span data-stu-id="31c3e-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="31c3e-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="31c3e-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="31c3e-118">рулеинфо</span><span class="sxs-lookup"><span data-stu-id="31c3e-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="31c3e-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="31c3e-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="31c3e-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="31c3e-120">Attributes</span></span>

|<span data-ttu-id="31c3e-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="31c3e-121">**Attribute**</span></span>|<span data-ttu-id="31c3e-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="31c3e-122">**Type**</span></span>|<span data-ttu-id="31c3e-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="31c3e-123">**Required**</span></span>|<span data-ttu-id="31c3e-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="31c3e-124">**Description**</span></span>|<span data-ttu-id="31c3e-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="31c3e-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="31c3e-126">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="31c3e-126">ID</span></span>  <br/> |<span data-ttu-id="31c3e-127">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="31c3e-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="31c3e-128">Обязательный</span><span class="sxs-lookup"><span data-stu-id="31c3e-128">required</span></span>  <br/> ||<span data-ttu-id="31c3e-129">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="31c3e-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="31c3e-130">Игнорирован</span><span class="sxs-lookup"><span data-stu-id="31c3e-130">Ignored</span></span>  <br/> |<span data-ttu-id="31c3e-131">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="31c3e-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="31c3e-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="31c3e-132">optional</span></span>  <br/> ||<span data-ttu-id="31c3e-133">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="31c3e-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

