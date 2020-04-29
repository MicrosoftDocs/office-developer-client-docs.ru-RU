---
title: Элемент Connection (DataConnections_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aab8be3-b236-029b-1df3-b6860d4f4586
description: Создает абстракцию для связи между одним или несколькими элементами записи данных и источником данных, не относящимся к XML.
ms.openlocfilehash: 619f3b4e3d9c93831cc23bc38fba3670107b2b51
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538405"
---
# <a name="dataconnection-element-dataconnections_type-complextype-visio-xml"></a><span data-ttu-id="6b62f-103">Элемент Connection (DataConnections_Type complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="6b62f-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="6b62f-104">Создает абстракцию для связи между одним или несколькими элементами **записи** данных и источником данных, не относящимся к XML.</span><span class="sxs-lookup"><span data-stu-id="6b62f-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="6b62f-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6b62f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b62f-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="6b62f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6b62f-107">DataConnection_Type</span><span class="sxs-lookup"><span data-stu-id="6b62f-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="6b62f-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="6b62f-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="6b62f-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="6b62f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6b62f-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="6b62f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="6b62f-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="6b62f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="6b62f-112">Connections. XML</span><span class="sxs-lookup"><span data-stu-id="6b62f-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6b62f-113">Определение</span><span class="sxs-lookup"><span data-stu-id="6b62f-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6b62f-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b62f-114">Elements and attributes</span></span>

<span data-ttu-id="6b62f-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="6b62f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6b62f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6b62f-116">Parent elements</span></span>

|<span data-ttu-id="6b62f-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6b62f-117">**Element**</span></span>|<span data-ttu-id="6b62f-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b62f-118">**Type**</span></span>|<span data-ttu-id="6b62f-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b62f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6b62f-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="6b62f-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="6b62f-121">DataConnections_Type</span><span class="sxs-lookup"><span data-stu-id="6b62f-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="6b62f-122">Содержит элементы **подключения** к документу.</span><span class="sxs-lookup"><span data-stu-id="6b62f-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6b62f-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6b62f-123">Child elements</span></span>

<span data-ttu-id="6b62f-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="6b62f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b62f-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6b62f-125">Attributes</span></span>

|<span data-ttu-id="6b62f-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="6b62f-126">**Attribute**</span></span>|<span data-ttu-id="6b62f-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="6b62f-127">**Type**</span></span>|<span data-ttu-id="6b62f-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="6b62f-128">**Required**</span></span>|<span data-ttu-id="6b62f-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6b62f-129">**Description**</span></span>|<span data-ttu-id="6b62f-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="6b62f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6b62f-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="6b62f-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="6b62f-132">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="6b62f-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6b62f-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b62f-133">optional</span></span>  <br/> |<span data-ttu-id="6b62f-134">Значение по умолчанию  false.</span><span class="sxs-lookup"><span data-stu-id="6b62f-134">The default value is false.</span></span> <span data-ttu-id="6b62f-135">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="6b62f-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="6b62f-136">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="6b62f-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6b62f-137">Command</span><span class="sxs-lookup"><span data-stu-id="6b62f-137">Command</span></span>  <br/> |<span data-ttu-id="6b62f-138">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="6b62f-138">xsd:string</span></span>  <br/> |<span data-ttu-id="6b62f-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b62f-139">optional</span></span>  <br/> |<span data-ttu-id="6b62f-140">Командная строка, используемая для запроса к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="6b62f-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="6b62f-141">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="6b62f-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b62f-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="6b62f-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="6b62f-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="6b62f-143">xsd:string</span></span>  <br/> |<span data-ttu-id="6b62f-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b62f-144">optional</span></span>  <br/> |<span data-ttu-id="6b62f-145">Строка подключения, определяющая параметры, необходимые для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="6b62f-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="6b62f-146">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="6b62f-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b62f-147">FileName</span><span class="sxs-lookup"><span data-stu-id="6b62f-147">FileName</span></span>  <br/> |<span data-ttu-id="6b62f-148">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="6b62f-148">xsd:string</span></span>  <br/> |<span data-ttu-id="6b62f-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b62f-149">required</span></span>  <br/> |<span data-ttu-id="6b62f-150">Имя файла подключения.</span><span class="sxs-lookup"><span data-stu-id="6b62f-150">The name of the connection file.</span></span> <span data-ttu-id="6b62f-151">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="6b62f-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="6b62f-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="6b62f-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b62f-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b62f-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="6b62f-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="6b62f-154">xsd:string</span></span>  <br/> |<span data-ttu-id="6b62f-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b62f-155">optional</span></span>  <br/> |<span data-ttu-id="6b62f-156">Имя, указанное пользователем для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="6b62f-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="6b62f-157">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="6b62f-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6b62f-158">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="6b62f-158">ID</span></span>  <br/> |<span data-ttu-id="6b62f-159">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="6b62f-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b62f-160">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6b62f-160">required</span></span>  <br/> |<span data-ttu-id="6b62f-161">Идентификатор, назначенный Visio для данного подключения, уникальный в пределах документа.</span><span class="sxs-lookup"><span data-stu-id="6b62f-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="6b62f-162">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="6b62f-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6b62f-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="6b62f-163">Timeout</span></span>  <br/> |<span data-ttu-id="6b62f-164">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="6b62f-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6b62f-165">необязательный</span><span class="sxs-lookup"><span data-stu-id="6b62f-165">optional</span></span>  <br/> |<span data-ttu-id="6b62f-166">Время ожидания в минутах при попытке установить подключение перед завершением попытки.</span><span class="sxs-lookup"><span data-stu-id="6b62f-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="6b62f-167">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="6b62f-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

