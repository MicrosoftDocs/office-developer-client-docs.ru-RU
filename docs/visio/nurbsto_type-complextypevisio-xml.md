---
title: NURBSTo_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7ae8a1d-5bb7-a92f-79d6-5a358d879c32
ms.openlocfilehash: 9b575662ef39eb4a6809d8c249771ad417c2bb45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814307"
---
# <a name="nurbstotype-complextype-visio-xml"></a><span data-ttu-id="12deb-102">NURBSTo_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="12deb-102">NURBSTo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="12deb-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="12deb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12deb-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="12deb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="12deb-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="12deb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="12deb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="12deb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="12deb-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="12deb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="12deb-108">GeometryRow_Type</span><span class="sxs-lookup"><span data-stu-id="12deb-108">GeometryRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="12deb-109">Определение</span><span class="sxs-lookup"><span data-stu-id="12deb-109">Definition</span></span>

```XML
          <xs:complexType name="NURBSTo_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="12deb-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="12deb-110">Elements and attributes</span></span>

<span data-ttu-id="12deb-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="12deb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="12deb-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="12deb-112">Child elements</span></span>

|<span data-ttu-id="12deb-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="12deb-113">**Element**</span></span>|<span data-ttu-id="12deb-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="12deb-114">**Type**</span></span>|<span data-ttu-id="12deb-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="12deb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="12deb-116">Cell</span><span class="sxs-lookup"><span data-stu-id="12deb-116">Cell</span></span>](cell-element-nurbsto-rowvisio-xml.md) <br/> |[<span data-ttu-id="12deb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="12deb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="12deb-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="12deb-118">Attributes</span></span>

<span data-ttu-id="12deb-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="12deb-119">None.</span></span>
  

