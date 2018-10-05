---
title: Layer_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f92ac1cc-fad2-dab9-5507-838c006ed633
ms.openlocfilehash: 9e6e477e97a0c8f1be1a89bd14262bb4c2a0d7dc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396705"
---
# <a name="layertype-complextype-visio-xml"></a><span data-ttu-id="5430c-102">Layer_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="5430c-102">Layer_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="5430c-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="5430c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5430c-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5430c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="5430c-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5430c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="5430c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="5430c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="5430c-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="5430c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="5430c-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="5430c-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5430c-109">Определение</span><span class="sxs-lookup"><span data-stu-id="5430c-109">Definition</span></span>

```XML
          <xs:complexType name="Layer_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="LayerRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5430c-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5430c-110">Elements and attributes</span></span>

<span data-ttu-id="5430c-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5430c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="5430c-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5430c-112">Child elements</span></span>

|<span data-ttu-id="5430c-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5430c-113">**Element**</span></span>|<span data-ttu-id="5430c-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5430c-114">**Type**</span></span>|<span data-ttu-id="5430c-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5430c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5430c-116">Строка</span><span class="sxs-lookup"><span data-stu-id="5430c-116">Row</span></span>](row-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="5430c-117">LayerRow_Type</span><span class="sxs-lookup"><span data-stu-id="5430c-117">LayerRow_Type</span></span>](layerrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="5430c-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5430c-118">Attributes</span></span>

<span data-ttu-id="5430c-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="5430c-119">None.</span></span>
  

