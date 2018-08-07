---
title: LayerRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c8015f59-06a7-54c5-2df6-bc9e4d19f17b
ms.openlocfilehash: 2382c7fbe244d031d3aa2004b9887e6495b0f7a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814072"
---
# <a name="layerrowtype-complextype-visio-xml"></a><span data-ttu-id="e7807-102">LayerRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e7807-102">LayerRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e7807-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e7807-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7807-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e7807-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e7807-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e7807-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e7807-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e7807-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e7807-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="e7807-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e7807-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="e7807-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e7807-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e7807-109">Definition</span></span>

```XML
          <xs:complexType name="LayerRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
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

## <a name="elements-and-attributes"></a><span data-ttu-id="e7807-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e7807-110">Elements and attributes</span></span>

<span data-ttu-id="e7807-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="e7807-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e7807-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e7807-112">Child elements</span></span>

|<span data-ttu-id="e7807-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e7807-113">**Element**</span></span>|<span data-ttu-id="e7807-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e7807-114">**Type**</span></span>|<span data-ttu-id="e7807-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e7807-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e7807-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e7807-116">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="e7807-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e7807-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e7807-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e7807-118">Attributes</span></span>

<span data-ttu-id="e7807-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="e7807-119">None.</span></span>
  

