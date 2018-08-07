---
title: Validation_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 26e7dec4ea54e118afd85ec25f334e69849a57dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19815132"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="56e1c-102">Validation_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="56e1c-102">Validation_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="56e1c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="56e1c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="56e1c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="56e1c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="56e1c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="56e1c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="56e1c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="56e1c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="56e1c-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="56e1c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="56e1c-108">Нет</span><span class="sxs-lookup"><span data-stu-id="56e1c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="56e1c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="56e1c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="56e1c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="56e1c-110">Elements and attributes</span></span>

<span data-ttu-id="56e1c-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="56e1c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="56e1c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="56e1c-112">Child elements</span></span>

|<span data-ttu-id="56e1c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="56e1c-113">**Element**</span></span>|<span data-ttu-id="56e1c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="56e1c-114">**Type**</span></span>|<span data-ttu-id="56e1c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56e1c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="56e1c-116">Проблемы</span><span class="sxs-lookup"><span data-stu-id="56e1c-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="56e1c-117">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="56e1c-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="56e1c-118">Наборы правил</span><span class="sxs-lookup"><span data-stu-id="56e1c-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="56e1c-119">RuleSets_Type</span><span class="sxs-lookup"><span data-stu-id="56e1c-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="56e1c-120">ValidationProperties</span><span class="sxs-lookup"><span data-stu-id="56e1c-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="56e1c-121">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="56e1c-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="56e1c-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="56e1c-122">Attributes</span></span>

<span data-ttu-id="56e1c-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="56e1c-123">None.</span></span>
  

