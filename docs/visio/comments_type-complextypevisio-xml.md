---
title: Comments_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6bc870d2-e163-636f-beae-b3002d54a96c
ms.openlocfilehash: 4d7a1d75387ddc84bec8eb1370cfb7d641c8a9ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813427"
---
# <a name="commentstype-complextype-visio-xml"></a><span data-ttu-id="730c8-102">Comments_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="730c8-102">Comments_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="730c8-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="730c8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="730c8-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="730c8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="730c8-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="730c8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="730c8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="730c8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="730c8-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="730c8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="730c8-108">Нет</span><span class="sxs-lookup"><span data-stu-id="730c8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="730c8-109">Определение</span><span class="sxs-lookup"><span data-stu-id="730c8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="730c8-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="730c8-110">Elements and attributes</span></span>

<span data-ttu-id="730c8-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="730c8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="730c8-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="730c8-112">Child elements</span></span>

|<span data-ttu-id="730c8-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="730c8-113">**Element**</span></span>|<span data-ttu-id="730c8-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="730c8-114">**Type**</span></span>|<span data-ttu-id="730c8-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="730c8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="730c8-116">AuthorList</span><span class="sxs-lookup"><span data-stu-id="730c8-116">AuthorList</span></span>](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="730c8-117">AuthorList_Type</span><span class="sxs-lookup"><span data-stu-id="730c8-117">AuthorList_Type</span></span>](authorlist_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="730c8-118">CommentList</span><span class="sxs-lookup"><span data-stu-id="730c8-118">CommentList</span></span>](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="730c8-119">CommentList_Type</span><span class="sxs-lookup"><span data-stu-id="730c8-119">CommentList_Type</span></span>](commentlist_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="730c8-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="730c8-120">Attributes</span></span>

|<span data-ttu-id="730c8-121">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="730c8-121">**Attribute**</span></span>|<span data-ttu-id="730c8-122">**Тип**</span><span class="sxs-lookup"><span data-stu-id="730c8-122">**Type**</span></span>|<span data-ttu-id="730c8-123">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="730c8-123">**Required**</span></span>|<span data-ttu-id="730c8-124">**Описание**</span><span class="sxs-lookup"><span data-stu-id="730c8-124">**Description**</span></span>|<span data-ttu-id="730c8-125">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="730c8-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="730c8-126">ShowCommentTags</span><span class="sxs-lookup"><span data-stu-id="730c8-126">ShowCommentTags</span></span>  <br/> |<span data-ttu-id="730c8-127">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="730c8-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="730c8-128">необязательный</span><span class="sxs-lookup"><span data-stu-id="730c8-128">optional</span></span>  <br/> ||<span data-ttu-id="730c8-129">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="730c8-129">Values of the xsd:boolean type.</span></span>  <br/> |
   

