---
title: Жеометри_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 1b16a32462f997ab80b0b6ef64df8eb202740c47
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542291"
---
# <a name="geometrytype-complextype-visio-xml"></a><span data-ttu-id="1bb89-102">Жеометри_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="1bb89-102">Geometry_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1bb89-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1bb89-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1bb89-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1bb89-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1bb89-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1bb89-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1bb89-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1bb89-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1bb89-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1bb89-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1bb89-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="1bb89-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1bb89-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1bb89-109">Definition</span></span>

```XML
          <xs:complexType name="Geometry_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:choice minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Row"  type="GeometryRow_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:choice>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1bb89-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1bb89-110">Elements and attributes</span></span>

<span data-ttu-id="1bb89-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1bb89-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1bb89-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1bb89-112">Child elements</span></span>

|<span data-ttu-id="1bb89-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1bb89-113">**Element**</span></span>|<span data-ttu-id="1bb89-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1bb89-114">**Type**</span></span>|<span data-ttu-id="1bb89-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1bb89-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1bb89-116">Cell</span><span class="sxs-lookup"><span data-stu-id="1bb89-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1bb89-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="1bb89-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="1bb89-118">Row</span><span class="sxs-lookup"><span data-stu-id="1bb89-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="1bb89-119">Жеометриров_типе</span><span class="sxs-lookup"><span data-stu-id="1bb89-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1bb89-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1bb89-120">Attributes</span></span>

<span data-ttu-id="1bb89-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="1bb89-121">None.</span></span>
  

