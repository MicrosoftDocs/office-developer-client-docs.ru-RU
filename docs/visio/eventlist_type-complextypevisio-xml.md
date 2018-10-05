---
title: EventList_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0e7a6e5e-5ce4-1e21-c1e8-dafd22bd367f
ms.openlocfilehash: 454a54749e9f72cacc3e7359041705d3487b9e79
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392083"
---
# <a name="eventlisttype-complextype-visio-xml"></a><span data-ttu-id="99a53-102">EventList_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="99a53-102">EventList_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="99a53-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="99a53-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="99a53-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="99a53-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="99a53-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="99a53-105">**Schema file**</span></span> <br/> |<span data-ttu-id="99a53-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="99a53-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="99a53-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="99a53-107">**Extension base**</span></span> <br/> |<span data-ttu-id="99a53-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="99a53-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="99a53-109">Определение</span><span class="sxs-lookup"><span data-stu-id="99a53-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="99a53-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="99a53-110">Elements and attributes</span></span>

<span data-ttu-id="99a53-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="99a53-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="99a53-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="99a53-112">Child elements</span></span>

|<span data-ttu-id="99a53-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="99a53-113">**Element**</span></span>|<span data-ttu-id="99a53-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="99a53-114">**Type**</span></span>|<span data-ttu-id="99a53-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="99a53-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="99a53-116">EventItem</span><span class="sxs-lookup"><span data-stu-id="99a53-116">EventItem</span></span>](eventitem-element-eventlist_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="99a53-117">EventItem_Type</span><span class="sxs-lookup"><span data-stu-id="99a53-117">EventItem_Type</span></span>](eventitem_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="99a53-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="99a53-118">Attributes</span></span>

<span data-ttu-id="99a53-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="99a53-119">None.</span></span>
  

