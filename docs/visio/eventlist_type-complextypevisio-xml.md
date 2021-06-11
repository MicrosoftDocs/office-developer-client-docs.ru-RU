---
title: EventList_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: bcee61ba9347dc77dd704d0221a9362843bf9858
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540765"
---
# <a name="eventlist_type-complextype-visio-xml"></a><span data-ttu-id="17016-102">EventList_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="17016-102">EventList_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="17016-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="17016-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17016-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="17016-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="17016-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="17016-105">**Schema file**</span></span> <br/> |<span data-ttu-id="17016-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="17016-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="17016-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="17016-107">**Extension base**</span></span> <br/> |<span data-ttu-id="17016-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="17016-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17016-109">Определение</span><span class="sxs-lookup"><span data-stu-id="17016-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="17016-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="17016-110">Elements and attributes</span></span>

<span data-ttu-id="17016-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="17016-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="17016-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="17016-112">Child elements</span></span>

|<span data-ttu-id="17016-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="17016-113">**Element**</span></span>|<span data-ttu-id="17016-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="17016-114">**Type**</span></span>|<span data-ttu-id="17016-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="17016-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17016-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="17016-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="17016-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="17016-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="17016-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="17016-118">Attributes</span></span>

<span data-ttu-id="17016-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="17016-119">None.</span></span>
  

