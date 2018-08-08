---
title: Элемент Comments (Comments_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Задает свойства, используемые для идентификации авторов и комментарии в документе.
ms.openlocfilehash: 77695fb32aa88cb6c2b6ac5e9bff99fa12e262bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813421"
---
# <a name="comments-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="cc039-103">Элемент Comments (Comments_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="cc039-103">Comments element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cc039-104">Задает свойства, используемые для идентификации авторов и комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="cc039-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cc039-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="cc039-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc039-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="cc039-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cc039-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="cc039-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cc039-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="cc039-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cc039-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="cc039-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cc039-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="cc039-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cc039-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="cc039-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cc039-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="cc039-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc039-113">Определение</span><span class="sxs-lookup"><span data-stu-id="cc039-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc039-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="cc039-114">Elements and attributes</span></span>

<span data-ttu-id="cc039-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="cc039-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cc039-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="cc039-116">Parent elements</span></span>

<span data-ttu-id="cc039-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="cc039-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cc039-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cc039-118">Child elements</span></span>

|<span data-ttu-id="cc039-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cc039-119">**Element**</span></span>|<span data-ttu-id="cc039-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cc039-120">**Type**</span></span>|<span data-ttu-id="cc039-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cc039-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc039-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="cc039-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc039-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="cc039-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc039-124">Задает авторы документа.</span><span class="sxs-lookup"><span data-stu-id="cc039-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="cc039-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="cc039-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc039-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="cc039-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cc039-127">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="cc039-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="cc039-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cc039-128">Attributes</span></span>

<span data-ttu-id="cc039-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="cc039-129">None.</span></span>
  

