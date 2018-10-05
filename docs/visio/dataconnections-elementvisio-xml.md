---
title: Элемент DataConnections ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Содержит элементы подключение данных для документа.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395030"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="f6bc9-103">Элемент DataConnections ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="f6bc9-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="f6bc9-104">Содержит элементы **подключение данных** для документа.</span><span class="sxs-lookup"><span data-stu-id="f6bc9-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="f6bc9-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f6bc9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f6bc9-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f6bc9-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="f6bc9-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f6bc9-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f6bc9-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f6bc9-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f6bc9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f6bc9-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f6bc9-112">Connections.XML</span><span class="sxs-lookup"><span data-stu-id="f6bc9-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f6bc9-113">Определение</span><span class="sxs-lookup"><span data-stu-id="f6bc9-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f6bc9-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="f6bc9-114">Elements and attributes</span></span>

<span data-ttu-id="f6bc9-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="f6bc9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f6bc9-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="f6bc9-116">Parent elements</span></span>

<span data-ttu-id="f6bc9-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="f6bc9-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f6bc9-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f6bc9-118">Child elements</span></span>

|<span data-ttu-id="f6bc9-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-119">**Element**</span></span>|<span data-ttu-id="f6bc9-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-120">**Type**</span></span>|<span data-ttu-id="f6bc9-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f6bc9-122">Подключение данных</span><span class="sxs-lookup"><span data-stu-id="f6bc9-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f6bc9-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="f6bc9-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f6bc9-124">Выделяет обмена данными между один или несколько элементов **записей данных** и источник данных не в формате XML.</span><span class="sxs-lookup"><span data-stu-id="f6bc9-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="f6bc9-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="f6bc9-125">Attributes</span></span>

|<span data-ttu-id="f6bc9-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-126">**Attribute**</span></span>|<span data-ttu-id="f6bc9-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-127">**Type**</span></span>|<span data-ttu-id="f6bc9-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-128">**Required**</span></span>|<span data-ttu-id="f6bc9-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-129">**Description**</span></span>|<span data-ttu-id="f6bc9-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="f6bc9-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f6bc9-131">NextID</span><span class="sxs-lookup"><span data-stu-id="f6bc9-131">NextID</span></span>  <br/> |<span data-ttu-id="f6bc9-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f6bc9-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f6bc9-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f6bc9-133">required</span></span>  <br/> |<span data-ttu-id="f6bc9-134">Идентификатор следующего недоступны для новых подключений.</span><span class="sxs-lookup"><span data-stu-id="f6bc9-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="f6bc9-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f6bc9-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

