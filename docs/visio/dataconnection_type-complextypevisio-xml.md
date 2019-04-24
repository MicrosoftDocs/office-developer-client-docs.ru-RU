---
title: Датаконнектион_типе complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344606"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="463c2-102">Датаконнектион_типе complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="463c2-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="463c2-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="463c2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="463c2-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="463c2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="463c2-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="463c2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="463c2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="463c2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="463c2-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="463c2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="463c2-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="463c2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="463c2-109">Определение</span><span class="sxs-lookup"><span data-stu-id="463c2-109">Definition</span></span>

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="463c2-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="463c2-110">Elements and attributes</span></span>

<span data-ttu-id="463c2-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="463c2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="463c2-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="463c2-112">Child elements</span></span>

<span data-ttu-id="463c2-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="463c2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="463c2-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="463c2-114">Attributes</span></span>

|<span data-ttu-id="463c2-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="463c2-115">**Attribute**</span></span>|<span data-ttu-id="463c2-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="463c2-116">**Type**</span></span>|<span data-ttu-id="463c2-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="463c2-117">**Required**</span></span>|<span data-ttu-id="463c2-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="463c2-118">**Description**</span></span>|<span data-ttu-id="463c2-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="463c2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="463c2-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="463c2-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="463c2-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="463c2-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="463c2-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="463c2-122">optional</span></span>  <br/> ||<span data-ttu-id="463c2-123">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="463c2-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="463c2-124">Command</span><span class="sxs-lookup"><span data-stu-id="463c2-124">Command</span></span>  <br/> |<span data-ttu-id="463c2-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="463c2-125">xsd:string</span></span>  <br/> |<span data-ttu-id="463c2-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="463c2-126">optional</span></span>  <br/> ||<span data-ttu-id="463c2-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="463c2-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="463c2-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="463c2-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="463c2-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="463c2-129">xsd:string</span></span>  <br/> |<span data-ttu-id="463c2-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="463c2-130">optional</span></span>  <br/> ||<span data-ttu-id="463c2-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="463c2-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="463c2-132">FileName</span><span class="sxs-lookup"><span data-stu-id="463c2-132">FileName</span></span>  <br/> |<span data-ttu-id="463c2-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="463c2-133">xsd:string</span></span>  <br/> |<span data-ttu-id="463c2-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="463c2-134">required</span></span>  <br/> ||<span data-ttu-id="463c2-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="463c2-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="463c2-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="463c2-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="463c2-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="463c2-137">xsd:string</span></span>  <br/> |<span data-ttu-id="463c2-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="463c2-138">optional</span></span>  <br/> ||<span data-ttu-id="463c2-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="463c2-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="463c2-140">ИД</span><span class="sxs-lookup"><span data-stu-id="463c2-140">ID</span></span>  <br/> |<span data-ttu-id="463c2-141">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="463c2-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="463c2-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="463c2-142">required</span></span>  <br/> ||<span data-ttu-id="463c2-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="463c2-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="463c2-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="463c2-144">Timeout</span></span>  <br/> |<span data-ttu-id="463c2-145">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="463c2-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="463c2-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="463c2-146">optional</span></span>  <br/> ||<span data-ttu-id="463c2-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="463c2-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

