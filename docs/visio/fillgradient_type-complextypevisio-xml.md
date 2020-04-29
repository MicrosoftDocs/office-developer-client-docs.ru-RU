---
title: FillGradient_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82545cdc-890d-1b2f-9c8f-4740f32d0ed7
ms.openlocfilehash: 83e8eef809f566bb2a69e5b2da1d1c5d932ce54c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539644"
---
# <a name="fillgradient_type-complextype-visio-xml"></a><span data-ttu-id="0a7de-102">FillGradient_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="0a7de-102">FillGradient_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0a7de-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0a7de-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a7de-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0a7de-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0a7de-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0a7de-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0a7de-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0a7de-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0a7de-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0a7de-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0a7de-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0a7de-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0a7de-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0a7de-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradient_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="FillGradientRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0a7de-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0a7de-110">Elements and attributes</span></span>

<span data-ttu-id="0a7de-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0a7de-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0a7de-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0a7de-112">Child elements</span></span>

|<span data-ttu-id="0a7de-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0a7de-113">**Element**</span></span>|<span data-ttu-id="0a7de-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0a7de-114">**Type**</span></span>|<span data-ttu-id="0a7de-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0a7de-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0a7de-116">Row</span><span class="sxs-lookup"><span data-stu-id="0a7de-116">Row</span></span>](row-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0a7de-117">FillGradientRow_Type</span><span class="sxs-lookup"><span data-stu-id="0a7de-117">FillGradientRow_Type</span></span>](fillgradientrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0a7de-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0a7de-118">Attributes</span></span>

<span data-ttu-id="0a7de-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="0a7de-119">None.</span></span>
  

