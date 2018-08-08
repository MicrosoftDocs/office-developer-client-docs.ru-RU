---
title: Элемент CommentList (Comments_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 49fee70d-6556-887b-003f-4f56916d541d
description: Указывает комментарии в документе.
ms.openlocfilehash: 5773b4553185fbc99718be495c48a478ae72000c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813425"
---
# <a name="commentlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="df209-103">Элемент CommentList (Comments_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="df209-103">CommentList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="df209-104">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="df209-104">Specifies the comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df209-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="df209-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df209-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="df209-106">**Element type**</span></span> <br/> |[<span data-ttu-id="df209-107">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="df209-107">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="df209-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="df209-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="df209-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="df209-109">**Schema file**</span></span> <br/> |<span data-ttu-id="df209-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="df209-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="df209-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="df209-111">**Document parts**</span></span> <br/> |<span data-ttu-id="df209-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="df209-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="df209-113">Определение</span><span class="sxs-lookup"><span data-stu-id="df209-113">Definition</span></span>

```XML
< xs:element name="CommentList" type="CommentList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="df209-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="df209-114">Elements and attributes</span></span>

<span data-ttu-id="df209-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="df209-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="df209-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="df209-116">Parent elements</span></span>

|<span data-ttu-id="df209-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="df209-117">**Element**</span></span>|<span data-ttu-id="df209-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="df209-118">**Type**</span></span>|<span data-ttu-id="df209-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df209-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df209-120">�����������</span><span class="sxs-lookup"><span data-stu-id="df209-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="df209-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="df209-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df209-122">Задает свойства, используемые для идентификации авторов и комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="df209-122">Specifies properties used to identify the authors and comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="df209-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="df209-123">Child elements</span></span>

|<span data-ttu-id="df209-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="df209-124">**Element**</span></span>|<span data-ttu-id="df209-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="df209-125">**Type**</span></span>|<span data-ttu-id="df209-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df209-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df209-127">CommentEntry</span><span class="sxs-lookup"><span data-stu-id="df209-127">CommentEntry</span></span>](commententry-element-commentlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="df209-128">CommentEntry_Type</span><span class="sxs-lookup"><span data-stu-id="df209-128">CommentEntry_Type</span></span>](commententry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="df209-129">Задает свойства, используемые для идентификации комментария в документ.</span><span class="sxs-lookup"><span data-stu-id="df209-129">Specifies properties used to identify a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="df209-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="df209-130">Attributes</span></span>

<span data-ttu-id="df209-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="df209-131">None.</span></span>
  

