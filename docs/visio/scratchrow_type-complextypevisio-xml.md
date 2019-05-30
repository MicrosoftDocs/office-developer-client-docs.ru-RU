---
title: Скратчров_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: c2fec0107bba66809536a1cf8bf43fb616a9ef81
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539028"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="b7dcd-102">Скратчров_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="b7dcd-102">ScratchRow_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="b7dcd-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b7dcd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7dcd-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b7dcd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b7dcd-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b7dcd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b7dcd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b7dcd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b7dcd-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b7dcd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b7dcd-108">Индекседров_типе</span><span class="sxs-lookup"><span data-stu-id="b7dcd-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7dcd-109">Определение</span><span class="sxs-lookup"><span data-stu-id="b7dcd-109">Definition</span></span>

```XML
          <xs:complexType name="ScratchRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="b7dcd-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7dcd-110">Elements and attributes</span></span>

<span data-ttu-id="b7dcd-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b7dcd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b7dcd-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7dcd-112">Child elements</span></span>

|<span data-ttu-id="b7dcd-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b7dcd-113">**Element**</span></span>|<span data-ttu-id="b7dcd-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7dcd-114">**Type**</span></span>|<span data-ttu-id="b7dcd-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7dcd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7dcd-116">Cell</span><span class="sxs-lookup"><span data-stu-id="b7dcd-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="b7dcd-117">Целл_типе</span><span class="sxs-lookup"><span data-stu-id="b7dcd-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b7dcd-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7dcd-118">Attributes</span></span>

<span data-ttu-id="b7dcd-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="b7dcd-119">None.</span></span>
  

