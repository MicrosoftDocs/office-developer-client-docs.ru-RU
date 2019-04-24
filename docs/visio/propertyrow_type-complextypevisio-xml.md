---
title: Пропертиров_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 813d6dee-b113-c0c9-3f53-c5bfd05b92f2
ms.openlocfilehash: fc59e95c8bb95932dd181b40a2e60dc6a3dac485
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326847"
---
# <a name="propertyrowtype-complextype-visio-xml"></a><span data-ttu-id="2b82e-102">Пропертиров_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="2b82e-102">PropertyRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2b82e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2b82e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b82e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2b82e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2b82e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2b82e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2b82e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2b82e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2b82e-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="2b82e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2b82e-108">Намедров_типе</span><span class="sxs-lookup"><span data-stu-id="2b82e-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b82e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2b82e-109">Definition</span></span>

```XML
          <xs:complexType name="PropertyRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="2b82e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2b82e-110">Elements and attributes</span></span>

<span data-ttu-id="2b82e-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2b82e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2b82e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2b82e-112">Child elements</span></span>

|<span data-ttu-id="2b82e-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2b82e-113">**Element**</span></span>|<span data-ttu-id="2b82e-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2b82e-114">**Type**</span></span>|<span data-ttu-id="2b82e-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b82e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b82e-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2b82e-116">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="2b82e-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="2b82e-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2b82e-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2b82e-118">Attributes</span></span>

<span data-ttu-id="2b82e-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="2b82e-119">None.</span></span>
  

