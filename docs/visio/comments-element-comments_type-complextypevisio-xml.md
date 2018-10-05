---
title: Элемент Comments (Comments_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Задает свойства, используемые для идентификации авторов и комментарии в документе.
ms.openlocfilehash: d82125cc5d795f0cb4455a5c10be1abf001e1198
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389647"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="c81af-103">Элемент Comments (Comments_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="c81af-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="c81af-104">Задает свойства, используемые для идентификации авторов и комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="c81af-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c81af-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c81af-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c81af-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="c81af-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c81af-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="c81af-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c81af-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="c81af-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c81af-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="c81af-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c81af-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c81af-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c81af-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="c81af-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c81af-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="c81af-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c81af-113">Определение</span><span class="sxs-lookup"><span data-stu-id="c81af-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c81af-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="c81af-114">Elements and attributes</span></span>

<span data-ttu-id="c81af-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="c81af-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c81af-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c81af-116">Parent elements</span></span>

<span data-ttu-id="c81af-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="c81af-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c81af-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c81af-118">Child elements</span></span>

|<span data-ttu-id="c81af-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c81af-119">**Element**</span></span>|<span data-ttu-id="c81af-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="c81af-120">**Type**</span></span>|<span data-ttu-id="c81af-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c81af-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c81af-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="c81af-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c81af-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="c81af-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c81af-124">Задает авторы документа.</span><span class="sxs-lookup"><span data-stu-id="c81af-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="c81af-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="c81af-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c81af-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="c81af-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c81af-127">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="c81af-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c81af-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c81af-128">Attributes</span></span>

<span data-ttu-id="c81af-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="c81af-129">None.</span></span>
  

