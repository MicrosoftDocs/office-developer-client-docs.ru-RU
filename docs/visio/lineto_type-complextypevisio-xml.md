---
title: LineTo_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 15859b84-5486-bb8c-e67e-5d0baaf59ee5
ms.openlocfilehash: 2291d7967ff08cc7a7d949d7a40feb178f16b497
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392895"
---
# <a name="linetotype-complextype-visio-xml"></a><span data-ttu-id="2b2b5-102">LineTo_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="2b2b5-102">LineTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2b2b5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2b2b5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b2b5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2b2b5-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2b2b5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2b2b5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2b2b5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2b2b5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2b2b5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="2b2b5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2b2b5-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="2b2b5-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b2b5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2b2b5-109">Definition</span></span>

```XML
          <xs:complexType name="LineTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="2b2b5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2b2b5-110">Elements and attributes</span></span>

<span data-ttu-id="2b2b5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2b2b5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2b2b5-112">Child elements</span></span>

|<span data-ttu-id="2b2b5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="2b2b5-113">**Element**</span></span>|<span data-ttu-id="2b2b5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2b2b5-114">**Type**</span></span>|<span data-ttu-id="2b2b5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2b2b5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b2b5-116">Cell</span><span class="sxs-lookup"><span data-stu-id="2b2b5-116">Cell</span></span>](cell-element-lineto-rowvisio-xml.md) <br/> |[<span data-ttu-id="2b2b5-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2b2b5-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2b2b5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2b2b5-118">Attributes</span></span>

<span data-ttu-id="2b2b5-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="2b2b5-119">None.</span></span>
  

