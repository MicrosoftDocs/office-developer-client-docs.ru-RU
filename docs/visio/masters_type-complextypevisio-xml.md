---
title: Мастерс_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beb489ab-d43c-51ad-d089-69c87d658a59
ms.openlocfilehash: 4b66e0cb7fded75a8c65f2ce93bc42442bedb033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341659"
---
# <a name="masterstype-complextype-visio-xml"></a><span data-ttu-id="b4c41-102">Мастерс_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="b4c41-102">Masters_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b4c41-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="b4c41-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4c41-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b4c41-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b4c41-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b4c41-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b4c41-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b4c41-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b4c41-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="b4c41-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b4c41-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="b4c41-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b4c41-109">Определение</span><span class="sxs-lookup"><span data-stu-id="b4c41-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b4c41-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b4c41-110">Elements and attributes</span></span>

<span data-ttu-id="b4c41-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b4c41-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b4c41-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b4c41-112">Child elements</span></span>

|<span data-ttu-id="b4c41-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b4c41-113">**Element**</span></span>|<span data-ttu-id="b4c41-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b4c41-114">**Type**</span></span>|<span data-ttu-id="b4c41-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b4c41-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b4c41-116">Master</span><span class="sxs-lookup"><span data-stu-id="b4c41-116">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b4c41-117">Мастер_типе</span><span class="sxs-lookup"><span data-stu-id="b4c41-117">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b4c41-118">MasterShortcut</span><span class="sxs-lookup"><span data-stu-id="b4c41-118">MasterShortcut</span></span>](mastershortcut-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b4c41-119">Мастершорткут_типе</span><span class="sxs-lookup"><span data-stu-id="b4c41-119">MasterShortcut_Type</span></span>](mastershortcut_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b4c41-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b4c41-120">Attributes</span></span>

<span data-ttu-id="b4c41-121">Нет.</span><span class="sxs-lookup"><span data-stu-id="b4c41-121">None.</span></span>
  

