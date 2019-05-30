---
title: Элемент Connection (Датаконнектионс_типе complexType) (XML для Visio)
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
# <a name="dataconnection-element-dataconnectionstype-complextype-visio-xml"></a><span data-ttu-id="b7bef-103">Элемент Connection (Датаконнектионс_типе complexType) (XML для Visio)</span><span class="sxs-lookup"><span data-stu-id="b7bef-103">DataConnection element (DataConnections_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="b7bef-104">Создает абстракцию для связи между одним или несколькими элементами **записи** данных и источником данных, не относящимся к XML.</span><span class="sxs-lookup"><span data-stu-id="b7bef-104">Abstracts communication between one or more **DataRecordset** elements and a non-XML data source.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="b7bef-105">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b7bef-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b7bef-106">**Тип элемента**</span><span class="sxs-lookup"><span data-stu-id="b7bef-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b7bef-107">Датаконнектион_типе</span><span class="sxs-lookup"><span data-stu-id="b7bef-107">DataConnection_Type</span></span>](dataconnection_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b7bef-108">**Пространство имен**</span><span class="sxs-lookup"><span data-stu-id="b7bef-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b7bef-109">**Файл схемы**</span><span class="sxs-lookup"><span data-stu-id="b7bef-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b7bef-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="b7bef-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b7bef-111">**Части документа**</span><span class="sxs-lookup"><span data-stu-id="b7bef-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b7bef-112">Connections. XML</span><span class="sxs-lookup"><span data-stu-id="b7bef-112">connections.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b7bef-113">Определение</span><span class="sxs-lookup"><span data-stu-id="b7bef-113">Definition</span></span>

