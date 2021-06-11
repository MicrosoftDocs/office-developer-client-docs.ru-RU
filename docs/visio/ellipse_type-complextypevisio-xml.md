---
title: Ellipse_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67dc78e-6639-e32f-4909-945001659d30
ms.openlocfilehash: d5e73eeb0dd4b4ead485b1bcd99585a2cd766c51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539914"
---
# <a name="ellipse_type-complextype-visio-xml"></a><span data-ttu-id="2aae5-102">Ellipse_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="2aae5-102">Ellipse_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="2aae5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2aae5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2aae5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2aae5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2aae5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2aae5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2aae5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2aae5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2aae5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="2aae5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2aae5-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="2aae5-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2aae5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2aae5-109">Definition</span></span>

```XML
          <xs:complexType name="Ellipse_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2aae5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2aae5-110">Elements and attributes</span></span>

<span data-ttu-id="2aae5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2aae5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2aae5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2aae5-112">Child elements</span></span>

|<span data-ttu-id="2aae5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2aae5-113">**Element**</span></span>|<span data-ttu-id="2aae5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2aae5-114">**Type**</span></span>|<span data-ttu-id="2aae5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2aae5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2aae5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2aae5-116">Cell</span></span>](cell-element-ellipse-rowvisio-xml.md) <br/> |[<span data-ttu-id="2aae5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2aae5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2aae5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2aae5-118">Attributes</span></span>

<span data-ttu-id="2aae5-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="2aae5-119">None.</span></span>
  

