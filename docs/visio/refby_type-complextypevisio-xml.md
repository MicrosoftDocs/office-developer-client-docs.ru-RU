---
title: RefBy_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e2990281-6410-5a35-2b28-3a8b33246c73
ms.openlocfilehash: 7970ae735f4933f05e71f1758912d3ecd382bf89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538279"
---
# <a name="refby_type-complextype-visio-xml"></a><span data-ttu-id="8524d-102">RefBy_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="8524d-102">RefBy_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="8524d-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="8524d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8524d-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="8524d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="8524d-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="8524d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="8524d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="8524d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="8524d-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="8524d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="8524d-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="8524d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="8524d-109">Определение</span><span class="sxs-lookup"><span data-stu-id="8524d-109">Definition</span></span>

```XML
      <xs:complexType name="RefBy_Type">
    <xs:attribute name="T"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="8524d-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="8524d-110">Elements and attributes</span></span>

<span data-ttu-id="8524d-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="8524d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="8524d-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8524d-112">Child elements</span></span>

<span data-ttu-id="8524d-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="8524d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8524d-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="8524d-114">Attributes</span></span>

|<span data-ttu-id="8524d-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="8524d-115">**Attribute**</span></span>|<span data-ttu-id="8524d-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="8524d-116">**Type**</span></span>|<span data-ttu-id="8524d-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="8524d-117">**Required**</span></span>|<span data-ttu-id="8524d-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="8524d-118">**Description**</span></span>|<span data-ttu-id="8524d-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="8524d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8524d-120">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="8524d-120">ID</span></span>  <br/> |<span data-ttu-id="8524d-121">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="8524d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="8524d-122">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8524d-122">required</span></span>  <br/> ||<span data-ttu-id="8524d-123">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="8524d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="8524d-124">Д</span><span class="sxs-lookup"><span data-stu-id="8524d-124">T</span></span>  <br/> |<span data-ttu-id="8524d-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="8524d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="8524d-126">Обязательный</span><span class="sxs-lookup"><span data-stu-id="8524d-126">required</span></span>  <br/> ||<span data-ttu-id="8524d-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="8524d-127">Values of the xsd:string type.</span></span>  <br/> |
   

