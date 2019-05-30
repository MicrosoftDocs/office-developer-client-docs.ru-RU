---
title: Элемент Аусорлист (Комментс_типе complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Указывает авторов комментариев в документе.
ms.openlocfilehash: c6e94c985d2728ba704a9159ec9bf3c4a2a72e95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537859"
---
# <a name="authorlist-element-commentstype-complextype-visio-xml"></a><span data-ttu-id="31198-103">Элемент Аусорлист (Комментс_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="31198-103">AuthorList element (Comments_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="31198-104">Указывает авторов комментариев в документе.</span><span class="sxs-lookup"><span data-stu-id="31198-104">Specifies the authors of comments in a drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31198-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="31198-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31198-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="31198-106">**Element type**</span></span> <br/> |[<span data-ttu-id="31198-107">Аусорлист_типе</span><span class="sxs-lookup"><span data-stu-id="31198-107">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="31198-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="31198-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="31198-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="31198-109">**Schema file**</span></span> <br/> |<span data-ttu-id="31198-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="31198-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="31198-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="31198-111">**Document parts**</span></span> <br/> |<span data-ttu-id="31198-112">Comments. XML</span><span class="sxs-lookup"><span data-stu-id="31198-112">comments.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="31198-113">Определение</span><span class="sxs-lookup"><span data-stu-id="31198-113">Definition</span></span>

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="31198-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="31198-114">Elements and attributes</span></span>

<span data-ttu-id="31198-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="31198-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="31198-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="31198-116">Parent elements</span></span>

|<span data-ttu-id="31198-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="31198-117">**Element**</span></span>|<span data-ttu-id="31198-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="31198-118">**Type**</span></span>|<span data-ttu-id="31198-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="31198-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="31198-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="31198-120">Comments</span></span>](comments-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="31198-121">Комментс_типе</span><span class="sxs-lookup"><span data-stu-id="31198-121">Comments_Type</span></span>](comments_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="31198-122">Задает комментарии в документе.</span><span class="sxs-lookup"><span data-stu-id="31198-122">Specifies the comments in a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="31198-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="31198-123">Child elements</span></span>

|<span data-ttu-id="31198-124">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="31198-124">**Element**</span></span>|<span data-ttu-id="31198-125">**Тип**</span><span class="sxs-lookup"><span data-stu-id="31198-125">**Type**</span></span>|<span data-ttu-id="31198-126">**Описание**</span><span class="sxs-lookup"><span data-stu-id="31198-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="31198-127">Аусорентри</span><span class="sxs-lookup"><span data-stu-id="31198-127">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="31198-128">Аусорентри_типе</span><span class="sxs-lookup"><span data-stu-id="31198-128">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="31198-129">Задает свойства, которые определяют автора комментария в документе.</span><span class="sxs-lookup"><span data-stu-id="31198-129">Specifies the properties that identify the author of a comment in a drawing.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="31198-130">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="31198-130">Attributes</span></span>

<span data-ttu-id="31198-131">Нет.</span><span class="sxs-lookup"><span data-stu-id="31198-131">None.</span></span>
  

