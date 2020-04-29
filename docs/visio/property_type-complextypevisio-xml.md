---
title: Property_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: 1eb2d9f11a264138f5d1a325d31e17789d1c9483
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540737"
---
# <a name="property_type-complextype-visio-xml"></a><span data-ttu-id="1dc03-102">Property_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="1dc03-102">Property_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1dc03-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1dc03-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1dc03-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1dc03-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1dc03-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1dc03-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1dc03-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1dc03-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1dc03-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1dc03-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1dc03-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1dc03-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1dc03-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1dc03-109">Definition</span></span>

```XML
          <xs:complexType name="Property_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="PropertyRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1dc03-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1dc03-110">Elements and attributes</span></span>

<span data-ttu-id="1dc03-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1dc03-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1dc03-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1dc03-112">Child elements</span></span>

|<span data-ttu-id="1dc03-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1dc03-113">**Element**</span></span>|<span data-ttu-id="1dc03-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1dc03-114">**Type**</span></span>|<span data-ttu-id="1dc03-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1dc03-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1dc03-116">Row</span><span class="sxs-lookup"><span data-stu-id="1dc03-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1dc03-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="1dc03-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1dc03-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1dc03-118">Attributes</span></span>

<span data-ttu-id="1dc03-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="1dc03-119">None.</span></span>
  

