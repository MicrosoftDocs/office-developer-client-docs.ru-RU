---
title: Элемент DataConnections (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Содержит элементы DataConnection для документа.
ms.openlocfilehash: 5d45d1dcd76524c2144336235e8277cd51f8a138
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539184"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="46afd-103">Элемент DataConnections (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="46afd-103">DataConnections element (Visio XML)</span></span>

<span data-ttu-id="46afd-104">Содержит **элементы DataConnection** для документа.</span><span class="sxs-lookup"><span data-stu-id="46afd-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="46afd-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="46afd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46afd-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="46afd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="46afd-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="46afd-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="46afd-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="46afd-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="46afd-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="46afd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="46afd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="46afd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="46afd-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="46afd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="46afd-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="46afd-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="46afd-113">Определение</span><span class="sxs-lookup"><span data-stu-id="46afd-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="46afd-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="46afd-114">Elements and attributes</span></span>

<span data-ttu-id="46afd-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="46afd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="46afd-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="46afd-116">Parent elements</span></span>

<span data-ttu-id="46afd-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="46afd-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46afd-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="46afd-118">Child elements</span></span>

|<span data-ttu-id="46afd-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="46afd-119">**Element**</span></span>|<span data-ttu-id="46afd-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="46afd-120">**Type**</span></span>|<span data-ttu-id="46afd-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46afd-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="46afd-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="46afd-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="46afd-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="46afd-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="46afd-124">Аннотация связи между одним или более **элементами DataRecordset** и источником данных, не относя к XML.</span><span class="sxs-lookup"><span data-stu-id="46afd-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="46afd-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="46afd-125">Attributes</span></span>

|<span data-ttu-id="46afd-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="46afd-126">**Attribute**</span></span>|<span data-ttu-id="46afd-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="46afd-127">**Type**</span></span>|<span data-ttu-id="46afd-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="46afd-128">**Required**</span></span>|<span data-ttu-id="46afd-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46afd-129">**Description**</span></span>|<span data-ttu-id="46afd-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="46afd-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="46afd-131">NextID</span><span class="sxs-lookup"><span data-stu-id="46afd-131">NextID</span></span>  <br/> |<span data-ttu-id="46afd-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="46afd-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="46afd-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="46afd-133">required</span></span>  <br/> |<span data-ttu-id="46afd-134">Следующий доступный ID для новых подключений.</span><span class="sxs-lookup"><span data-stu-id="46afd-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="46afd-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="46afd-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

