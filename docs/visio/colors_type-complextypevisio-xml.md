---
title: Колорс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: e447ceb6fc0e6b79ec6e62b5f3b73a32cec589d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359026"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="2ed6d-102">Колорс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2ed6d-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2ed6d-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2ed6d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ed6d-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2ed6d-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2ed6d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2ed6d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2ed6d-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2ed6d-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="2ed6d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2ed6d-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2ed6d-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2ed6d-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2ed6d-110">Elements and attributes</span></span>

<span data-ttu-id="2ed6d-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2ed6d-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2ed6d-112">Child elements</span></span>

|<span data-ttu-id="2ed6d-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-113">**Element**</span></span>|<span data-ttu-id="2ed6d-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-114">**Type**</span></span>|<span data-ttu-id="2ed6d-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2ed6d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2ed6d-116">Колорентри</span><span class="sxs-lookup"><span data-stu-id="2ed6d-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2ed6d-117">Колорентри_типе</span><span class="sxs-lookup"><span data-stu-id="2ed6d-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2ed6d-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2ed6d-118">Attributes</span></span>

<span data-ttu-id="2ed6d-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="2ed6d-119">None.</span></span>
  

