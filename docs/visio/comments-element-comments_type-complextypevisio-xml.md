---
title: Элемент Comments (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f72ced69-0d49-18cd-f1e6-d0b2cb39b4c0
description: Указывает свойства, используемые для идентификации авторов и комментариев в документе.
ms.openlocfilehash: 93e75e47a203ee13385085c4b5e261fd3a724d4f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539222"
---
# <a name="comments-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="ae645-103">Элемент Comments (Comments_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="ae645-103">Comments element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ae645-104">Указывает свойства, используемые для идентификации авторов и комментариев в документе.</span><span class="sxs-lookup"><span data-stu-id="ae645-104">Specifies properties used to identify the authors and comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae645-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ae645-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae645-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="ae645-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ae645-107">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="ae645-107">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ae645-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="ae645-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ae645-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="ae645-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ae645-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ae645-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ae645-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="ae645-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ae645-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="ae645-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ae645-113">Определение</span><span class="sxs-lookup"><span data-stu-id="ae645-113">Definition</span></span>

```XML
< xs:element name="Comments" type="Comments_Type" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ae645-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="ae645-114">Elements and attributes</span></span>

<span data-ttu-id="ae645-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="ae645-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ae645-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ae645-116">Parent elements</span></span>

<span data-ttu-id="ae645-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="ae645-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ae645-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ae645-118">Child elements</span></span>

|<span data-ttu-id="ae645-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ae645-119">**Element**</span></span>|<span data-ttu-id="ae645-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ae645-120">**Type**</span></span>|<span data-ttu-id="ae645-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ae645-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ae645-122">AuthorList</span><span class="sxs-lookup"><span data-stu-id="ae645-122">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae645-123">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="ae645-123">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae645-124">Указывает авторов в документе.</span><span class="sxs-lookup"><span data-stu-id="ae645-124">Specifies the authors in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="ae645-125">CommentList</span><span class="sxs-lookup"><span data-stu-id="ae645-125">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ae645-126">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="ae645-126">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ae645-127">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="ae645-127">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="ae645-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ae645-128">Attributes</span></span>

<span data-ttu-id="ae645-129">Нет.</span><span class="sxs-lookup"><span data-stu-id="ae645-129">None.</span></span>
  

