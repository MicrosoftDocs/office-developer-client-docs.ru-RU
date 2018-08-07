---
title: Issue_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: f0346c20e4a290819e3f23a0384a59b308a5e907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814031"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="e397c-102">Issue_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e397c-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e397c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e397c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e397c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e397c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e397c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e397c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e397c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e397c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e397c-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="e397c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e397c-108">Нет</span><span class="sxs-lookup"><span data-stu-id="e397c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e397c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e397c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e397c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e397c-110">Elements and attributes</span></span>

<span data-ttu-id="e397c-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="e397c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e397c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e397c-112">Child elements</span></span>

|<span data-ttu-id="e397c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e397c-113">**Element**</span></span>|<span data-ttu-id="e397c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e397c-114">**Type**</span></span>|<span data-ttu-id="e397c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e397c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e397c-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="e397c-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e397c-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="e397c-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e397c-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="e397c-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e397c-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="e397c-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e397c-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e397c-120">Attributes</span></span>

|<span data-ttu-id="e397c-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e397c-121">**Attribute**</span></span>|<span data-ttu-id="e397c-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e397c-122">**Type**</span></span>|<span data-ttu-id="e397c-123">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="e397c-123">**Required**</span></span>|<span data-ttu-id="e397c-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e397c-124">**Description**</span></span>|<span data-ttu-id="e397c-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e397c-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e397c-126">ID</span><span class="sxs-lookup"><span data-stu-id="e397c-126">ID</span></span>  <br/> |<span data-ttu-id="e397c-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e397c-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e397c-128">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e397c-128">required</span></span>  <br/> ||<span data-ttu-id="e397c-129">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e397c-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e397c-130">Игнорируется</span><span class="sxs-lookup"><span data-stu-id="e397c-130">Ignored</span></span>  <br/> |<span data-ttu-id="e397c-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="e397c-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e397c-132">необязательный</span><span class="sxs-lookup"><span data-stu-id="e397c-132">optional</span></span>  <br/> ||<span data-ttu-id="e397c-133">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e397c-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

