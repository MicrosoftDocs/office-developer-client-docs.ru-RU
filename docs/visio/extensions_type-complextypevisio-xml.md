---
title: Extensions_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5f516e1a-e789-8085-1cc3-70514910eb26
ms.openlocfilehash: 1da1418e2256f7750ac2e963bac0f78321233c99
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813731"
---
# <a name="extensionstype-complextype-visio-xml"></a><span data-ttu-id="d3908-102">Extensions_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d3908-102">Extensions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d3908-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d3908-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d3908-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d3908-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d3908-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d3908-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d3908-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d3908-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d3908-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="d3908-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d3908-108">Нет</span><span class="sxs-lookup"><span data-stu-id="d3908-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d3908-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d3908-109">Definition</span></span>

```XML
          <xs:complexType name="Extensions_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="FunctionDef"  type="FunctionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="SectionDef"  type="SectionDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d3908-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d3908-110">Elements and attributes</span></span>

<span data-ttu-id="d3908-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="d3908-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d3908-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d3908-112">Child elements</span></span>

|<span data-ttu-id="d3908-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d3908-113">**Element**</span></span>|<span data-ttu-id="d3908-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d3908-114">**Type**</span></span>|<span data-ttu-id="d3908-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d3908-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d3908-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="d3908-116">CellDef</span></span>](http://msdn.microsoft.com/library/8fb193f0-5c88-6891-1cda-f1df486aabfc%28Office.15%29.aspx) <br/> |[<span data-ttu-id="d3908-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="d3908-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3908-118">FunctionDef</span><span class="sxs-lookup"><span data-stu-id="d3908-118">FunctionDef</span></span>](http://msdn.microsoft.com/library/dad99181-c14c-cce7-3883-106fe05f20a6%28Office.15%29.aspx) <br/> |[<span data-ttu-id="d3908-119">FunctionDef_Type</span><span class="sxs-lookup"><span data-stu-id="d3908-119">FunctionDef_Type</span></span>](functiondef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d3908-120">SectionDef</span><span class="sxs-lookup"><span data-stu-id="d3908-120">SectionDef</span></span>](http://msdn.microsoft.com/library/751da480-f387-4c68-6699-8948271c23ac%28Office.15%29.aspx) <br/> |[<span data-ttu-id="d3908-121">SectionDef_Type</span><span class="sxs-lookup"><span data-stu-id="d3908-121">SectionDef_Type</span></span>](sectiondef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d3908-122">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d3908-122">Attributes</span></span>

<span data-ttu-id="d3908-123">Нет.</span><span class="sxs-lookup"><span data-stu-id="d3908-123">None.</span></span>
  

