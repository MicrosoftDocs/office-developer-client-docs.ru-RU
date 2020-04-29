---
title: DataConnection_Type complexType (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539651"
---
# <a name="dataconnection_type-complextype-visio-xml"></a><span data-ttu-id="1170e-102">DataConnection_Type complexType (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="1170e-102">DataConnection_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="1170e-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="1170e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1170e-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="1170e-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1170e-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="1170e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1170e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1170e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1170e-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="1170e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1170e-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="1170e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1170e-109">Определение</span><span class="sxs-lookup"><span data-stu-id="1170e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1170e-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="1170e-110">Elements and attributes</span></span>

<span data-ttu-id="1170e-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="1170e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1170e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1170e-112">Child elements</span></span>

<span data-ttu-id="1170e-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="1170e-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1170e-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="1170e-114">Attributes</span></span>

|<span data-ttu-id="1170e-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="1170e-115">**Attribute**</span></span>|<span data-ttu-id="1170e-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="1170e-116">**Type**</span></span>|<span data-ttu-id="1170e-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="1170e-117">**Required**</span></span>|<span data-ttu-id="1170e-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1170e-118">**Description**</span></span>|<span data-ttu-id="1170e-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="1170e-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1170e-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="1170e-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="1170e-121">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="1170e-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1170e-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="1170e-122">optional</span></span>  <br/> ||<span data-ttu-id="1170e-123">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="1170e-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1170e-124">Command</span><span class="sxs-lookup"><span data-stu-id="1170e-124">Command</span></span>  <br/> |<span data-ttu-id="1170e-125">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1170e-125">xsd:string</span></span>  <br/> |<span data-ttu-id="1170e-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="1170e-126">optional</span></span>  <br/> ||<span data-ttu-id="1170e-127">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1170e-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1170e-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1170e-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="1170e-129">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1170e-129">xsd:string</span></span>  <br/> |<span data-ttu-id="1170e-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="1170e-130">optional</span></span>  <br/> ||<span data-ttu-id="1170e-131">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1170e-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1170e-132">FileName</span><span class="sxs-lookup"><span data-stu-id="1170e-132">FileName</span></span>  <br/> |<span data-ttu-id="1170e-133">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1170e-133">xsd:string</span></span>  <br/> |<span data-ttu-id="1170e-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1170e-134">required</span></span>  <br/> ||<span data-ttu-id="1170e-135">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1170e-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1170e-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="1170e-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="1170e-137">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="1170e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="1170e-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="1170e-138">optional</span></span>  <br/> ||<span data-ttu-id="1170e-139">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="1170e-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="1170e-140">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="1170e-140">ID</span></span>  <br/> |<span data-ttu-id="1170e-141">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="1170e-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1170e-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="1170e-142">required</span></span>  <br/> ||<span data-ttu-id="1170e-143">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="1170e-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1170e-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="1170e-144">Timeout</span></span>  <br/> |<span data-ttu-id="1170e-145">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="1170e-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1170e-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="1170e-146">optional</span></span>  <br/> ||<span data-ttu-id="1170e-147">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="1170e-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

