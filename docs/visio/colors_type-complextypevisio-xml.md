---
title: Colors_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: 187d51c2102e9d13ffea15c6de2db849ef980fb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813393"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="1b664-102">Colors_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="1b664-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1b664-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1b664-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b664-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1b664-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1b664-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1b664-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1b664-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1b664-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1b664-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="1b664-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1b664-108">Нет</span><span class="sxs-lookup"><span data-stu-id="1b664-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b664-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1b664-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1b664-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1b664-110">Elements and attributes</span></span>

<span data-ttu-id="1b664-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="1b664-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1b664-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1b664-112">Child elements</span></span>

|<span data-ttu-id="1b664-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1b664-113">**Element**</span></span>|<span data-ttu-id="1b664-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1b664-114">**Type**</span></span>|<span data-ttu-id="1b664-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1b664-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b664-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="1b664-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1b664-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="1b664-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1b664-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1b664-118">Attributes</span></span>

<span data-ttu-id="1b664-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="1b664-119">None.</span></span>
  

