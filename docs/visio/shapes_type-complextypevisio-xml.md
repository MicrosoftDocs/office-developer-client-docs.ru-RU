---
title: Shapes_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 707f20823d0413e0b064b2a367da803419889ef7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814800"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="9cb68-102">Shapes_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="9cb68-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9cb68-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="9cb68-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9cb68-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="9cb68-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9cb68-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="9cb68-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9cb68-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9cb68-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9cb68-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="9cb68-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9cb68-108">Нет</span><span class="sxs-lookup"><span data-stu-id="9cb68-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9cb68-109">Определение</span><span class="sxs-lookup"><span data-stu-id="9cb68-109">Definition</span></span>

```XML
          <xs:complexType name="Shapes_Type">
          
          <xs:sequence>
    <xs:element name="Shape"  type="ShapeSheet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9cb68-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="9cb68-110">Elements and attributes</span></span>

<span data-ttu-id="9cb68-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="9cb68-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9cb68-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9cb68-112">Child elements</span></span>

|<span data-ttu-id="9cb68-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="9cb68-113">**Element**</span></span>|<span data-ttu-id="9cb68-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="9cb68-114">**Type**</span></span>|<span data-ttu-id="9cb68-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9cb68-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9cb68-116">Фигура</span><span class="sxs-lookup"><span data-stu-id="9cb68-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9cb68-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="9cb68-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9cb68-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="9cb68-118">Attributes</span></span>

<span data-ttu-id="9cb68-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="9cb68-119">None.</span></span>
  

