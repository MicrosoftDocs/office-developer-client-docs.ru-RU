---
title: NURBSTo_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7ae8a1d-5bb7-a92f-79d6-5a358d879c32
ms.openlocfilehash: 47c8c552fb50c29ecf2f89325c1a818e61d60d1f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391761"
---
# <a name="nurbstotype-complextype-visio-xml"></a><span data-ttu-id="53e63-102">NURBSTo_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="53e63-102">NURBSTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="53e63-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="53e63-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="53e63-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="53e63-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="53e63-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="53e63-105">**Schema file**</span></span> <br/> |<span data-ttu-id="53e63-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="53e63-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="53e63-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="53e63-107">**Extension base**</span></span> <br/> |<span data-ttu-id="53e63-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="53e63-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="53e63-109">Определение</span><span class="sxs-lookup"><span data-stu-id="53e63-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="53e63-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="53e63-110">Elements and attributes</span></span>

<span data-ttu-id="53e63-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="53e63-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="53e63-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="53e63-112">Child elements</span></span>

|<span data-ttu-id="53e63-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="53e63-113">**Element**</span></span>|<span data-ttu-id="53e63-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="53e63-114">**Type**</span></span>|<span data-ttu-id="53e63-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="53e63-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="53e63-116">Cell</span><span class="sxs-lookup"><span data-stu-id="53e63-116">Cell</span></span>](cell-element-nurbsto-rowvisio-xml.md) <br/> |[<span data-ttu-id="53e63-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="53e63-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="53e63-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="53e63-118">Attributes</span></span>

<span data-ttu-id="53e63-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="53e63-119">None.</span></span>
  

