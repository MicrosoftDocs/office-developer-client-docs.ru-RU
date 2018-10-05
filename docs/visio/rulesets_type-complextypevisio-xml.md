---
title: RuleSets_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9bd05541-7cd8-321b-8dd6-fa885c269057
ms.openlocfilehash: 41172a4f15b0d9038fd0ffb0c0a7d8c3d4078798
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385923"
---
# <a name="rulesetstype-complextype-visio-xml"></a><span data-ttu-id="421ef-102">RuleSets_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="421ef-102">RuleSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="421ef-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="421ef-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="421ef-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="421ef-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="421ef-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="421ef-105">**Schema file**</span></span> <br/> |<span data-ttu-id="421ef-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="421ef-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="421ef-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="421ef-107">**Extension base**</span></span> <br/> |<span data-ttu-id="421ef-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="421ef-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="421ef-109">Определение</span><span class="sxs-lookup"><span data-stu-id="421ef-109">Definition</span></span>

```XML
          <xs:complexType name="RuleSets_Type">
          
          <xs:sequence>
    <xs:element name="RuleSet"  type="RuleSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="421ef-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="421ef-110">Elements and attributes</span></span>

<span data-ttu-id="421ef-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="421ef-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="421ef-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="421ef-112">Child elements</span></span>

|<span data-ttu-id="421ef-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="421ef-113">**Element**</span></span>|<span data-ttu-id="421ef-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="421ef-114">**Type**</span></span>|<span data-ttu-id="421ef-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="421ef-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="421ef-116">Набор правил</span><span class="sxs-lookup"><span data-stu-id="421ef-116">RuleSet</span></span>](ruleset-element-rulesets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="421ef-117">RuleSet_Type</span><span class="sxs-lookup"><span data-stu-id="421ef-117">RuleSet_Type</span></span>](ruleset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="421ef-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="421ef-118">Attributes</span></span>

<span data-ttu-id="421ef-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="421ef-119">None.</span></span>
  

