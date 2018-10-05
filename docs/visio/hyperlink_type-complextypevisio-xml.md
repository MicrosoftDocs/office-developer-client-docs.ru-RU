---
title: Hyperlink_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48c31987-bb85-e49a-c337-740fa507a02d
ms.openlocfilehash: 6c966447c13d90b05918138aeeafb11133e7bb5e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392034"
---
# <a name="hyperlinktype-complextype-visio-xml"></a><span data-ttu-id="7ea2d-102">Hyperlink_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7ea2d-102">Hyperlink_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7ea2d-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7ea2d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7ea2d-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7ea2d-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7ea2d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7ea2d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7ea2d-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7ea2d-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7ea2d-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7ea2d-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7ea2d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7ea2d-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7ea2d-110">Elements and attributes</span></span>

<span data-ttu-id="7ea2d-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7ea2d-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7ea2d-112">Child elements</span></span>

|<span data-ttu-id="7ea2d-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-113">**Element**</span></span>|<span data-ttu-id="7ea2d-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-114">**Type**</span></span>|<span data-ttu-id="7ea2d-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7ea2d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7ea2d-116">Строка</span><span class="sxs-lookup"><span data-stu-id="7ea2d-116">Row</span></span>](row-element-hyperlink-sectionvisio-xml.md) <br/> |[<span data-ttu-id="7ea2d-117">HyperlinkRow_Type</span><span class="sxs-lookup"><span data-stu-id="7ea2d-117">HyperlinkRow_Type</span></span>](hyperlinkrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7ea2d-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7ea2d-118">Attributes</span></span>

<span data-ttu-id="7ea2d-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="7ea2d-119">None.</span></span>
  

