---
title: Comments_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: cce19353343190225efedec7f0a5c7bc0f026705
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542018"
---
# <a name="comments_type-complextype-visio-xml"></a><span data-ttu-id="fe9c9-102">Comments_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fe9c9-102">Comments_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="fe9c9-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="fe9c9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fe9c9-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fe9c9-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fe9c9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fe9c9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fe9c9-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fe9c9-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="fe9c9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fe9c9-109">Определение</span><span class="sxs-lookup"><span data-stu-id="fe9c9-109">Definition</span></span>

```XML
          <xs:complexType name="Comments_Type">
          
          <xs:sequence>
    <xs:element name="AuthorList"  type="AuthorList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="CommentList"  type="CommentList_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ShowCommentTags"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fe9c9-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fe9c9-110">Elements and attributes</span></span>

<span data-ttu-id="fe9c9-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="fe9c9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fe9c9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fe9c9-112">Child elements</span></span>

|<span data-ttu-id="fe9c9-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-113">**Element**</span></span>|<span data-ttu-id="fe9c9-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-114">**Type**</span></span>|<span data-ttu-id="fe9c9-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fe9c9-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="fe9c9-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fe9c9-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="fe9c9-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="fe9c9-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="fe9c9-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fe9c9-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="fe9c9-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fe9c9-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fe9c9-120">Attributes</span></span>

|<span data-ttu-id="fe9c9-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-121">**Attribute**</span></span>|<span data-ttu-id="fe9c9-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-122">**Type**</span></span>|<span data-ttu-id="fe9c9-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-123">**Required**</span></span>|<span data-ttu-id="fe9c9-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-124">**Description**</span></span>|<span data-ttu-id="fe9c9-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="fe9c9-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fe9c9-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="fe9c9-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="fe9c9-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="fe9c9-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="fe9c9-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="fe9c9-128">optional</span></span>  <br/> ||<span data-ttu-id="fe9c9-129">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="fe9c9-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

