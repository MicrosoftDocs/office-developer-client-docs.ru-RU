---
title: Пажес_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13508e59-e29a-ca70-676b-c5b23ca8e3d0
ms.openlocfilehash: 4615f365448b96981088352f9f2d6e98255e4101
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538944"
---
# <a name="pagestype-complextype-visio-xml"></a><span data-ttu-id="770d5-102">Пажес_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="770d5-102">Pages_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="770d5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="770d5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="770d5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="770d5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="770d5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="770d5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="770d5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="770d5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="770d5-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="770d5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="770d5-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="770d5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="770d5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="770d5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="770d5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="770d5-110">Elements and attributes</span></span>

<span data-ttu-id="770d5-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="770d5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="770d5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="770d5-112">Child elements</span></span>

|<span data-ttu-id="770d5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="770d5-113">**Element**</span></span>|<span data-ttu-id="770d5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="770d5-114">**Type**</span></span>|<span data-ttu-id="770d5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="770d5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="770d5-116">Page</span><span class="sxs-lookup"><span data-stu-id="770d5-116">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="770d5-117">Паже_типе</span><span class="sxs-lookup"><span data-stu-id="770d5-117">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="770d5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="770d5-118">Attributes</span></span>

<span data-ttu-id="770d5-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="770d5-119">None.</span></span>
  

