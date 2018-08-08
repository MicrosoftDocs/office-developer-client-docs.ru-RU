---
title: Элемент DataConnection (DataConnections_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Выделяет обмена данными между один или несколько элементов записей данных и источник данных не в формате XML.
ms.openlocfilehash: 74e15795e023517263d9b79e9f19557653e4e939
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813551"
---
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="35557-103">Элемент DataConnection (DataConnections_Type complexType) ('Visio XML»)</span><span class="sxs-lookup"><span data-stu-id="35557-103">DataConnection element (DataConnections_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="35557-104">Выделяет обмена данными между один или несколько элементов **записей данных** и источник данных не в формате XML.</span><span class="sxs-lookup"><span data-stu-id="35557-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="35557-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="35557-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="35557-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="35557-106">**Element type**</span></span> <br/> |[<span data-ttu-id="35557-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="35557-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="35557-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="35557-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="35557-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="35557-109">**Schema file**</span></span> <br/> |<span data-ttu-id="35557-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="35557-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="35557-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="35557-111">**Document parts**</span></span> <br/> |<span data-ttu-id="35557-112">Connections.XML</span><span class="sxs-lookup"><span data-stu-id="35557-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="35557-113">Определение</span><span class="sxs-lookup"><span data-stu-id="35557-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="35557-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="35557-114">Elements and attributes</span></span>

<span data-ttu-id="35557-115">Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение.</span><span class="sxs-lookup"><span data-stu-id="35557-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="35557-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="35557-116">Parent elements</span></span>

|<span data-ttu-id="35557-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="35557-117">**Element**</span></span>|<span data-ttu-id="35557-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="35557-118">**Type**</span></span>|<span data-ttu-id="35557-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35557-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="35557-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="35557-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="35557-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="35557-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="35557-122">Содержит элементы **подключение данных** для документа.</span><span class="sxs-lookup"><span data-stu-id="35557-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="35557-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="35557-123">Child elements</span></span>

<span data-ttu-id="35557-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="35557-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="35557-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="35557-125">Attributes</span></span>

|<span data-ttu-id="35557-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="35557-126">**Attribute**</span></span>|<span data-ttu-id="35557-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="35557-127">**Type**</span></span>|<span data-ttu-id="35557-128">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="35557-128">**Required**</span></span>|<span data-ttu-id="35557-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="35557-129">**Description**</span></span>|<span data-ttu-id="35557-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="35557-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="35557-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="35557-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="35557-132">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="35557-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="35557-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="35557-133">optional</span></span>  <br/> |<span data-ttu-id="35557-134">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="35557-134">The default value is false.</span></span> <span data-ttu-id="35557-135">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="35557-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="35557-136">Значения типа xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="35557-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="35557-137">Команда</span><span class="sxs-lookup"><span data-stu-id="35557-137">Command</span></span>  <br/> |<span data-ttu-id="35557-138">XSD:String</span><span class="sxs-lookup"><span data-stu-id="35557-138">xsd:string</span></span>  <br/> |<span data-ttu-id="35557-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="35557-139">optional</span></span>  <br/> |<span data-ttu-id="35557-140">Командную строку, используемую для запроса источника данных.</span><span class="sxs-lookup"><span data-stu-id="35557-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="35557-141">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="35557-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35557-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="35557-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="35557-143">XSD:String</span><span class="sxs-lookup"><span data-stu-id="35557-143">xsd:string</span></span>  <br/> |<span data-ttu-id="35557-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="35557-144">optional</span></span>  <br/> |<span data-ttu-id="35557-145">Строка подключения, который определяет параметры, необходимые для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="35557-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="35557-146">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="35557-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35557-147">FileName</span><span class="sxs-lookup"><span data-stu-id="35557-147">FileName</span></span>  <br/> |<span data-ttu-id="35557-148">XSD:String</span><span class="sxs-lookup"><span data-stu-id="35557-148">xsd:string</span></span>  <br/> |<span data-ttu-id="35557-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35557-149">required</span></span>  <br/> |<span data-ttu-id="35557-150">Имя файла подключения.</span><span class="sxs-lookup"><span data-stu-id="35557-150">The name of the connection file.</span></span> <span data-ttu-id="35557-151">Для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="35557-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="35557-152">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="35557-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35557-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="35557-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="35557-154">XSD:String</span><span class="sxs-lookup"><span data-stu-id="35557-154">xsd:string</span></span>  <br/> |<span data-ttu-id="35557-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="35557-155">optional</span></span>  <br/> |<span data-ttu-id="35557-156">Предоставляются имя пользователя для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="35557-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="35557-157">Значения типа xsd:string.</span><span class="sxs-lookup"><span data-stu-id="35557-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="35557-158">ID</span><span class="sxs-lookup"><span data-stu-id="35557-158">ID</span></span>  <br/> |<span data-ttu-id="35557-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="35557-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="35557-160">Обязательный</span><span class="sxs-lookup"><span data-stu-id="35557-160">required</span></span>  <br/> |<span data-ttu-id="35557-161">Идентификатор, назначенный с Visio для данного подключения, уникальные в документе.</span><span class="sxs-lookup"><span data-stu-id="35557-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="35557-162">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="35557-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="35557-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="35557-163">Timeout</span></span>  <br/> |<span data-ttu-id="35557-164">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="35557-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="35557-165">необязательный</span><span class="sxs-lookup"><span data-stu-id="35557-165">optional</span></span>  <br/> |<span data-ttu-id="35557-166">Время ожидания в минутах при попытке установить подключение завершается.</span><span class="sxs-lookup"><span data-stu-id="35557-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="35557-167">Значения типа xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="35557-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

