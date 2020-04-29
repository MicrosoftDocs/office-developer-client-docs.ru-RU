---
title: NURBSTo_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7ae8a1d-5bb7-a92f-79d6-5a358d879c32
ms.openlocfilehash: 090df2487eb6fabfba4b3917c7d938fe4f841147
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540919"
---
# <a name="nurbsto_type-complextype-visio-xml"></a><span data-ttu-id="d8017-102">NURBSTo_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="d8017-102">NURBSTo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="d8017-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d8017-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8017-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d8017-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8017-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d8017-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8017-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8017-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8017-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="d8017-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8017-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="d8017-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8017-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d8017-109">Definition</span></span>

```XML
          <xs:complexType name="NURBSTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="d8017-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d8017-110">Elements and attributes</span></span>

<span data-ttu-id="d8017-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="d8017-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8017-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d8017-112">Child elements</span></span>

|<span data-ttu-id="d8017-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d8017-113">**Element**</span></span>|<span data-ttu-id="d8017-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d8017-114">**Type**</span></span>|<span data-ttu-id="d8017-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d8017-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8017-116">Cell</span><span class="sxs-lookup"><span data-stu-id="d8017-116">Cell</span></span>](cell-element-nurbsto-rowvisio-xml.md) <br/> |[<span data-ttu-id="d8017-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="d8017-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d8017-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d8017-118">Attributes</span></span>

<span data-ttu-id="d8017-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="d8017-119">None.</span></span>
  

