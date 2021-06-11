---
title: Hyperlink_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: ce9a1f5b9a6e402ec157d641f81a82c6df4b92e1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541556"
---
# <a name="hyperlink_type-complextype-visio-xml"></a><span data-ttu-id="69ff4-102">Hyperlink_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="69ff4-102">Hyperlink_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="69ff4-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="69ff4-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69ff4-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="69ff4-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="69ff4-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="69ff4-105">**Schema file**</span></span> <br/> |<span data-ttu-id="69ff4-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="69ff4-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="69ff4-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="69ff4-107">**Extension base**</span></span> <br/> |<span data-ttu-id="69ff4-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="69ff4-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69ff4-109">Определение</span><span class="sxs-lookup"><span data-stu-id="69ff4-109">Definition</span></span>

```XML
          <xs:complexType name="Hyperlink_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="HyperlinkRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="69ff4-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="69ff4-110">Elements and attributes</span></span>

<span data-ttu-id="69ff4-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="69ff4-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="69ff4-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="69ff4-112">Child elements</span></span>

|<span data-ttu-id="69ff4-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="69ff4-113">**Element**</span></span>|<span data-ttu-id="69ff4-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="69ff4-114">**Type**</span></span>|<span data-ttu-id="69ff4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="69ff4-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="69ff4-116">Row</span><span class="sxs-lookup"><span data-stu-id="69ff4-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="69ff4-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="69ff4-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="69ff4-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="69ff4-118">Attributes</span></span>

<span data-ttu-id="69ff4-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="69ff4-119">None.</span></span>
  

