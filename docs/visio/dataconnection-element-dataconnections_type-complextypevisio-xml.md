---
title: Элемент DataConnection (DataConnections_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Аннотация связи между одним или более элементами DataRecordset и источником данных, не относя к XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538405"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="e9fae-103">Элемент DataConnection (DataConnections_Type ComplexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e9fae-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="e9fae-104">Аннотация связи между одним или более **элементами DataRecordset** и источником данных, не относя к XML.</span><span class="sxs-lookup"><span data-stu-id="e9fae-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e9fae-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e9fae-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e9fae-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="e9fae-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e9fae-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="e9fae-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e9fae-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="e9fae-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e9fae-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="e9fae-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e9fae-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e9fae-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e9fae-111">**Части документов**</span><span class="sxs-lookup"><span data-stu-id="e9fae-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e9fae-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="e9fae-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e9fae-113">Определение</span><span class="sxs-lookup"><span data-stu-id="e9fae-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e9fae-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="e9fae-114">Elements and attributes</span></span>

<span data-ttu-id="e9fae-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="e9fae-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e9fae-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="e9fae-116">Parent elements</span></span>

|<span data-ttu-id="e9fae-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e9fae-117">**Element**</span></span>|<span data-ttu-id="e9fae-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e9fae-118">**Type**</span></span>|<span data-ttu-id="e9fae-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9fae-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e9fae-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="e9fae-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="e9fae-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="e9fae-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e9fae-122">Содержит **элементы DataConnection** для документа.</span><span class="sxs-lookup"><span data-stu-id="e9fae-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e9fae-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e9fae-123">Child elements</span></span>

<span data-ttu-id="e9fae-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="e9fae-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e9fae-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e9fae-125">Attributes</span></span>

|<span data-ttu-id="e9fae-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="e9fae-126">**Attribute**</span></span>|<span data-ttu-id="e9fae-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="e9fae-127">**Type**</span></span>|<span data-ttu-id="e9fae-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="e9fae-128">**Required**</span></span>|<span data-ttu-id="e9fae-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e9fae-129">**Description**</span></span>|<span data-ttu-id="e9fae-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="e9fae-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e9fae-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="e9fae-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="e9fae-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="e9fae-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e9fae-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9fae-133">optional</span></span>  <br/> |<span data-ttu-id="e9fae-134">Значение по умолчанию  false.</span><span class="sxs-lookup"><span data-stu-id="e9fae-134">The default value is false.</span></span> <span data-ttu-id="e9fae-135">Дополнительные сведения см. в комментарии.</span><span class="sxs-lookup"><span data-stu-id="e9fae-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="e9fae-136">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e9fae-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e9fae-137">Команда</span><span class="sxs-lookup"><span data-stu-id="e9fae-137">Command</span></span>  <br/> |<span data-ttu-id="e9fae-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9fae-138">xsd:string</span></span>  <br/> |<span data-ttu-id="e9fae-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9fae-139">optional</span></span>  <br/> |<span data-ttu-id="e9fae-140">Строка команд, используемая для запроса источника данных.</span><span class="sxs-lookup"><span data-stu-id="e9fae-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="e9fae-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e9fae-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e9fae-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e9fae-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="e9fae-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9fae-143">xsd:string</span></span>  <br/> |<span data-ttu-id="e9fae-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9fae-144">optional</span></span>  <br/> |<span data-ttu-id="e9fae-145">Строка подключения, определяемая параметрами, необходимыми для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="e9fae-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="e9fae-146">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e9fae-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e9fae-147">FileName</span><span class="sxs-lookup"><span data-stu-id="e9fae-147">FileName</span></span>  <br/> |<span data-ttu-id="e9fae-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9fae-148">xsd:string</span></span>  <br/> |<span data-ttu-id="e9fae-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9fae-149">required</span></span>  <br/> |<span data-ttu-id="e9fae-150">Имя файла подключения.</span><span class="sxs-lookup"><span data-stu-id="e9fae-150">The name of the connection file.</span></span> <span data-ttu-id="e9fae-151">Дополнительные сведения см. в комментарии.</span><span class="sxs-lookup"><span data-stu-id="e9fae-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="e9fae-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e9fae-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e9fae-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e9fae-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="e9fae-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="e9fae-154">xsd:string</span></span>  <br/> |<span data-ttu-id="e9fae-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9fae-155">optional</span></span>  <br/> |<span data-ttu-id="e9fae-156">Пользователь предоставил имя для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="e9fae-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="e9fae-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="e9fae-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="e9fae-158">ID</span><span class="sxs-lookup"><span data-stu-id="e9fae-158">ID</span></span>  <br/> |<span data-ttu-id="e9fae-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9fae-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9fae-160">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e9fae-160">required</span></span>  <br/> |<span data-ttu-id="e9fae-161">ID, заданный Visio для данного подключения, уникального в документе.</span><span class="sxs-lookup"><span data-stu-id="e9fae-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="e9fae-162">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9fae-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e9fae-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="e9fae-163">Timeout</span></span>  <br/> |<span data-ttu-id="e9fae-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e9fae-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e9fae-165">необязательный</span><span class="sxs-lookup"><span data-stu-id="e9fae-165">optional</span></span>  <br/> |<span data-ttu-id="e9fae-166">Время ожидания в минутах при попытке установить подключение перед прекращением попытки.</span><span class="sxs-lookup"><span data-stu-id="e9fae-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="e9fae-167">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e9fae-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

