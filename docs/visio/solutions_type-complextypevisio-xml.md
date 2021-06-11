---
title: Solutions_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: b68955d2ed161d1ec0952b4a1b9d657fe0de81fc
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540233"
---
# <a name="solutions_type-complextype-visio-xml"></a><span data-ttu-id="1a09f-102">Solutions_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1a09f-102">Solutions_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1a09f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1a09f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a09f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1a09f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1a09f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1a09f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1a09f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1a09f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1a09f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1a09f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1a09f-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1a09f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a09f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1a09f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1a09f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1a09f-110">Elements and attributes</span></span>

<span data-ttu-id="1a09f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1a09f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1a09f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1a09f-112">Child elements</span></span>

|<span data-ttu-id="1a09f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1a09f-113">**Element**</span></span>|<span data-ttu-id="1a09f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1a09f-114">**Type**</span></span>|<span data-ttu-id="1a09f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1a09f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1a09f-116">Решение</span><span class="sxs-lookup"><span data-stu-id="1a09f-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1a09f-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="1a09f-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1a09f-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1a09f-118">Attributes</span></span>

<span data-ttu-id="1a09f-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="1a09f-119">None.</span></span>
  

