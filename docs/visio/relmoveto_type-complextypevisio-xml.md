---
title: RelMoveTo_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3759d7cc-061b-0c0b-c372-b7d60effbfd0
ms.openlocfilehash: fd0af55b33bb6c14a3d5203d1f6c469e55f91d23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814578"
---
# <a name="relmovetotype-complextype-visio-xml"></a><span data-ttu-id="7b5af-102">RelMoveTo_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="7b5af-102">RelMoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7b5af-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="7b5af-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b5af-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="7b5af-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7b5af-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="7b5af-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7b5af-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7b5af-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7b5af-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="7b5af-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7b5af-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="7b5af-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7b5af-109">Определение</span><span class="sxs-lookup"><span data-stu-id="7b5af-109">Definition</span></span>

```XML
          <xs:complexType name="RelMoveTo_Type">
          
          <xs:complexContent>
          <xs:extension base="GeometryRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7b5af-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b5af-110">Elements and attributes</span></span>

<span data-ttu-id="7b5af-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="7b5af-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7b5af-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7b5af-112">Child elements</span></span>

|<span data-ttu-id="7b5af-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="7b5af-113">**Element**</span></span>|<span data-ttu-id="7b5af-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="7b5af-114">**Type**</span></span>|<span data-ttu-id="7b5af-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b5af-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7b5af-116">Cell</span><span class="sxs-lookup"><span data-stu-id="7b5af-116">Cell</span></span>](cell-element-relmoveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="7b5af-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7b5af-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7b5af-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7b5af-118">Attributes</span></span>

<span data-ttu-id="7b5af-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="7b5af-119">None.</span></span>
  

