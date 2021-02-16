---
title: LineGradientRow_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: 9c39ddd971f3089bb8b87026616c455e6a0524eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541143"
---
# <a name="linegradientrow_type-complextype-visio-xml"></a><span data-ttu-id="e13a4-102">LineGradientRow_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e13a4-102">LineGradientRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e13a4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e13a4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e13a4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e13a4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e13a4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e13a4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e13a4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e13a4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e13a4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="e13a4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e13a4-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="e13a4-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e13a4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e13a4-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="e13a4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e13a4-110">Elements and attributes</span></span>

<span data-ttu-id="e13a4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e13a4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e13a4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e13a4-112">Child elements</span></span>

|<span data-ttu-id="e13a4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e13a4-113">**Element**</span></span>|<span data-ttu-id="e13a4-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e13a4-114">**Type**</span></span>|<span data-ttu-id="e13a4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e13a4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e13a4-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e13a4-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e13a4-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e13a4-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e13a4-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e13a4-118">Attributes</span></span>

<span data-ttu-id="e13a4-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="e13a4-119">None.</span></span>
  

