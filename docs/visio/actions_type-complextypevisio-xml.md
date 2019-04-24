---
title: Актионс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 158a0dfa31c2da3ac9e530c07edd075b4fabbd75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283053"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="7d20c-102">Актионс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="7d20c-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7d20c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7d20c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d20c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7d20c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7d20c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7d20c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7d20c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7d20c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7d20c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7d20c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7d20c-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="7d20c-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d20c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7d20c-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7d20c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7d20c-110">Elements and attributes</span></span>

<span data-ttu-id="7d20c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7d20c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7d20c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7d20c-112">Child elements</span></span>

|<span data-ttu-id="7d20c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7d20c-113">**Element**</span></span>|<span data-ttu-id="7d20c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7d20c-114">**Type**</span></span>|<span data-ttu-id="7d20c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7d20c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d20c-116">Row</span><span class="sxs-lookup"><span data-stu-id="7d20c-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7d20c-117">Актионсров_типе</span><span class="sxs-lookup"><span data-stu-id="7d20c-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7d20c-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7d20c-118">Attributes</span></span>

<span data-ttu-id="7d20c-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="7d20c-119">None.</span></span>
  

