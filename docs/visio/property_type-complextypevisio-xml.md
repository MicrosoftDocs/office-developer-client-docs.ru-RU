---
title: Property_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4f927461-7122-1742-57f5-e2035890b486
ms.openlocfilehash: ed0cd01a47a1bdd3df77fdd1210f196ec20670b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814489"
---
# <a name="propertytype-complextype-visio-xml"></a><span data-ttu-id="cc84b-102">Property_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="cc84b-102">Property_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cc84b-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="cc84b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc84b-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="cc84b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cc84b-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="cc84b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cc84b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cc84b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cc84b-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="cc84b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cc84b-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="cc84b-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc84b-109">Определение</span><span class="sxs-lookup"><span data-stu-id="cc84b-109">Definition</span></span>

```XML
          <xs:complexType name="Property_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="PropertyRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc84b-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="cc84b-110">Elements and attributes</span></span>

<span data-ttu-id="cc84b-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="cc84b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cc84b-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="cc84b-112">Child elements</span></span>

|<span data-ttu-id="cc84b-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="cc84b-113">**Element**</span></span>|<span data-ttu-id="cc84b-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="cc84b-114">**Type**</span></span>|<span data-ttu-id="cc84b-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="cc84b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc84b-116">Row</span><span class="sxs-lookup"><span data-stu-id="cc84b-116">Row</span></span>](row-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="cc84b-117">PropertyRow_Type</span><span class="sxs-lookup"><span data-stu-id="cc84b-117">PropertyRow_Type</span></span>](propertyrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cc84b-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="cc84b-118">Attributes</span></span>

<span data-ttu-id="cc84b-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="cc84b-119">None.</span></span>
  

