---
title: Элемент Комментлист (Комментс_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Задает комментарии в документе.
ms.openlocfilehash: 424eb10ab356fc2b7f07a1fae27a8e2715e3f2fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359432"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="02d13-103">Элемент Комментлист (Комментс_типе complexType) (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="02d13-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="02d13-104">Задает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="02d13-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="02d13-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="02d13-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="02d13-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="02d13-106">**Element type**</span></span> <br/> |[<span data-ttu-id="02d13-107">Комментлист_типе</span><span class="sxs-lookup"><span data-stu-id="02d13-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="02d13-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="02d13-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="02d13-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="02d13-109">**Schema file**</span></span> <br/> |<span data-ttu-id="02d13-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="02d13-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="02d13-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="02d13-111">**Document parts**</span></span> <br/> |<span data-ttu-id="02d13-112">Comments. XML</span><span class="sxs-lookup"><span data-stu-id="02d13-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="02d13-113">Определение</span><span class="sxs-lookup"><span data-stu-id="02d13-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="02d13-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="02d13-114">Elements and attributes</span></span>

<span data-ttu-id="02d13-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="02d13-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="02d13-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="02d13-116">Parent elements</span></span>

|<span data-ttu-id="02d13-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="02d13-117">**Element**</span></span>|<span data-ttu-id="02d13-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="02d13-118">**Type**</span></span>|<span data-ttu-id="02d13-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02d13-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02d13-120">Comments</span><span class="sxs-lookup"><span data-stu-id="02d13-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02d13-121">Комментс_типе</span><span class="sxs-lookup"><span data-stu-id="02d13-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02d13-122">Задает свойства, используемые для идентификации авторов и комментариев в документе.</span><span class="sxs-lookup"><span data-stu-id="02d13-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="02d13-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="02d13-123">Child elements</span></span>

|<span data-ttu-id="02d13-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="02d13-124">**Element**</span></span>|<span data-ttu-id="02d13-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="02d13-125">**Type**</span></span>|<span data-ttu-id="02d13-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="02d13-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="02d13-127">Комментентри</span><span class="sxs-lookup"><span data-stu-id="02d13-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="02d13-128">Комментентри_типе</span><span class="sxs-lookup"><span data-stu-id="02d13-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="02d13-129">Задает свойства, используемые для идентификации комментария в документе.</span><span class="sxs-lookup"><span data-stu-id="02d13-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="02d13-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="02d13-130">Attributes</span></span>

<span data-ttu-id="02d13-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="02d13-131">None.</span></span>
  

