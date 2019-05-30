---
title: Табс_типе complexType (XML для Visio)
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
# <a name="tabstype-complextype-visio-xml"></a><span data-ttu-id="44277-102">Табс_типе complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="44277-102">Tabs_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="44277-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="44277-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44277-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="44277-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="44277-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="44277-105">**Schema file**</span></span> <br/> |<span data-ttu-id="44277-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="44277-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="44277-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="44277-107">**Extension base**</span></span> <br/> |<span data-ttu-id="44277-108">Сектион_типе</span><span class="sxs-lookup"><span data-stu-id="44277-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="44277-109">Определение</span><span class="sxs-lookup"><span data-stu-id="44277-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="44277-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="44277-110">Elements and attributes</span></span>

<span data-ttu-id="44277-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="44277-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="44277-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="44277-112">Child elements</span></span>

|<span data-ttu-id="44277-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="44277-113">**Element**</span></span>|<span data-ttu-id="44277-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="44277-114">**Type**</span></span>|<span data-ttu-id="44277-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="44277-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="44277-116">Row</span><span class="sxs-lookup"><span data-stu-id="44277-116">Row</span></span>](row-element-tabs-sectionvisio-xml.md) <br/> |[<span data-ttu-id="44277-117">Табсров_типе</span><span class="sxs-lookup"><span data-stu-id="44277-117">TabsRow_Type</span></span>](tabsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="44277-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="44277-118">Attributes</span></span>

<span data-ttu-id="44277-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="44277-119">None.</span></span>
  

