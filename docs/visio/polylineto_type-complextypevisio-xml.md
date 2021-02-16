---
title: PolylineTo_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e0b87cc0-397d-7640-34ea-2a725d8f0999
ms.openlocfilehash: e1c6c6912105ba593467cd4bb4e4cb0ded460233
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540100"
---
# <a name="polylineto_type-complextype-visio-xml"></a><span data-ttu-id="8b54c-102">PolylineTo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="8b54c-102">PolylineTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8b54c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8b54c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8b54c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8b54c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8b54c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8b54c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8b54c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8b54c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8b54c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="8b54c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8b54c-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="8b54c-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8b54c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8b54c-109">Definition</span></span>

```XML
          <xs:complexType name="PolylineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="8b54c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8b54c-110">Elements and attributes</span></span>

<span data-ttu-id="8b54c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8b54c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8b54c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8b54c-112">Child elements</span></span>

|<span data-ttu-id="8b54c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8b54c-113">**Element**</span></span>|<span data-ttu-id="8b54c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8b54c-114">**Type**</span></span>|<span data-ttu-id="8b54c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8b54c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8b54c-116">Cell</span><span class="sxs-lookup"><span data-stu-id="8b54c-116">Cell</span></span>](cell-element-polylineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="8b54c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="8b54c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8b54c-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8b54c-118">Attributes</span></span>

<span data-ttu-id="8b54c-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="8b54c-119">None.</span></span>
  

