---
title: RelMoveTo_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3759d7cc-061b-0c0b-c372-b7d60effbfd0
ms.openlocfilehash: 0b8c81b389244fe45b99c3fadde5c110c60d0393
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542760"
---
# <a name="relmoveto_type-complextype-visio-xml"></a><span data-ttu-id="65e1b-102">RelMoveTo_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="65e1b-102">RelMoveTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="65e1b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="65e1b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="65e1b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="65e1b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="65e1b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="65e1b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="65e1b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="65e1b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="65e1b-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="65e1b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="65e1b-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="65e1b-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="65e1b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="65e1b-109">Definition</span></span>

```XML
          <xs:complexType name="RelMoveTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="65e1b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="65e1b-110">Elements and attributes</span></span>

<span data-ttu-id="65e1b-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="65e1b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="65e1b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="65e1b-112">Child elements</span></span>

|<span data-ttu-id="65e1b-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="65e1b-113">**Element**</span></span>|<span data-ttu-id="65e1b-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="65e1b-114">**Type**</span></span>|<span data-ttu-id="65e1b-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="65e1b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="65e1b-116">Cell</span><span class="sxs-lookup"><span data-stu-id="65e1b-116">Cell</span></span>](cell-element-relmoveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="65e1b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="65e1b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="65e1b-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="65e1b-118">Attributes</span></span>

<span data-ttu-id="65e1b-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="65e1b-119">None.</span></span>
  

