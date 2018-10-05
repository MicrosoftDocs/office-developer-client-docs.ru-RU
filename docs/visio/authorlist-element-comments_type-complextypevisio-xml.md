---
title: Элемент AuthorList (Comments_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Задает авторов комментариев в документе.
ms.openlocfilehash: af1b1889fa3736931c9abde35191cf5cb3e1bbd5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387743"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="62d40-103">Элемент AuthorList (Comments_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="62d40-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="62d40-104">Задает авторов комментариев в документе.</span><span class="sxs-lookup"><span data-stu-id="62d40-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62d40-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62d40-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62d40-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="62d40-106">**Element type**</span></span> <br/> |[<span data-ttu-id="62d40-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="62d40-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="62d40-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="62d40-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="62d40-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="62d40-109">**Schema file**</span></span> <br/> |<span data-ttu-id="62d40-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="62d40-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="62d40-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="62d40-111">**Document parts**</span></span> <br/> |<span data-ttu-id="62d40-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="62d40-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62d40-113">Определение</span><span class="sxs-lookup"><span data-stu-id="62d40-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62d40-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="62d40-114">Elements and attributes</span></span>

<span data-ttu-id="62d40-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="62d40-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="62d40-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="62d40-116">Parent elements</span></span>

|<span data-ttu-id="62d40-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="62d40-117">**Element**</span></span>|<span data-ttu-id="62d40-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="62d40-118">**Type**</span></span>|<span data-ttu-id="62d40-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62d40-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62d40-120">�����������</span><span class="sxs-lookup"><span data-stu-id="62d40-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62d40-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="62d40-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62d40-122">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="62d40-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62d40-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62d40-123">Child elements</span></span>

|<span data-ttu-id="62d40-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="62d40-124">**Element**</span></span>|<span data-ttu-id="62d40-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="62d40-125">**Type**</span></span>|<span data-ttu-id="62d40-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="62d40-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62d40-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="62d40-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62d40-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="62d40-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62d40-129">Задает свойства, которые задают автора комментария в документ.</span><span class="sxs-lookup"><span data-stu-id="62d40-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="62d40-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62d40-130">Attributes</span></span>

<span data-ttu-id="62d40-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="62d40-131">None.</span></span>
  

