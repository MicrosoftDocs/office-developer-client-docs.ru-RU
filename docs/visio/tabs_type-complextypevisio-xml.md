---
title: Tabs_Type ComplexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b97155ce-f0d2-e35c-bc58-e288f653ce2c
ms.openlocfilehash: f3c484fe8656d97484dd136175506bf60f0e299b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538846"
---
# <a name="tabs_type-complextype-visio-xml"></a><span data-ttu-id="0b282-102">Tabs_Type ComplexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="0b282-102">Tabs_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0b282-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="0b282-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b282-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="0b282-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0b282-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="0b282-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0b282-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0b282-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0b282-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="0b282-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0b282-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="0b282-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0b282-109">Определение</span><span class="sxs-lookup"><span data-stu-id="0b282-109">Definition</span></span>

```XML
          <xs:complexType name="Tabs_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="TabsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0b282-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="0b282-110">Elements and attributes</span></span>

<span data-ttu-id="0b282-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="0b282-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0b282-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0b282-112">Child elements</span></span>

|<span data-ttu-id="0b282-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="0b282-113">**Element**</span></span>|<span data-ttu-id="0b282-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="0b282-114">**Type**</span></span>|<span data-ttu-id="0b282-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0b282-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0b282-116">Row</span><span class="sxs-lookup"><span data-stu-id="0b282-116">Row</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="0b282-117">TabsRow_Type</span><span class="sxs-lookup"><span data-stu-id="0b282-117">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="0b282-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0b282-118">Attributes</span></span>

<span data-ttu-id="0b282-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="0b282-119">None.</span></span>
  

