---
title: Элемент DataConnection (DataConnections_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Абстрагировать связь между одним или более элементами DataRecordset и источником данных, не относяющимися к XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538405"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="188c5-103">Элемент DataConnection (DataConnections_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="188c5-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="188c5-104">Абстрагировать связь между одним или более **элементами DataRecordset** и источником данных, не относяющимися к XML.</span><span class="sxs-lookup"><span data-stu-id="188c5-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="188c5-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="188c5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="188c5-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="188c5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="188c5-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="188c5-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="188c5-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="188c5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="188c5-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="188c5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="188c5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="188c5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="188c5-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="188c5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="188c5-112">connections.xml</span><span class="sxs-lookup"><span data-stu-id="188c5-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="188c5-113">Определение</span><span class="sxs-lookup"><span data-stu-id="188c5-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="188c5-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="188c5-114">Elements and attributes</span></span>

<span data-ttu-id="188c5-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="188c5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="188c5-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="188c5-116">Parent elements</span></span>

|<span data-ttu-id="188c5-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="188c5-117">**Element**</span></span>|<span data-ttu-id="188c5-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="188c5-118">**Type**</span></span>|<span data-ttu-id="188c5-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="188c5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="188c5-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="188c5-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="188c5-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="188c5-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="188c5-122">Содержит элементы **DataConnection** для документа.</span><span class="sxs-lookup"><span data-stu-id="188c5-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="188c5-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="188c5-123">Child elements</span></span>

<span data-ttu-id="188c5-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="188c5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="188c5-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="188c5-125">Attributes</span></span>

|<span data-ttu-id="188c5-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="188c5-126">**Attribute**</span></span>|<span data-ttu-id="188c5-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="188c5-127">**Type**</span></span>|<span data-ttu-id="188c5-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="188c5-128">**Required**</span></span>|<span data-ttu-id="188c5-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="188c5-129">**Description**</span></span>|<span data-ttu-id="188c5-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="188c5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="188c5-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="188c5-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="188c5-132">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="188c5-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="188c5-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="188c5-133">optional</span></span>  <br/> |<span data-ttu-id="188c5-134">Значение по умолчанию  false.</span><span class="sxs-lookup"><span data-stu-id="188c5-134">The default value is false.</span></span> <span data-ttu-id="188c5-135">Дополнительные сведения см. в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="188c5-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="188c5-136">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="188c5-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="188c5-137">Команда</span><span class="sxs-lookup"><span data-stu-id="188c5-137">Command</span></span>  <br/> |<span data-ttu-id="188c5-138">xsd:string</span><span class="sxs-lookup"><span data-stu-id="188c5-138">xsd:string</span></span>  <br/> |<span data-ttu-id="188c5-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="188c5-139">optional</span></span>  <br/> |<span data-ttu-id="188c5-140">Строка команды, используемая для запроса источника данных.</span><span class="sxs-lookup"><span data-stu-id="188c5-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="188c5-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="188c5-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="188c5-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="188c5-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="188c5-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="188c5-143">xsd:string</span></span>  <br/> |<span data-ttu-id="188c5-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="188c5-144">optional</span></span>  <br/> |<span data-ttu-id="188c5-145">Строка подключения, которая определяет параметры, необходимые для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="188c5-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="188c5-146">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="188c5-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="188c5-147">FileName</span><span class="sxs-lookup"><span data-stu-id="188c5-147">FileName</span></span>  <br/> |<span data-ttu-id="188c5-148">xsd:string</span><span class="sxs-lookup"><span data-stu-id="188c5-148">xsd:string</span></span>  <br/> |<span data-ttu-id="188c5-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="188c5-149">required</span></span>  <br/> |<span data-ttu-id="188c5-150">Имя файла подключения.</span><span class="sxs-lookup"><span data-stu-id="188c5-150">The name of the connection file.</span></span> <span data-ttu-id="188c5-151">Дополнительные сведения см. в примечаиях.</span><span class="sxs-lookup"><span data-stu-id="188c5-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="188c5-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="188c5-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="188c5-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="188c5-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="188c5-154">xsd:string</span><span class="sxs-lookup"><span data-stu-id="188c5-154">xsd:string</span></span>  <br/> |<span data-ttu-id="188c5-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="188c5-155">optional</span></span>  <br/> |<span data-ttu-id="188c5-156">Имя, предоставленное пользователем для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="188c5-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="188c5-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="188c5-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="188c5-158">ID</span><span class="sxs-lookup"><span data-stu-id="188c5-158">ID</span></span>  <br/> |<span data-ttu-id="188c5-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="188c5-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="188c5-160">Обязательный</span><span class="sxs-lookup"><span data-stu-id="188c5-160">required</span></span>  <br/> |<span data-ttu-id="188c5-161">ИД, присвоенный Visio для заданного подключения, уникальный в документе.</span><span class="sxs-lookup"><span data-stu-id="188c5-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="188c5-162">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="188c5-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="188c5-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="188c5-163">Timeout</span></span>  <br/> |<span data-ttu-id="188c5-164">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="188c5-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="188c5-165">необязательный</span><span class="sxs-lookup"><span data-stu-id="188c5-165">optional</span></span>  <br/> |<span data-ttu-id="188c5-166">Время ожидания в минутах при попытке установить подключение перед прерыванием попытки.</span><span class="sxs-lookup"><span data-stu-id="188c5-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="188c5-167">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="188c5-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

