---
title: Элемент DataConnection (DataConnections_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Выделяет обмена данными между один или несколько элементов записей данных и источник данных не в формате XML.
ms.openlocfilehash: 0073c329ec9149263530421531522c4d0b95633d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399426"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="51af1-103">Элемент DataConnection (DataConnections_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="51af1-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="51af1-104">Выделяет обмена данными между один или несколько элементов **записей данных** и источник данных не в формате XML.</span><span class="sxs-lookup"><span data-stu-id="51af1-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="51af1-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="51af1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="51af1-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="51af1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="51af1-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="51af1-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="51af1-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="51af1-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="51af1-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="51af1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="51af1-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="51af1-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="51af1-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="51af1-111">**Document parts**</span></span> <br/> |<span data-ttu-id="51af1-112">Connections.XML</span><span class="sxs-lookup"><span data-stu-id="51af1-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="51af1-113">Определение</span><span class="sxs-lookup"><span data-stu-id="51af1-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="51af1-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="51af1-114">Elements and attributes</span></span>

<span data-ttu-id="51af1-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="51af1-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="51af1-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="51af1-116">Parent elements</span></span>

|<span data-ttu-id="51af1-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="51af1-117">**Element**</span></span>|<span data-ttu-id="51af1-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="51af1-118">**Type**</span></span>|<span data-ttu-id="51af1-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51af1-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="51af1-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="51af1-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="51af1-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="51af1-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="51af1-122">Содержит элементы **подключение данных** для документа.</span><span class="sxs-lookup"><span data-stu-id="51af1-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="51af1-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="51af1-123">Child elements</span></span>

<span data-ttu-id="51af1-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="51af1-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="51af1-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="51af1-125">Attributes</span></span>

|<span data-ttu-id="51af1-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="51af1-126">**Attribute**</span></span>|<span data-ttu-id="51af1-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="51af1-127">**Type**</span></span>|<span data-ttu-id="51af1-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="51af1-128">**Required**</span></span>|<span data-ttu-id="51af1-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="51af1-129">**Description**</span></span>|<span data-ttu-id="51af1-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="51af1-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="51af1-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="51af1-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="51af1-132">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="51af1-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="51af1-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="51af1-133">optional</span></span>  <br/> |<span data-ttu-id="51af1-134">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="51af1-134">The default value is false.</span></span> <span data-ttu-id="51af1-135">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="51af1-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="51af1-136">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="51af1-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="51af1-137">Команда</span><span class="sxs-lookup"><span data-stu-id="51af1-137">Command</span></span>  <br/> |<span data-ttu-id="51af1-138">XSD:String</span><span class="sxs-lookup"><span data-stu-id="51af1-138">xsd:string</span></span>  <br/> |<span data-ttu-id="51af1-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="51af1-139">optional</span></span>  <br/> |<span data-ttu-id="51af1-140">Командную строку, используемую для запроса источника данных.</span><span class="sxs-lookup"><span data-stu-id="51af1-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="51af1-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="51af1-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="51af1-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="51af1-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="51af1-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="51af1-143">xsd:string</span></span>  <br/> |<span data-ttu-id="51af1-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="51af1-144">optional</span></span>  <br/> |<span data-ttu-id="51af1-145">Строка подключения, который определяет параметры, необходимые для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="51af1-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="51af1-146">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="51af1-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="51af1-147">FileName</span><span class="sxs-lookup"><span data-stu-id="51af1-147">FileName</span></span>  <br/> |<span data-ttu-id="51af1-148">XSD:String</span><span class="sxs-lookup"><span data-stu-id="51af1-148">xsd:string</span></span>  <br/> |<span data-ttu-id="51af1-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51af1-149">required</span></span>  <br/> |<span data-ttu-id="51af1-150">Имя файла подключения.</span><span class="sxs-lookup"><span data-stu-id="51af1-150">The name of the connection file.</span></span> <span data-ttu-id="51af1-151">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="51af1-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="51af1-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="51af1-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="51af1-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="51af1-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="51af1-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="51af1-154">xsd:string</span></span>  <br/> |<span data-ttu-id="51af1-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="51af1-155">optional</span></span>  <br/> |<span data-ttu-id="51af1-156">Предоставляются имя пользователя для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="51af1-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="51af1-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="51af1-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="51af1-158">ID</span><span class="sxs-lookup"><span data-stu-id="51af1-158">ID</span></span>  <br/> |<span data-ttu-id="51af1-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="51af1-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="51af1-160">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51af1-160">required</span></span>  <br/> |<span data-ttu-id="51af1-161">Идентификатор, назначенный с Visio для данного подключения, уникальные в документе.</span><span class="sxs-lookup"><span data-stu-id="51af1-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="51af1-162">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="51af1-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="51af1-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="51af1-163">Timeout</span></span>  <br/> |<span data-ttu-id="51af1-164">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="51af1-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="51af1-165">необязательный</span><span class="sxs-lookup"><span data-stu-id="51af1-165">optional</span></span>  <br/> |<span data-ttu-id="51af1-166">Время ожидания в минутах при попытке установить подключение завершается.</span><span class="sxs-lookup"><span data-stu-id="51af1-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="51af1-167">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="51af1-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

