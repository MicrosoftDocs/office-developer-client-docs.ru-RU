---
title: Pages_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: a03c5df25a28da40724178cf1c7f917ee4e723c5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400161"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="aac34-102">Pages_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="aac34-102">Pages_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="aac34-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="aac34-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aac34-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="aac34-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="aac34-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="aac34-105">**Schema file**</span></span> <br/> |<span data-ttu-id="aac34-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="aac34-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="aac34-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="aac34-107">**Extension base**</span></span> <br/> |<span data-ttu-id="aac34-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="aac34-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aac34-109">Определение</span><span class="sxs-lookup"><span data-stu-id="aac34-109">Definition</span></span>

```XML
          <xs:complexType name="Pages_Type">
          
          <xs:sequence>
    <xs:element name="Page"  type="Page_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aac34-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="aac34-110">Elements and attributes</span></span>

<span data-ttu-id="aac34-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="aac34-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="aac34-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aac34-112">Child elements</span></span>

|<span data-ttu-id="aac34-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="aac34-113">**Element**</span></span>|<span data-ttu-id="aac34-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="aac34-114">**Type**</span></span>|<span data-ttu-id="aac34-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="aac34-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aac34-116">Страница</span><span class="sxs-lookup"><span data-stu-id="aac34-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aac34-117">Page_Type</span><span class="sxs-lookup"><span data-stu-id="aac34-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="aac34-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="aac34-118">Attributes</span></span>

<span data-ttu-id="aac34-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="aac34-119">None.</span></span>
  

