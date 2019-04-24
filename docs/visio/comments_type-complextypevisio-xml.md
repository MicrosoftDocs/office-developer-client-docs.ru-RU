---
title: Комментс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: b2d40b1c8368945cfa27aad0e1d567beea694c28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359411"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="bbaa9-102">Комментс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="bbaa9-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="bbaa9-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="bbaa9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bbaa9-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bbaa9-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bbaa9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bbaa9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bbaa9-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bbaa9-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="bbaa9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bbaa9-109">Определение</span><span class="sxs-lookup"><span data-stu-id="bbaa9-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bbaa9-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="bbaa9-110">Elements and attributes</span></span>

<span data-ttu-id="bbaa9-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="bbaa9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bbaa9-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bbaa9-112">Child elements</span></span>

|<span data-ttu-id="bbaa9-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-113">**Element**</span></span>|<span data-ttu-id="bbaa9-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-114">**Type**</span></span>|<span data-ttu-id="bbaa9-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bbaa9-116">Аусорлист</span><span class="sxs-lookup"><span data-stu-id="bbaa9-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bbaa9-117">Аусорлист_типе</span><span class="sxs-lookup"><span data-stu-id="bbaa9-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="bbaa9-118">Комментлист</span><span class="sxs-lookup"><span data-stu-id="bbaa9-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bbaa9-119">Комментлист_типе</span><span class="sxs-lookup"><span data-stu-id="bbaa9-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="bbaa9-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="bbaa9-120">Attributes</span></span>

|<span data-ttu-id="bbaa9-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-121">**Attribute**</span></span>|<span data-ttu-id="bbaa9-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-122">**Type**</span></span>|<span data-ttu-id="bbaa9-123">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-123">**Required**</span></span>|<span data-ttu-id="bbaa9-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-124">**Description**</span></span>|<span data-ttu-id="bbaa9-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="bbaa9-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bbaa9-126">Шовкомменттагс</span><span class="sxs-lookup"><span data-stu-id="bbaa9-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="bbaa9-127">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="bbaa9-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="bbaa9-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="bbaa9-128">optional</span></span>  <br/> ||<span data-ttu-id="bbaa9-129">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="bbaa9-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

