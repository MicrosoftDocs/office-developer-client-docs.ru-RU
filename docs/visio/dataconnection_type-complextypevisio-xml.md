---
title: DataConnection_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389143"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="2e002-102">DataConnection_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="2e002-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2e002-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="2e002-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2e002-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="2e002-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2e002-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="2e002-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2e002-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2e002-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2e002-107">**Базовый элемент расширения**</span><span class="sxs-lookup"><span data-stu-id="2e002-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2e002-108">Отсутствует</span><span class="sxs-lookup"><span data-stu-id="2e002-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2e002-109">Определение</span><span class="sxs-lookup"><span data-stu-id="2e002-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2e002-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="2e002-110">Elements and attributes</span></span>

<span data-ttu-id="2e002-111">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="2e002-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2e002-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2e002-112">Child elements</span></span>

<span data-ttu-id="2e002-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="2e002-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2e002-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2e002-114">Attributes</span></span>

|<span data-ttu-id="2e002-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="2e002-115">**Attribute**</span></span>|<span data-ttu-id="2e002-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="2e002-116">**Type**</span></span>|<span data-ttu-id="2e002-117">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="2e002-117">**Required**</span></span>|<span data-ttu-id="2e002-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2e002-118">**Description**</span></span>|<span data-ttu-id="2e002-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="2e002-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2e002-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="2e002-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="2e002-121">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="2e002-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2e002-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="2e002-122">optional</span></span>  <br/> ||<span data-ttu-id="2e002-123">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2e002-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2e002-124">Команда</span><span class="sxs-lookup"><span data-stu-id="2e002-124">Command</span></span>  <br/> |<span data-ttu-id="2e002-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="2e002-125">xsd:string</span></span>  <br/> |<span data-ttu-id="2e002-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="2e002-126">optional</span></span>  <br/> ||<span data-ttu-id="2e002-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e002-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e002-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2e002-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="2e002-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="2e002-129">xsd:string</span></span>  <br/> |<span data-ttu-id="2e002-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="2e002-130">optional</span></span>  <br/> ||<span data-ttu-id="2e002-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e002-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e002-132">FileName</span><span class="sxs-lookup"><span data-stu-id="2e002-132">FileName</span></span>  <br/> |<span data-ttu-id="2e002-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="2e002-133">xsd:string</span></span>  <br/> |<span data-ttu-id="2e002-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2e002-134">required</span></span>  <br/> ||<span data-ttu-id="2e002-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e002-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e002-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2e002-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="2e002-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="2e002-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2e002-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="2e002-138">optional</span></span>  <br/> ||<span data-ttu-id="2e002-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="2e002-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="2e002-140">ID</span><span class="sxs-lookup"><span data-stu-id="2e002-140">ID</span></span>  <br/> |<span data-ttu-id="2e002-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2e002-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2e002-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2e002-142">required</span></span>  <br/> ||<span data-ttu-id="2e002-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2e002-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2e002-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="2e002-144">Timeout</span></span>  <br/> |<span data-ttu-id="2e002-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2e002-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2e002-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="2e002-146">optional</span></span>  <br/> ||<span data-ttu-id="2e002-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2e002-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

