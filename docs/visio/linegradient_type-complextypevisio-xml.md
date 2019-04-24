---
title: Линеградиент_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b36eb8f-d1af-9bbc-2822-0c3d09dfc2a9
ms.openlocfilehash: 5918e306479b907760fb539c3e476708d28de5e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359291"
---
# <a name="linegradienttype-complextype-visio-xml"></a><span data-ttu-id="9bce1-102">Линеградиент_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="9bce1-102">LineGradient_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9bce1-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9bce1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bce1-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9bce1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9bce1-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9bce1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9bce1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9bce1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9bce1-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="9bce1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9bce1-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="9bce1-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9bce1-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9bce1-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LineGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9bce1-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9bce1-110">Elements and attributes</span></span>

<span data-ttu-id="9bce1-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="9bce1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9bce1-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9bce1-112">Child elements</span></span>

|<span data-ttu-id="9bce1-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9bce1-113">**Element**</span></span>|<span data-ttu-id="9bce1-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9bce1-114">**Type**</span></span>|<span data-ttu-id="9bce1-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9bce1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9bce1-116">Row</span><span class="sxs-lookup"><span data-stu-id="9bce1-116">Row</span></span>](row-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="9bce1-117">Линеградиентров_типе</span><span class="sxs-lookup"><span data-stu-id="9bce1-117">LineGradientRow_Type</span></span>](linegradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9bce1-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9bce1-118">Attributes</span></span>

<span data-ttu-id="9bce1-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="9bce1-119">None.</span></span>
  

