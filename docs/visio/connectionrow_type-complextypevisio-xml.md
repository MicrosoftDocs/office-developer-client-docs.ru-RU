---
title: ConnectionRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 14a92d20-78fb-0043-7360-7dfda52fb9c7
ms.openlocfilehash: a71c9ac7abe11214ce23460ca48163745874c214
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393756"
---
# <a name="connectionrowtype-complextype-visio-xml"></a><span data-ttu-id="4ef8f-102">ConnectionRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="4ef8f-102">ConnectionRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4ef8f-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="4ef8f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ef8f-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4ef8f-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4ef8f-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4ef8f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4ef8f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4ef8f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4ef8f-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="4ef8f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4ef8f-108">NamedIndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="4ef8f-108">NamedIndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ef8f-109">Определение</span><span class="sxs-lookup"><span data-stu-id="4ef8f-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="4ef8f-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4ef8f-110">Elements and attributes</span></span>

<span data-ttu-id="4ef8f-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4ef8f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4ef8f-112">Child elements</span></span>

|<span data-ttu-id="4ef8f-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4ef8f-113">**Element**</span></span>|<span data-ttu-id="4ef8f-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4ef8f-114">**Type**</span></span>|<span data-ttu-id="4ef8f-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4ef8f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4ef8f-116">Cell</span><span class="sxs-lookup"><span data-stu-id="4ef8f-116">Cell</span></span>](cell-element-connection-rowvisio-xml.md) <br/> |[<span data-ttu-id="4ef8f-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4ef8f-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4ef8f-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4ef8f-118">Attributes</span></span>

<span data-ttu-id="4ef8f-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-119">None.</span></span>
  

