---
title: AuthorList_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc1e059b-7705-8b30-aeab-f56707086416
ms.openlocfilehash: e4cee87a5060580e8b7f1efc7970091d56fd310f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813148"
---
# <a name="authorlisttype-complextype-visio-xml"></a><span data-ttu-id="49bc5-102">AuthorList_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="49bc5-102">AuthorList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="49bc5-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="49bc5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="49bc5-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="49bc5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="49bc5-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="49bc5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="49bc5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="49bc5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="49bc5-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="49bc5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="49bc5-108">Нет</span><span class="sxs-lookup"><span data-stu-id="49bc5-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="49bc5-109">Определение</span><span class="sxs-lookup"><span data-stu-id="49bc5-109">Definition</span></span>

```XML
          <xs:complexType name="AuthorList_Type">
          
          <xs:sequence>
    <xs:element name="AuthorEntry"  type="AuthorEntry_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="49bc5-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="49bc5-110">Elements and attributes</span></span>

<span data-ttu-id="49bc5-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="49bc5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="49bc5-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="49bc5-112">Child elements</span></span>

|<span data-ttu-id="49bc5-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="49bc5-113">**Element**</span></span>|<span data-ttu-id="49bc5-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="49bc5-114">**Type**</span></span>|<span data-ttu-id="49bc5-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="49bc5-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="49bc5-116">AuthorEntry</span><span class="sxs-lookup"><span data-stu-id="49bc5-116">AuthorEntry</span></span>](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="49bc5-117">AuthorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="49bc5-117">AuthorEntry_Type</span></span>](authorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="49bc5-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="49bc5-118">Attributes</span></span>

<span data-ttu-id="49bc5-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="49bc5-119">None.</span></span>
  

