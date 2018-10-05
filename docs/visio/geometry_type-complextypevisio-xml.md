---
title: Geometry_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 115a1499-ae55-f85c-676c-e78f478c4703
ms.openlocfilehash: 76627f406e8a829a77658cd486b586d8eebd19b7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399335"
---
# <a name="geometrytype-complextype-visio-xml"></a><span data-ttu-id="be427-102">Geometry_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="be427-102">Geometry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="be427-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="be427-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="be427-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="be427-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="be427-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="be427-105">**Schema file**</span></span> <br/> |<span data-ttu-id="be427-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="be427-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="be427-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="be427-107">**Extension base**</span></span> <br/> |<span data-ttu-id="be427-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="be427-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="be427-109">Определение</span><span class="sxs-lookup"><span data-stu-id="be427-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="be427-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="be427-110">Elements and attributes</span></span>

<span data-ttu-id="be427-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="be427-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="be427-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="be427-112">Child elements</span></span>

|<span data-ttu-id="be427-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="be427-113">**Element**</span></span>|<span data-ttu-id="be427-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="be427-114">**Type**</span></span>|<span data-ttu-id="be427-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="be427-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="be427-116">Cell</span><span class="sxs-lookup"><span data-stu-id="be427-116">Cell</span></span>](cell-element-geometry-sectionvisio-xml.md) <br/> |[<span data-ttu-id="be427-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="be427-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="be427-118">Строка</span><span class="sxs-lookup"><span data-stu-id="be427-118">Row</span></span>](row-element-geometry-sectionvisio-xml.md) <br/> |<span data-ttu-id="be427-119">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="be427-119">GeometryRow_Type</span></span>  <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="be427-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="be427-120">Attributes</span></span>

<span data-ttu-id="be427-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="be427-121">None.</span></span>
  

