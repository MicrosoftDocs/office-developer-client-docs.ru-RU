---
title: Validation_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 6f751db1566e39d919fd0a456d3aab72559ceeba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385594"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="b73fa-102">Validation_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b73fa-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b73fa-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b73fa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b73fa-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b73fa-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b73fa-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b73fa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b73fa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b73fa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b73fa-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b73fa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b73fa-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b73fa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b73fa-109">Определение</span><span class="sxs-lookup"><span data-stu-id="b73fa-109">Definition</span></span>

```XML
          <xs:complexType name="Validation_Type">
          
          <xs:sequence>
    <xs:element name="ValidationProperties"  type="ValidationProperties_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleSets"  type="RuleSets_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Issues"  type="Issues_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b73fa-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b73fa-110">Elements and attributes</span></span>

<span data-ttu-id="b73fa-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b73fa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b73fa-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b73fa-112">Child elements</span></span>

|<span data-ttu-id="b73fa-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b73fa-113">**Element**</span></span>|<span data-ttu-id="b73fa-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b73fa-114">**Type**</span></span>|<span data-ttu-id="b73fa-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b73fa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b73fa-116">Проблемы</span><span class="sxs-lookup"><span data-stu-id="b73fa-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b73fa-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="b73fa-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b73fa-118">Наборы правил</span><span class="sxs-lookup"><span data-stu-id="b73fa-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b73fa-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="b73fa-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b73fa-120">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="b73fa-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b73fa-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="b73fa-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b73fa-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b73fa-122">Attributes</span></span>

<span data-ttu-id="b73fa-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="b73fa-123">None.</span></span>
  

