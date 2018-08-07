---
title: DataConnection_Type complexType ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 3a900e22fd36c936f689081149b484bd5e7460fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813552"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a><span data-ttu-id="889eb-102">DataConnection_Type complexType ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="889eb-102">DataConnection_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="889eb-103">Сведения о типе</span><span class="sxs-lookup"><span data-stu-id="889eb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="889eb-104">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="889eb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="889eb-105">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="889eb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="889eb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="889eb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="889eb-107">**База расширения**</span><span class="sxs-lookup"><span data-stu-id="889eb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="889eb-108">Нет</span><span class="sxs-lookup"><span data-stu-id="889eb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="889eb-109">Определение</span><span class="sxs-lookup"><span data-stu-id="889eb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="889eb-110">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="889eb-110">Elements and attributes</span></span>

<span data-ttu-id="889eb-111">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="889eb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="889eb-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="889eb-112">Child elements</span></span>

<span data-ttu-id="889eb-113">Нет.</span><span class="sxs-lookup"><span data-stu-id="889eb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="889eb-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="889eb-114">Attributes</span></span>

|<span data-ttu-id="889eb-115">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="889eb-115">**Attribute**</span></span>|<span data-ttu-id="889eb-116">**Тип**</span><span class="sxs-lookup"><span data-stu-id="889eb-116">**Type**</span></span>|<span data-ttu-id="889eb-117">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="889eb-117">**Required**</span></span>|<span data-ttu-id="889eb-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="889eb-118">**Description**</span></span>|<span data-ttu-id="889eb-119">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="889eb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="889eb-120">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="889eb-120">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="889eb-121">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="889eb-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="889eb-122">необязательный</span><span class="sxs-lookup"><span data-stu-id="889eb-122">optional</span></span>  <br/> ||<span data-ttu-id="889eb-123">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="889eb-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="889eb-124">Команда</span><span class="sxs-lookup"><span data-stu-id="889eb-124">Command</span></span>  <br/> |<span data-ttu-id="889eb-125">XSD:String</span><span class="sxs-lookup"><span data-stu-id="889eb-125">xsd:string</span></span>  <br/> |<span data-ttu-id="889eb-126">необязательный</span><span class="sxs-lookup"><span data-stu-id="889eb-126">optional</span></span>  <br/> ||<span data-ttu-id="889eb-127">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="889eb-127">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="889eb-128">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="889eb-128">ConnectionString</span></span>  <br/> |<span data-ttu-id="889eb-129">XSD:String</span><span class="sxs-lookup"><span data-stu-id="889eb-129">xsd:string</span></span>  <br/> |<span data-ttu-id="889eb-130">необязательный</span><span class="sxs-lookup"><span data-stu-id="889eb-130">optional</span></span>  <br/> ||<span data-ttu-id="889eb-131">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="889eb-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="889eb-132">FileName</span><span class="sxs-lookup"><span data-stu-id="889eb-132">FileName</span></span>  <br/> |<span data-ttu-id="889eb-133">XSD:String</span><span class="sxs-lookup"><span data-stu-id="889eb-133">xsd:string</span></span>  <br/> |<span data-ttu-id="889eb-134">Обязательный</span><span class="sxs-lookup"><span data-stu-id="889eb-134">required</span></span>  <br/> ||<span data-ttu-id="889eb-135">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="889eb-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="889eb-136">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="889eb-136">FriendlyName</span></span>  <br/> |<span data-ttu-id="889eb-137">XSD:String</span><span class="sxs-lookup"><span data-stu-id="889eb-137">xsd:string</span></span>  <br/> |<span data-ttu-id="889eb-138">необязательный</span><span class="sxs-lookup"><span data-stu-id="889eb-138">optional</span></span>  <br/> ||<span data-ttu-id="889eb-139">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="889eb-139">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="889eb-140">ID</span><span class="sxs-lookup"><span data-stu-id="889eb-140">ID</span></span>  <br/> |<span data-ttu-id="889eb-141">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="889eb-141">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="889eb-142">Обязательный</span><span class="sxs-lookup"><span data-stu-id="889eb-142">required</span></span>  <br/> ||<span data-ttu-id="889eb-143">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="889eb-143">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="889eb-144">Timeout</span><span class="sxs-lookup"><span data-stu-id="889eb-144">Timeout</span></span>  <br/> |<span data-ttu-id="889eb-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="889eb-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="889eb-146">необязательный</span><span class="sxs-lookup"><span data-stu-id="889eb-146">optional</span></span>  <br/> ||<span data-ttu-id="889eb-147">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="889eb-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

