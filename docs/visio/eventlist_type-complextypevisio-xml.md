---
title: EventList_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 7bbb8d1074d869a9171a188118c920260b3a903d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813712"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="fff09-102">EventList_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="fff09-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="fff09-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="fff09-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fff09-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="fff09-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="fff09-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="fff09-105">**Schema file**</span></span> <br/> |<span data-ttu-id="fff09-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="fff09-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="fff09-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="fff09-107">**Extension base**</span></span> <br/> |<span data-ttu-id="fff09-108">Нет</span><span class="sxs-lookup"><span data-stu-id="fff09-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fff09-109">Определение</span><span class="sxs-lookup"><span data-stu-id="fff09-109">Definition</span></span>

```XML
          <xs:complexType name="EventList_Type">
          
          <xs:sequence>
    <xs:element name="EventItem"  type="EventItem_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fff09-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="fff09-110">Elements and attributes</span></span>

<span data-ttu-id="fff09-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="fff09-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="fff09-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fff09-112">Child elements</span></span>

|<span data-ttu-id="fff09-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="fff09-113">**Element**</span></span>|<span data-ttu-id="fff09-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="fff09-114">**Type**</span></span>|<span data-ttu-id="fff09-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fff09-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fff09-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="fff09-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fff09-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="fff09-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="fff09-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fff09-118">Attributes</span></span>

<span data-ttu-id="fff09-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="fff09-119">None.</span></span>
  

