---
title: ScratchRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 35ed6fc0-d737-a931-fddb-7bbb770c8d37
ms.openlocfilehash: 74f106f34596ca4ff2c200e0127155f4df54da28
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391467"
---
# <a name="scratchrowtype-complextype-visio-xml"></a><span data-ttu-id="72937-102">ScratchRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="72937-102">ScratchRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="72937-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="72937-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="72937-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="72937-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="72937-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="72937-105">**Schema file**</span></span> <br/> |<span data-ttu-id="72937-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="72937-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="72937-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="72937-107">**Extension base**</span></span> <br/> |<span data-ttu-id="72937-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="72937-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="72937-109">Определение</span><span class="sxs-lookup"><span data-stu-id="72937-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="72937-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="72937-110">Elements and attributes</span></span>

<span data-ttu-id="72937-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="72937-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="72937-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="72937-112">Child elements</span></span>

|<span data-ttu-id="72937-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="72937-113">**Element**</span></span>|<span data-ttu-id="72937-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="72937-114">**Type**</span></span>|<span data-ttu-id="72937-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="72937-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="72937-116">Cell</span><span class="sxs-lookup"><span data-stu-id="72937-116">Cell</span></span>](cell-element-scratch-sectionvisio-xml.md) <br/> |[<span data-ttu-id="72937-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="72937-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="72937-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="72937-118">Attributes</span></span>

<span data-ttu-id="72937-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="72937-119">None.</span></span>
  

