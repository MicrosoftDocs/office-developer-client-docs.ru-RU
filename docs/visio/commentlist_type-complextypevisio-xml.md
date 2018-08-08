---
title: CommentList_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 640ba8825ffdfaa92c7a7ce43fb6bfb92e19ce12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813415"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="d23aa-102">CommentList_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="d23aa-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d23aa-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="d23aa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d23aa-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="d23aa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d23aa-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="d23aa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d23aa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d23aa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d23aa-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="d23aa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d23aa-108">Нет</span><span class="sxs-lookup"><span data-stu-id="d23aa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d23aa-109">Определение</span><span class="sxs-lookup"><span data-stu-id="d23aa-109">Definition</span></span>

```XML
          <xs:complexType name="CommentList_Type">
          
          <xs:sequence>
    <xs:element name="CommentEntry"  type="CommentEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d23aa-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="d23aa-110">Elements and attributes</span></span>

<span data-ttu-id="d23aa-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="d23aa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d23aa-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d23aa-112">Child elements</span></span>

|<span data-ttu-id="d23aa-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="d23aa-113">**Element**</span></span>|<span data-ttu-id="d23aa-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="d23aa-114">**Type**</span></span>|<span data-ttu-id="d23aa-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d23aa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d23aa-116">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="d23aa-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d23aa-117">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="d23aa-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d23aa-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d23aa-118">Attributes</span></span>

<span data-ttu-id="d23aa-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="d23aa-119">None.</span></span>
  

