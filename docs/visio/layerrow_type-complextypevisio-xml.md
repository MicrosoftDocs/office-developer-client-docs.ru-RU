---
title: LayerRow_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c8015f59-06a7-54c5-2df6-bc9e4d19f17b
ms.openlocfilehash: 332bd6bc93f66bad46b726cb42bad471980a6a3c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388275"
---
# <a name="layerrowtype-complextype-visio-xml"></a><span data-ttu-id="0f344-102">LayerRow_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="0f344-102">LayerRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0f344-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0f344-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0f344-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0f344-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0f344-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0f344-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0f344-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0f344-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0f344-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0f344-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0f344-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="0f344-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0f344-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0f344-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0f344-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0f344-110">Elements and attributes</span></span>

<span data-ttu-id="0f344-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0f344-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0f344-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0f344-112">Child elements</span></span>

|<span data-ttu-id="0f344-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0f344-113">**Element**</span></span>|<span data-ttu-id="0f344-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0f344-114">**Type**</span></span>|<span data-ttu-id="0f344-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0f344-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0f344-116">Cell</span><span class="sxs-lookup"><span data-stu-id="0f344-116">Cell</span></span>](cell-element-layer-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0f344-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="0f344-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0f344-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0f344-118">Attributes</span></span>

<span data-ttu-id="0f344-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="0f344-119">None.</span></span>
  

