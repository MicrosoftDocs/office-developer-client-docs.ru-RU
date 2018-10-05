---
title: Solutions_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: bf43b971399ec69c6f73cbfaaa6cade8c583d3c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400539"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="c8180-102">Solutions_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c8180-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c8180-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="c8180-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8180-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c8180-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c8180-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c8180-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c8180-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c8180-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c8180-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="c8180-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c8180-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="c8180-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8180-109">Определение</span><span class="sxs-lookup"><span data-stu-id="c8180-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c8180-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c8180-110">Elements and attributes</span></span>

<span data-ttu-id="c8180-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c8180-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c8180-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c8180-112">Child elements</span></span>

|<span data-ttu-id="c8180-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c8180-113">**Element**</span></span>|<span data-ttu-id="c8180-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c8180-114">**Type**</span></span>|<span data-ttu-id="c8180-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c8180-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8180-116">Решение</span><span class="sxs-lookup"><span data-stu-id="c8180-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c8180-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="c8180-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c8180-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c8180-118">Attributes</span></span>

<span data-ttu-id="c8180-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="c8180-119">None.</span></span>
  

