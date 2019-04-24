---
title: Комментлист_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 76a41e59-d2cf-dd6a-0ac4-370c1aca4c01
ms.openlocfilehash: af23616556cecdbfa1157a8d4c49de1ca4b2fd88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359418"
---
# <a name="commentlisttype-complextype-visio-xml"></a><span data-ttu-id="0c9fc-102">Комментлист_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="0c9fc-102">CommentList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0c9fc-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0c9fc-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c9fc-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0c9fc-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c9fc-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0c9fc-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c9fc-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c9fc-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c9fc-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0c9fc-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c9fc-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="0c9fc-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c9fc-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0c9fc-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0c9fc-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0c9fc-110">Elements and attributes</span></span>

<span data-ttu-id="0c9fc-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0c9fc-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c9fc-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0c9fc-112">Child elements</span></span>

|<span data-ttu-id="0c9fc-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0c9fc-113">**Element**</span></span>|<span data-ttu-id="0c9fc-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0c9fc-114">**Type**</span></span>|<span data-ttu-id="0c9fc-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0c9fc-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0c9fc-116">Комментентри</span><span class="sxs-lookup"><span data-stu-id="0c9fc-116">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="0c9fc-117">Комментентри_типе</span><span class="sxs-lookup"><span data-stu-id="0c9fc-117">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0c9fc-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0c9fc-118">Attributes</span></span>

<span data-ttu-id="0c9fc-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="0c9fc-119">None.</span></span>
  

