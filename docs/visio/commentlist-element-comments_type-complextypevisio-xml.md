---
title: Элемент CommentList (Comments_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Указывает комментарии на рисунке.
ms.openlocfilehash: fbbc7ea668686a8f075f3f11843b2d828c257363
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539250"
---
# <a name="commentlist-element-comments_type-complextype-visio-xml"></a><span data-ttu-id="32d00-103">Элемент CommentList (Comments_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="32d00-103">CommentList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="32d00-104">Указывает комментарии на рисунке.</span><span class="sxs-lookup"><span data-stu-id="32d00-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="32d00-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="32d00-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32d00-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="32d00-106">**Element type**</span></span> <br/> |[<span data-ttu-id="32d00-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="32d00-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="32d00-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="32d00-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="32d00-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="32d00-109">**Schema file**</span></span> <br/> |<span data-ttu-id="32d00-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="32d00-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="32d00-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="32d00-111">**Document parts**</span></span> <br/> |<span data-ttu-id="32d00-112">comments.xml</span><span class="sxs-lookup"><span data-stu-id="32d00-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="32d00-113">Определение</span><span class="sxs-lookup"><span data-stu-id="32d00-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="32d00-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="32d00-114">Elements and attributes</span></span>

<span data-ttu-id="32d00-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="32d00-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="32d00-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="32d00-116">Parent elements</span></span>

|<span data-ttu-id="32d00-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="32d00-117">**Element**</span></span>|<span data-ttu-id="32d00-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="32d00-118">**Type**</span></span>|<span data-ttu-id="32d00-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32d00-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32d00-120">Comments</span><span class="sxs-lookup"><span data-stu-id="32d00-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="32d00-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="32d00-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="32d00-122">Указывает свойства, используемые для идентификации авторов и комментариев на рисунке.</span><span class="sxs-lookup"><span data-stu-id="32d00-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="32d00-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="32d00-123">Child elements</span></span>

|<span data-ttu-id="32d00-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="32d00-124">**Element**</span></span>|<span data-ttu-id="32d00-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="32d00-125">**Type**</span></span>|<span data-ttu-id="32d00-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="32d00-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32d00-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="32d00-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="32d00-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="32d00-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="32d00-129">Указывает свойства, используемые для идентификации комментария на рисунке.</span><span class="sxs-lookup"><span data-stu-id="32d00-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="32d00-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="32d00-130">Attributes</span></span>

<span data-ttu-id="32d00-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="32d00-131">None.</span></span>
  

