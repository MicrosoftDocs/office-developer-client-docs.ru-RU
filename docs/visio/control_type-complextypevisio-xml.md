---
title: Control_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eba241a-e64d-6bac-6d8e-a049e4febe96
ms.openlocfilehash: 8e5cb58e6964f2bb6db530e9ff01781520d06539
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538706"
---
# <a name="control_type-complextype-visio-xml"></a><span data-ttu-id="a45ff-102">Control_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a45ff-102">Control_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="a45ff-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="a45ff-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a45ff-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="a45ff-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="a45ff-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="a45ff-105">**Schema file**</span></span> <br/> |<span data-ttu-id="a45ff-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="a45ff-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="a45ff-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="a45ff-107">**Extension base**</span></span> <br/> |<span data-ttu-id="a45ff-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="a45ff-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a45ff-109">Определение</span><span class="sxs-lookup"><span data-stu-id="a45ff-109">Definition</span></span>

```XML
          <xs:complexType name="Control_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ControlRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a45ff-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="a45ff-110">Elements and attributes</span></span>

<span data-ttu-id="a45ff-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="a45ff-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="a45ff-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a45ff-112">Child elements</span></span>

|<span data-ttu-id="a45ff-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="a45ff-113">**Element**</span></span>|<span data-ttu-id="a45ff-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="a45ff-114">**Type**</span></span>|<span data-ttu-id="a45ff-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a45ff-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a45ff-116">Row</span><span class="sxs-lookup"><span data-stu-id="a45ff-116">Row</span></span>](row-element-controls-sectionvisio-xml.md) <br/> |[<span data-ttu-id="a45ff-117">ControlRow_Type</span><span class="sxs-lookup"><span data-stu-id="a45ff-117">ControlRow_Type</span></span>](controlrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="a45ff-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a45ff-118">Attributes</span></span>

<span data-ttu-id="a45ff-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="a45ff-119">None.</span></span>
  

