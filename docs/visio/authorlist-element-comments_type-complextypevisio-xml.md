---
title: Элемент AuthorList (Comments_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Задает авторов комментариев в документе.
ms.openlocfilehash: 0f31e11e52809df60b41cb67b868b15435e0eb47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813192"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="f5877-103">Элемент AuthorList (Comments_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f5877-103">AuthorList element (Comments_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f5877-104">Задает авторов комментариев в документе.</span><span class="sxs-lookup"><span data-stu-id="f5877-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f5877-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f5877-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5877-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f5877-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f5877-107">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="f5877-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f5877-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f5877-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f5877-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f5877-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f5877-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f5877-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f5877-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f5877-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f5877-112">Comments.XML</span><span class="sxs-lookup"><span data-stu-id="f5877-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f5877-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f5877-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f5877-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f5877-114">Elements and attributes</span></span>

<span data-ttu-id="f5877-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="f5877-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f5877-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f5877-116">Parent elements</span></span>

|<span data-ttu-id="f5877-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f5877-117">**Element**</span></span>|<span data-ttu-id="f5877-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f5877-118">**Type**</span></span>|<span data-ttu-id="f5877-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5877-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f5877-120">�����������</span><span class="sxs-lookup"><span data-stu-id="f5877-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5877-121">Comments_Type</span><span class="sxs-lookup"><span data-stu-id="f5877-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f5877-122">Указывает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="f5877-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f5877-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f5877-123">Child elements</span></span>

|<span data-ttu-id="f5877-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f5877-124">**Element**</span></span>|<span data-ttu-id="f5877-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f5877-125">**Type**</span></span>|<span data-ttu-id="f5877-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f5877-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f5877-127">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="f5877-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f5877-128">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="f5877-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f5877-129">Задает свойства, которые задают автора комментария в документ.</span><span class="sxs-lookup"><span data-stu-id="f5877-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f5877-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f5877-130">Attributes</span></span>

<span data-ttu-id="f5877-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="f5877-131">None.</span></span>
  

