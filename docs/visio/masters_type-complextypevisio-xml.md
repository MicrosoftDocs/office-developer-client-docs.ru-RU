---
title: Masters_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398495"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="06873-102">Masters_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="06873-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="06873-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="06873-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="06873-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="06873-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="06873-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="06873-105">**Schema file**</span></span> <br/> |<span data-ttu-id="06873-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="06873-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="06873-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="06873-107">**Extension base**</span></span> <br/> |<span data-ttu-id="06873-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="06873-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="06873-109">Определение</span><span class="sxs-lookup"><span data-stu-id="06873-109">Definition</span></span>

```XML
          <xs:complexType name="Masters_Type">
          
          <xs:sequence>
    <xs:element name="Master"  type="Master_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="MasterShortcut"  type="MasterShortcut_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="06873-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="06873-110">Elements and attributes</span></span>

<span data-ttu-id="06873-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="06873-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="06873-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="06873-112">Child elements</span></span>

|<span data-ttu-id="06873-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="06873-113">**Element**</span></span>|<span data-ttu-id="06873-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="06873-114">**Type**</span></span>|<span data-ttu-id="06873-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="06873-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="06873-116">Master</span><span class="sxs-lookup"><span data-stu-id="06873-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="06873-117">Master_Type</span><span class="sxs-lookup"><span data-stu-id="06873-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="06873-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="06873-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="06873-119">MasterShortcut_Type</span><span class="sxs-lookup"><span data-stu-id="06873-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="06873-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="06873-120">Attributes</span></span>

<span data-ttu-id="06873-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="06873-121">None.</span></span>
  

