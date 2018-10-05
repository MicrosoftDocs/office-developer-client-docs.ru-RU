---
title: Shapes_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ef84fa3-6fb8-c570-a5ee-3c1c9dddb86c
ms.openlocfilehash: 7d028939ad6c99ecf4160b95764c86779c399c8e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397613"
---
# <a name="shapestype-complextype-visio-xml"></a><span data-ttu-id="b7a71-102">Shapes_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="b7a71-102">Shapes_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b7a71-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b7a71-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7a71-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b7a71-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b7a71-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b7a71-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b7a71-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b7a71-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b7a71-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b7a71-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b7a71-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b7a71-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7a71-109">Определение</span><span class="sxs-lookup"><span data-stu-id="b7a71-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b7a71-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7a71-110">Elements and attributes</span></span>

<span data-ttu-id="b7a71-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b7a71-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b7a71-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7a71-112">Child elements</span></span>

|<span data-ttu-id="b7a71-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b7a71-113">**Element**</span></span>|<span data-ttu-id="b7a71-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7a71-114">**Type**</span></span>|<span data-ttu-id="b7a71-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7a71-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7a71-116">Фигура</span><span class="sxs-lookup"><span data-stu-id="b7a71-116">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b7a71-117">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="b7a71-117">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b7a71-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7a71-118">Attributes</span></span>

<span data-ttu-id="b7a71-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="b7a71-119">None.</span></span>
  

