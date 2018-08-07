---
title: Tabs_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b97155ce-f0d2-e35c-bc58-e288f653ce2c
ms.openlocfilehash: a46e9d0cfa1ad0e9bd398afec7a2f03de46c367f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814977"
---
# <a name="tabstype-complextype-visio-xml"></a><span data-ttu-id="6ce96-102">Tabs_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="6ce96-102">Tabs_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6ce96-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="6ce96-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6ce96-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6ce96-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6ce96-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6ce96-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6ce96-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6ce96-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6ce96-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="6ce96-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6ce96-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="6ce96-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6ce96-109">Определение</span><span class="sxs-lookup"><span data-stu-id="6ce96-109">Definition</span></span>

```XML
          <xs:complexType name="Tabs_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="TabsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6ce96-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6ce96-110">Elements and attributes</span></span>

<span data-ttu-id="6ce96-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="6ce96-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6ce96-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6ce96-112">Child elements</span></span>

|<span data-ttu-id="6ce96-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6ce96-113">**Element**</span></span>|<span data-ttu-id="6ce96-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6ce96-114">**Type**</span></span>|<span data-ttu-id="6ce96-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6ce96-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6ce96-116">Row</span><span class="sxs-lookup"><span data-stu-id="6ce96-116">Row</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="6ce96-117">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="6ce96-117">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6ce96-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6ce96-118">Attributes</span></span>

<span data-ttu-id="6ce96-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="6ce96-119">None.</span></span>
  

