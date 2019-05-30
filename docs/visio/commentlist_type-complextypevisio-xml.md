---
title: Комментлист_типе complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: 9b85a3731cfde30307084c65da1d23aa86280afd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542053"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="8dd67-102">Комментлист_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8dd67-102">CommentList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8dd67-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8dd67-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8dd67-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8dd67-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8dd67-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8dd67-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8dd67-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8dd67-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8dd67-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="8dd67-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8dd67-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8dd67-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8dd67-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8dd67-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="8dd67-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8dd67-110">Elements and attributes</span></span>

<span data-ttu-id="8dd67-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8dd67-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8dd67-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8dd67-112">Child elements</span></span>

|<span data-ttu-id="8dd67-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="8dd67-113">**Element**</span></span>|<span data-ttu-id="8dd67-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8dd67-114">**Type**</span></span>|<span data-ttu-id="8dd67-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8dd67-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="8dd67-116">Комментентри</span><span class="sxs-lookup"><span data-stu-id="8dd67-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="8dd67-117">Комментентри_типе</span><span class="sxs-lookup"><span data-stu-id="8dd67-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="8dd67-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8dd67-118">Attributes</span></span>

<span data-ttu-id="8dd67-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="8dd67-119">None.</span></span>
  

