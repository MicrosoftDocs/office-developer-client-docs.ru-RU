---
title: Элемент DataConnections ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3cac0cd0-87ff-8c82-2d33-20070a505f4e
description: Содержит элементы подключение данных для документа.
ms.openlocfilehash: 4de4429985ab0417341224f7f9e267a9873c6504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813541"
---
# <a name="dataconnections-element-visio-xml"></a><span data-ttu-id="4205a-103">Элемент DataConnections ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="4205a-103">DataConnections element ('Visio XML')</span></span>

<span data-ttu-id="4205a-104">Содержит элементы **подключение данных** для документа.</span><span class="sxs-lookup"><span data-stu-id="4205a-104">Contains the **DataConnection** elements for the document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="4205a-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="4205a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4205a-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="4205a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4205a-107">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="4205a-107">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4205a-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="4205a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4205a-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="4205a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4205a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4205a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4205a-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="4205a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4205a-112">Connections.XML</span><span class="sxs-lookup"><span data-stu-id="4205a-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4205a-113">Определение</span><span class="sxs-lookup"><span data-stu-id="4205a-113">Definition</span></span>

```XML
< xs:element name="DataConnections" type="DataConnections_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4205a-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="4205a-114">Elements and attributes</span></span>

<span data-ttu-id="4205a-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="4205a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4205a-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="4205a-116">Parent elements</span></span>

<span data-ttu-id="4205a-117">Нет.</span><span class="sxs-lookup"><span data-stu-id="4205a-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4205a-118">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4205a-118">Child elements</span></span>

|<span data-ttu-id="4205a-119">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="4205a-119">**Element**</span></span>|<span data-ttu-id="4205a-120">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4205a-120">**Type**</span></span>|<span data-ttu-id="4205a-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4205a-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4205a-122">Подключение данных</span><span class="sxs-lookup"><span data-stu-id="4205a-122">DataConnection</span></span>](dataconnection-element-dataconnections_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4205a-123">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="4205a-123">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4205a-124">Выделяет обмена данными между один или несколько элементов **записей данных** и источник данных не в формате XML.</span><span class="sxs-lookup"><span data-stu-id="4205a-124">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="4205a-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="4205a-125">Attributes</span></span>

|<span data-ttu-id="4205a-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="4205a-126">**Attribute**</span></span>|<span data-ttu-id="4205a-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4205a-127">**Type**</span></span>|<span data-ttu-id="4205a-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="4205a-128">**Required**</span></span>|<span data-ttu-id="4205a-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4205a-129">**Description**</span></span>|<span data-ttu-id="4205a-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="4205a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4205a-131">NextID</span><span class="sxs-lookup"><span data-stu-id="4205a-131">NextID</span></span>  <br/> |<span data-ttu-id="4205a-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4205a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4205a-133">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4205a-133">required</span></span>  <br/> |<span data-ttu-id="4205a-134">Идентификатор следующего недоступны для новых подключений.</span><span class="sxs-lookup"><span data-stu-id="4205a-134">The next available ID for new connections.</span></span>  <br/> |<span data-ttu-id="4205a-135">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4205a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

