---
title: Коннектионров_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 14a92d20-78fb-0043-7360-7dfda52fb9c7
ms.openlocfilehash: ad8f4f877153b871b897be7da5d5e09a5ff070fb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538734"
---
# <a name="connectionrowtype-complextype-visio-xml"></a><span data-ttu-id="6e156-102">Коннектионров_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="6e156-102">ConnectionRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6e156-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="6e156-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6e156-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6e156-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6e156-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6e156-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6e156-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6e156-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6e156-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="6e156-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6e156-108">Намединдекседров_типе</span><span class="sxs-lookup"><span data-stu-id="6e156-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6e156-109">Определение</span><span class="sxs-lookup"><span data-stu-id="6e156-109">Definition</span></span>

```XML
          <xs:complexType name="ConnectionRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedIndexedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6e156-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e156-110">Elements and attributes</span></span>

<span data-ttu-id="6e156-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6e156-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6e156-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6e156-112">Child elements</span></span>

|<span data-ttu-id="6e156-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6e156-113">**Element**</span></span>|<span data-ttu-id="6e156-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6e156-114">**Type**</span></span>|<span data-ttu-id="6e156-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6e156-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6e156-116">Cell</span><span class="sxs-lookup"><span data-stu-id="6e156-116">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="6e156-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="6e156-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6e156-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6e156-118">Attributes</span></span>

<span data-ttu-id="6e156-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="6e156-119">None.</span></span>
  