```XML
< xs:element name="DataConnection" type="DataConnection_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b7bef-114">Элементы и атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7bef-114">Elements and attributes</span></span>

<span data-ttu-id="b7bef-115">Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений.</span><span class="sxs-lookup"><span data-stu-id="b7bef-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b7bef-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="b7bef-116">Parent elements</span></span>

|<span data-ttu-id="b7bef-117">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="b7bef-117">**Element**</span></span>|<span data-ttu-id="b7bef-118">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7bef-118">**Type**</span></span>|<span data-ttu-id="b7bef-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7bef-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b7bef-120">DataConnections</span><span class="sxs-lookup"><span data-stu-id="b7bef-120">DataConnections</span></span>](dataconnections-elementvisio-xml.md) <br/> |[<span data-ttu-id="b7bef-121">Датаконнектионс_типе</span><span class="sxs-lookup"><span data-stu-id="b7bef-121">DataConnections_Type</span></span>](dataconnections_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b7bef-122">Содержит элементы **подключения** к документу.</span><span class="sxs-lookup"><span data-stu-id="b7bef-122">Contains the **DataConnection** elements for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b7bef-123">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b7bef-123">Child elements</span></span>

<span data-ttu-id="b7bef-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="b7bef-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b7bef-125">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b7bef-125">Attributes</span></span>

|<span data-ttu-id="b7bef-126">**Атрибут**</span><span class="sxs-lookup"><span data-stu-id="b7bef-126">**Attribute**</span></span>|<span data-ttu-id="b7bef-127">**Тип**</span><span class="sxs-lookup"><span data-stu-id="b7bef-127">**Type**</span></span>|<span data-ttu-id="b7bef-128">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="b7bef-128">**Required**</span></span>|<span data-ttu-id="b7bef-129">**Описание**</span><span class="sxs-lookup"><span data-stu-id="b7bef-129">**Description**</span></span>|<span data-ttu-id="b7bef-130">**Возможные значения**</span><span class="sxs-lookup"><span data-stu-id="b7bef-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b7bef-131">AlwaysUseConnectionFile</span><span class="sxs-lookup"><span data-stu-id="b7bef-131">AlwaysUseConnectionFile</span></span>  <br/> |<span data-ttu-id="b7bef-132">XSD: Boolean</span><span class="sxs-lookup"><span data-stu-id="b7bef-132">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b7bef-133">необязательный</span><span class="sxs-lookup"><span data-stu-id="b7bef-133">optional</span></span>  <br/> |<span data-ttu-id="b7bef-134">Значение по умолчанию  false.</span><span class="sxs-lookup"><span data-stu-id="b7bef-134">The default value is false.</span></span> <span data-ttu-id="b7bef-135">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="b7bef-135">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="b7bef-136">Значения типа XSD: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b7bef-136">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b7bef-137">Command</span><span class="sxs-lookup"><span data-stu-id="b7bef-137">Command</span></span>  <br/> |<span data-ttu-id="b7bef-138">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="b7bef-138">xsd:string</span></span>  <br/> |<span data-ttu-id="b7bef-139">необязательный</span><span class="sxs-lookup"><span data-stu-id="b7bef-139">optional</span></span>  <br/> |<span data-ttu-id="b7bef-140">Командная строка, используемая для запроса к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="b7bef-140">The command string used to query the data source.</span></span>  <br/> |<span data-ttu-id="b7bef-141">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="b7bef-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b7bef-142">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b7bef-142">ConnectionString</span></span>  <br/> |<span data-ttu-id="b7bef-143">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="b7bef-143">xsd:string</span></span>  <br/> |<span data-ttu-id="b7bef-144">необязательный</span><span class="sxs-lookup"><span data-stu-id="b7bef-144">optional</span></span>  <br/> |<span data-ttu-id="b7bef-145">Строка подключения, определяющая параметры, необходимые для подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="b7bef-145">The connection string that defines the parameters necessary to connect to a data source.</span></span>  <br/> |<span data-ttu-id="b7bef-146">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="b7bef-146">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b7bef-147">FileName</span><span class="sxs-lookup"><span data-stu-id="b7bef-147">FileName</span></span>  <br/> |<span data-ttu-id="b7bef-148">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="b7bef-148">xsd:string</span></span>  <br/> |<span data-ttu-id="b7bef-149">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b7bef-149">required</span></span>  <br/> |<span data-ttu-id="b7bef-150">Имя файла подключения.</span><span class="sxs-lookup"><span data-stu-id="b7bef-150">The name of the connection file.</span></span> <span data-ttu-id="b7bef-151">Дополнительные сведения см.</span><span class="sxs-lookup"><span data-stu-id="b7bef-151">See Remarks for more information.</span></span>  <br/> |<span data-ttu-id="b7bef-152">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="b7bef-152">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b7bef-153">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b7bef-153">FriendlyName</span></span>  <br/> |<span data-ttu-id="b7bef-154">XSD: строка</span><span class="sxs-lookup"><span data-stu-id="b7bef-154">xsd:string</span></span>  <br/> |<span data-ttu-id="b7bef-155">необязательный</span><span class="sxs-lookup"><span data-stu-id="b7bef-155">optional</span></span>  <br/> |<span data-ttu-id="b7bef-156">Имя, указанное пользователем для подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="b7bef-156">A user provided name for the data connection.</span></span>  <br/> |<span data-ttu-id="b7bef-157">Значения типа String: XSD.</span><span class="sxs-lookup"><span data-stu-id="b7bef-157">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b7bef-158">ID</span><span class="sxs-lookup"><span data-stu-id="b7bef-158">ID</span></span>  <br/> |<span data-ttu-id="b7bef-159">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="b7bef-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7bef-160">Обязательный</span><span class="sxs-lookup"><span data-stu-id="b7bef-160">required</span></span>  <br/> |<span data-ttu-id="b7bef-161">Идентификатор, назначенный Visio для данного подключения, уникальный в пределах документа.</span><span class="sxs-lookup"><span data-stu-id="b7bef-161">The ID assigned by Visio for a given connection, unique within the document.</span></span>  <br/> |<span data-ttu-id="b7bef-162">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="b7bef-162">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b7bef-163">Timeout</span><span class="sxs-lookup"><span data-stu-id="b7bef-163">Timeout</span></span>  <br/> |<span data-ttu-id="b7bef-164">XSD: Унсигнединт</span><span class="sxs-lookup"><span data-stu-id="b7bef-164">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b7bef-165">необязательный</span><span class="sxs-lookup"><span data-stu-id="b7bef-165">optional</span></span>  <br/> |<span data-ttu-id="b7bef-166">Время ожидания в минутах при попытке установить подключение перед завершением попытки.</span><span class="sxs-lookup"><span data-stu-id="b7bef-166">The wait time in minutes while trying to establish a connection before terminating the attempt.</span></span>  <br/> |<span data-ttu-id="b7bef-167">Значения типа XSD: Унсигнединт.</span><span class="sxs-lookup"><span data-stu-id="b7bef-167">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

