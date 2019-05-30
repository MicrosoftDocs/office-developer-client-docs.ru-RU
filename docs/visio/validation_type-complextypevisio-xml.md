---
title: Валидатион_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bc106ec-879a-0a4b-8c04-a5734eb0097a
ms.openlocfilehash: 7c7b3c8b1a5fdb52ee835c87e18941b902b51734
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538531"
---
# <a name="validationtype-complextype-visio-xml"></a><span data-ttu-id="8c669-102">Валидатион_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8c669-102">Validation_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8c669-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8c669-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8c669-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8c669-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8c669-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8c669-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8c669-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8c669-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8c669-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="8c669-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8c669-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8c669-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8c669-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8c669-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8c669-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8c669-110">Elements and attributes</span></span>

<span data-ttu-id="8c669-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8c669-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8c669-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8c669-112">Child elements</span></span>

|<span data-ttu-id="8c669-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8c669-113">**Element**</span></span>|<span data-ttu-id="8c669-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8c669-114">**Type**</span></span>|<span data-ttu-id="8c669-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8c669-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8c669-116">Issues</span><span class="sxs-lookup"><span data-stu-id="8c669-116">Issues</span></span>](issues-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c669-117">Иссуес_типе</span><span class="sxs-lookup"><span data-stu-id="8c669-117">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8c669-118">RuleSets</span><span class="sxs-lookup"><span data-stu-id="8c669-118">RuleSets</span></span>](rulesets-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c669-119">Рулесетс_типе</span><span class="sxs-lookup"><span data-stu-id="8c669-119">RuleSets_Type</span></span>](rulesets_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="8c669-120">Валидатионпропертиес</span><span class="sxs-lookup"><span data-stu-id="8c669-120">ValidationProperties</span></span>](validationproperties-element-validation_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8c669-121">Валидатионпропертиес_типе</span><span class="sxs-lookup"><span data-stu-id="8c669-121">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8c669-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8c669-122">Attributes</span></span>

<span data-ttu-id="8c669-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="8c669-123">None.</span></span>
  

