---
title: Усерров_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: 54edb9a1396582eae87db8735c4f75bd9597f1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337074"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="f77b1-102">Усерров_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="f77b1-102">UserRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f77b1-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="f77b1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f77b1-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f77b1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f77b1-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f77b1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f77b1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f77b1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f77b1-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="f77b1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f77b1-108">Намедров_типе</span><span class="sxs-lookup"><span data-stu-id="f77b1-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f77b1-109">Определение</span><span class="sxs-lookup"><span data-stu-id="f77b1-109">Definition</span></span>

```XML
          <xs:complexType name="UserRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f77b1-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f77b1-110">Elements and attributes</span></span>

<span data-ttu-id="f77b1-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f77b1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f77b1-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f77b1-112">Child elements</span></span>

|<span data-ttu-id="f77b1-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f77b1-113">**Element**</span></span>|<span data-ttu-id="f77b1-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f77b1-114">**Type**</span></span>|<span data-ttu-id="f77b1-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f77b1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f77b1-116">Cell</span><span class="sxs-lookup"><span data-stu-id="f77b1-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="f77b1-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="f77b1-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f77b1-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f77b1-118">Attributes</span></span>

<span data-ttu-id="f77b1-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="f77b1-119">None.</span></span>
  

