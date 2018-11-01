---
title: Свойства сервера (RDS)
TOCTitle: Server Property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 487b6e676816ab571cb08f6cfe7870362c7a8c84
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868436"
---
# <a name="server-property-rds"></a><span data-ttu-id="5c194-102">Свойства сервера (RDS)</span><span class="sxs-lookup"><span data-stu-id="5c194-102">Server Property (RDS)</span></span>


<span data-ttu-id="5c194-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c194-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5c194-104">Указывает имя и связи протокол Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="5c194-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="5c194-105">Свойства **сервера** во время разработки в [RDS. DataControl](datacontrol-object-rds.md) теги OBJECT объекта, или во время выполнения в коде сценария.</span><span class="sxs-lookup"><span data-stu-id="5c194-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c194-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5c194-106">Syntax</span></span>

|<span data-ttu-id="5c194-107">Протокол</span><span class="sxs-lookup"><span data-stu-id="5c194-107">Protocol</span></span>|<span data-ttu-id="5c194-108">Синтаксис во время разработки</span><span class="sxs-lookup"><span data-stu-id="5c194-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="5c194-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="5c194-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="5c194-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="5c194-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="5c194-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="5c194-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="5c194-112">В работе</span><span class="sxs-lookup"><span data-stu-id="5c194-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="5c194-113">Протокол</span><span class="sxs-lookup"><span data-stu-id="5c194-113">Protocol</span></span>|<span data-ttu-id="5c194-114">Синтаксис во время выполнения</span><span class="sxs-lookup"><span data-stu-id="5c194-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="5c194-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="5c194-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="5c194-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="5c194-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="5c194-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="5c194-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="5c194-118">В работе</span><span class="sxs-lookup"><span data-stu-id="5c194-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="5c194-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="5c194-119">Parameters</span></span>

<span data-ttu-id="5c194-120">*awebsrvr* или *имя компьютера*</span><span class="sxs-lookup"><span data-stu-id="5c194-120">*awebsrvr* or *computername*</span></span>

- <span data-ttu-id="5c194-121">**Строковое** значение, содержащее Интернет или интрасети путь или имя компьютера, если сервер на удаленном компьютере; или же пустая строка, если сервер не на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5c194-121">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>

<span data-ttu-id="5c194-122">*порт*</span><span class="sxs-lookup"><span data-stu-id="5c194-122">*port*</span></span>

- <span data-ttu-id="5c194-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="5c194-123">Optional.</span></span> <span data-ttu-id="5c194-124">Порт, используемый для подключения к серверу службы IIS.</span><span class="sxs-lookup"><span data-stu-id="5c194-124">A port that is used to connect to an IIS server.</span></span> <span data-ttu-id="5c194-125">Номер порта задано в Internet Explorer (в меню **Сервис** выберите пункт **Свойства обозревателя**и перейдите на вкладку **подключения** ) или в службах IIS.</span><span class="sxs-lookup"><span data-stu-id="5c194-125">The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>

<span data-ttu-id="5c194-126">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="5c194-126">*DataControl*</span></span>

- <span data-ttu-id="5c194-127">Объектную переменную, которая представляет **RDS. DataControl** объекта.</span><span class="sxs-lookup"><span data-stu-id="5c194-127">An object variable that represents an **RDS.DataControl** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c194-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="5c194-128">Remarks</span></span>

<span data-ttu-id="5c194-129">Сервер — это местоположение где **RDS. DataControl** обработки запроса (то есть, запроса или обновления).</span><span class="sxs-lookup"><span data-stu-id="5c194-129">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="5c194-130">По умолчанию все запросы обрабатываются с помощью объекта [RDSServer.DataFactory](datafactory-object-rdsserver.md) , [MSDFMAP. Обработчик](datafactory-customization.md) компонента и [MSDFMAP. INI](understanding-the-customization-file.md) файл на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="5c194-130">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="5c194-131">Помните, что при изменении серверы для согласования параметров в старой и новой **MSDFMAP. INI** файлов.</span><span class="sxs-lookup"><span data-stu-id="5c194-131">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="5c194-132">На совместимость может стать причиной запросов, которые выполняются успешно на одном сервере к сбою на другой.</span><span class="sxs-lookup"><span data-stu-id="5c194-132">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="5c194-133">Если свойство сервера задано значение «», эти объекты будут использоваться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5c194-133">If the Server property is set to "", these objects will be used on the local machine.</span></span>

