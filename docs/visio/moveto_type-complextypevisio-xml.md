---
title: MoveTo_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4cd3e605-9ac1-14f5-f4e1-992c9100b1b2
ms.openlocfilehash: ea88f86ad9e38692408730b49ee2f3d6cbc35a54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814287"
---
# <a name="movetotype-complextype-visio-xml"></a><span data-ttu-id="e5826-102">MoveTo_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="e5826-102">MoveTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e5826-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="e5826-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5826-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e5826-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e5826-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e5826-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e5826-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e5826-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e5826-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="e5826-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e5826-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="e5826-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5826-109">Определение</span><span class="sxs-lookup"><span data-stu-id="e5826-109">Definition</span></span>

```XML
          <xs:complexType name="MoveTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="e5826-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5826-110">Elements and attributes</span></span>

<span data-ttu-id="e5826-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="e5826-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e5826-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e5826-112">Child elements</span></span>

|<span data-ttu-id="e5826-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e5826-113">**Element**</span></span>|<span data-ttu-id="e5826-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e5826-114">**Type**</span></span>|<span data-ttu-id="e5826-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5826-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5826-116">Cell</span><span class="sxs-lookup"><span data-stu-id="e5826-116">Cell</span></span>](cell-element-moveto-rowvisio-xml.md) <br/> |[<span data-ttu-id="e5826-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e5826-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e5826-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e5826-118">Attributes</span></span>

<span data-ttu-id="e5826-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="e5826-119">None.</span></span>
  

