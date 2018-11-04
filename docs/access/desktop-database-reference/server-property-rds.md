---
title: Свойство Server (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 492602d7150f3080df329d30a38e3af51755cf0f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949504"
---
# <a name="server-property-rds"></a><span data-ttu-id="aefe5-102">Свойство Server (RDS)</span><span class="sxs-lookup"><span data-stu-id="aefe5-102">Server property (RDS)</span></span>

<span data-ttu-id="aefe5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aefe5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aefe5-104">Указывает имя и связи протокол Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="aefe5-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="aefe5-105">Свойства **сервера** во время разработки в [RDS. DataControl](datacontrol-object-rds.md) теги OBJECT объекта, или во время выполнения в коде сценария.</span><span class="sxs-lookup"><span data-stu-id="aefe5-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aefe5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aefe5-106">Syntax</span></span>

|<span data-ttu-id="aefe5-107">Протокол</span><span class="sxs-lookup"><span data-stu-id="aefe5-107">Protocol</span></span>|<span data-ttu-id="aefe5-108">Синтаксис во время разработки</span><span class="sxs-lookup"><span data-stu-id="aefe5-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="aefe5-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="aefe5-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="aefe5-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="aefe5-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="aefe5-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="aefe5-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="aefe5-112">В работе</span><span class="sxs-lookup"><span data-stu-id="aefe5-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="aefe5-113">Протокол</span><span class="sxs-lookup"><span data-stu-id="aefe5-113">Protocol</span></span>|<span data-ttu-id="aefe5-114">Синтаксис во время выполнения</span><span class="sxs-lookup"><span data-stu-id="aefe5-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="aefe5-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="aefe5-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="aefe5-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="aefe5-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="aefe5-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="aefe5-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="aefe5-118">В работе</span><span class="sxs-lookup"><span data-stu-id="aefe5-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="aefe5-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="aefe5-119">Parameters</span></span>

|<span data-ttu-id="aefe5-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="aefe5-120">Parameter</span></span>|<span data-ttu-id="aefe5-121">Описание</span><span class="sxs-lookup"><span data-stu-id="aefe5-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="aefe5-122">*awebsrvr* или *имя компьютера*</span><span class="sxs-lookup"><span data-stu-id="aefe5-122">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="aefe5-123">**Строковое** значение, содержащее Интернет или интрасети путь или имя компьютера, если сервер на удаленном компьютере; или же пустая строка, если сервер не на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="aefe5-123">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>|
|<span data-ttu-id="aefe5-124">*порт*</span><span class="sxs-lookup"><span data-stu-id="aefe5-124">*port*</span></span> |<span data-ttu-id="aefe5-125">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="aefe5-125">Optional.</span></span> <span data-ttu-id="aefe5-126">Порт, используемый для подключения к серверу службы IIS.</span><span class="sxs-lookup"><span data-stu-id="aefe5-126">A port that is used to connect to an IIS server.</span></span> <span data-ttu-id="aefe5-127">Номер порта задано в Internet Explorer (в меню **Сервис** выберите пункт **Свойства обозревателя**и перейдите на вкладку **подключения** ) или в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="aefe5-127">The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>|
|<span data-ttu-id="aefe5-128">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="aefe5-128">*DataControl*</span></span> |<span data-ttu-id="aefe5-129">Объектную переменную, которая представляет **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="aefe5-129">An object variable that represents an **RDS.DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="aefe5-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="aefe5-130">Remarks</span></span>

<span data-ttu-id="aefe5-131">Сервер — это местоположение где **RDS. DataControl** обработки запроса (то есть, запроса или обновления).</span><span class="sxs-lookup"><span data-stu-id="aefe5-131">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="aefe5-132">По умолчанию все запросы обрабатываются с помощью объекта [RDSServer.DataFactory](datafactory-object-rdsserver.md) , [MSDFMAP. Обработчик](datafactory-customization.md) компонента и [MSDFMAP. INI](understanding-the-customization-file.md) файл на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="aefe5-132">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="aefe5-133">Помните, что при изменении серверы для согласования параметров в старой и новой **MSDFMAP. INI** файлов.</span><span class="sxs-lookup"><span data-stu-id="aefe5-133">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="aefe5-134">На совместимость может стать причиной запросов, которые выполняются успешно на одном сервере к сбою на другой.</span><span class="sxs-lookup"><span data-stu-id="aefe5-134">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="aefe5-135">Если свойство сервера задано значение «», эти объекты будут использоваться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="aefe5-135">If the Server property is set to "", these objects will be used on the local machine.</span></span>

