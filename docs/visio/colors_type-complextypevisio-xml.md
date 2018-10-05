---
title: Colors_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f997b5-1f3c-ddff-41f2-af84960266ff
ms.openlocfilehash: e447ceb6fc0e6b79ec6e62b5f3b73a32cec589d9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400917"
---
# <a name="colorstype-complextype-visio-xml"></a><span data-ttu-id="55ede-102">Colors_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="55ede-102">Colors_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="55ede-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="55ede-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55ede-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="55ede-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="55ede-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="55ede-105">**Schema file**</span></span> <br/> |<span data-ttu-id="55ede-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="55ede-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="55ede-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="55ede-107">**Extension base**</span></span> <br/> |<span data-ttu-id="55ede-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="55ede-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="55ede-109">Определение</span><span class="sxs-lookup"><span data-stu-id="55ede-109">Definition</span></span>

```XML
          <xs:complexType name="Colors_Type">
          
          <xs:sequence>
    <xs:element name="ColorEntry"  type="ColorEntry_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="55ede-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="55ede-110">Elements and attributes</span></span>

<span data-ttu-id="55ede-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="55ede-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="55ede-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="55ede-112">Child elements</span></span>

|<span data-ttu-id="55ede-113">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="55ede-113">**Element**</span></span>|<span data-ttu-id="55ede-114">**Тип**</span><span class="sxs-lookup"><span data-stu-id="55ede-114">**Type**</span></span>|<span data-ttu-id="55ede-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="55ede-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="55ede-116">ColorEntry</span><span class="sxs-lookup"><span data-stu-id="55ede-116">ColorEntry</span></span>](colorentry-element-colors_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="55ede-117">ColorEntry_Type</span><span class="sxs-lookup"><span data-stu-id="55ede-117">ColorEntry_Type</span></span>](colorentry_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="55ede-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="55ede-118">Attributes</span></span>

<span data-ttu-id="55ede-119">Нет.</span><span class="sxs-lookup"><span data-stu-id="55ede-119">None.</span></span>
  

