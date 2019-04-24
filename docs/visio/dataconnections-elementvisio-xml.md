---
title: Элемент Connections ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Содержит элементы подключения к документу.
ms.openlocfilehash: 5b1619253a2818f2a181d281c78a0445318ed6ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344494"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="5ee3f-103">Элемент Connections ("Visio XML")</span><span class="sxs-lookup"><span data-stu-id="5ee3f-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="5ee3f-104">Содержит элементы **подключения** к документу.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="5ee3f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5ee3f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ee3f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="5ee3f-107">Датаконнектионс_типе</span><span class="sxs-lookup"><span data-stu-id="5ee3f-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="5ee3f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="5ee3f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="5ee3f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="5ee3f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="5ee3f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="5ee3f-112">Connections. XML</span><span class="sxs-lookup"><span data-stu-id="5ee3f-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="5ee3f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="5ee3f-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="5ee3f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="5ee3f-114">Elements and attributes</span></span>

<span data-ttu-id="5ee3f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="5ee3f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="5ee3f-116">Parent elements</span></span>

<span data-ttu-id="5ee3f-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5ee3f-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5ee3f-118">Child elements</span></span>

|<span data-ttu-id="5ee3f-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-119">**Element**</span></span>|<span data-ttu-id="5ee3f-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-120">**Type**</span></span>|<span data-ttu-id="5ee3f-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="5ee3f-122">DataConnection</span><span class="sxs-lookup"><span data-stu-id="5ee3f-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="5ee3f-123">Датаконнектион_типе</span><span class="sxs-lookup"><span data-stu-id="5ee3f-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="5ee3f-124">Создает абстракцию для связи между одним или несколькими элементами **записи** данных и источником данных, не относящимся к XML.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="5ee3f-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5ee3f-125">Attributes</span></span>

|<span data-ttu-id="5ee3f-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-126">**Attribute**</span></span>|<span data-ttu-id="5ee3f-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-127">**Type**</span></span>|<span data-ttu-id="5ee3f-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-128">**Required**</span></span>|<span data-ttu-id="5ee3f-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-129">**Description**</span></span>|<span data-ttu-id="5ee3f-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="5ee3f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5ee3f-131">Некстид</span><span class="sxs-lookup"><span data-stu-id="5ee3f-131">NextID</span></span>  <br/> |<span data-ttu-id="5ee3f-132">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="5ee3f-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="5ee3f-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="5ee3f-133">required</span></span>  <br/> |<span data-ttu-id="5ee3f-134">Следующий доступный идентификатор для новых подключений.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="5ee3f-135">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="5ee3f-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

