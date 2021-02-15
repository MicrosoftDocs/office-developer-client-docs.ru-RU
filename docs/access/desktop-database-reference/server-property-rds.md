---
title: Свойство сервера (RDS)
TOCTitle: Server property (RDS)
ms:assetid: 17519dbe-a43a-1d0d-22c1-dc0def2f63ab
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248926(v=office.15)
ms:contentKeyID: 48543448
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f35910591d86e0e5a2b92d680be3c5f64504088
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308689"
---
# <a name="server-property-rds"></a><span data-ttu-id="f0034-102">Свойство сервера (RDS)</span><span class="sxs-lookup"><span data-stu-id="f0034-102">Server property (RDS)</span></span>

<span data-ttu-id="f0034-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0034-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0034-104">Указывает имя служб IIS и протокол связи.</span><span class="sxs-lookup"><span data-stu-id="f0034-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="f0034-105">Вы можете настроить свойство **Server** во время разработки в [RDS. Теги](datacontrol-object-rds.md) OBJECT объекта DataControl или во время запуска в коде скриптов.</span><span class="sxs-lookup"><span data-stu-id="f0034-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0034-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0034-106">Syntax</span></span>

|<span data-ttu-id="f0034-107">Протокол</span><span class="sxs-lookup"><span data-stu-id="f0034-107">Protocol</span></span>|<span data-ttu-id="f0034-108">Синтаксис времени разработки</span><span class="sxs-lookup"><span data-stu-id="f0034-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="f0034-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="f0034-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="f0034-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f0034-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="f0034-111">DCOM</span><span class="sxs-lookup"><span data-stu-id="f0034-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="f0034-112">В процессе</span><span class="sxs-lookup"><span data-stu-id="f0034-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="f0034-113">Протокол</span><span class="sxs-lookup"><span data-stu-id="f0034-113">Protocol</span></span>|<span data-ttu-id="f0034-114">Синтаксис времени запуска</span><span class="sxs-lookup"><span data-stu-id="f0034-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="f0034-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="f0034-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="f0034-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="f0034-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="f0034-117">DCOM</span><span class="sxs-lookup"><span data-stu-id="f0034-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="f0034-118">В процессе</span><span class="sxs-lookup"><span data-stu-id="f0034-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="f0034-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0034-119">Parameters</span></span>

|<span data-ttu-id="f0034-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="f0034-120">Parameter</span></span>|<span data-ttu-id="f0034-121">Описание</span><span class="sxs-lookup"><span data-stu-id="f0034-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f0034-122">*awebsrvr* или *имя компьютера*</span><span class="sxs-lookup"><span data-stu-id="f0034-122">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="f0034-123">**Строка,** которая содержит путь к Интернету или интрасети или имя компьютера, если сервер находится на удаленном компьютере; или пустую строку, если сервер находится на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f0034-123">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>|
|<span data-ttu-id="f0034-124">*port*</span><span class="sxs-lookup"><span data-stu-id="f0034-124">*port*</span></span> |<span data-ttu-id="f0034-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="f0034-125">Optional.</span></span> <span data-ttu-id="f0034-126">Порт, используемый для подключения к серверу IIS.</span><span class="sxs-lookup"><span data-stu-id="f0034-126">A port that is used to connect to an IIS server.</span></span> <span data-ttu-id="f0034-127">Номер порта устанавливается в Internet Explorer (в меню "Инструменты"  щелкните "Параметры браузера" и выберите вкладку "Подключение") или в IIS. </span><span class="sxs-lookup"><span data-stu-id="f0034-127">The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>|
|<span data-ttu-id="f0034-128">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="f0034-128">*DataControl*</span></span> |<span data-ttu-id="f0034-129">Объектная переменная, представляюная **RDS. Объект DataControl.**</span><span class="sxs-lookup"><span data-stu-id="f0034-129">An object variable that represents an **RDS.DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="f0034-130">Заметки</span><span class="sxs-lookup"><span data-stu-id="f0034-130">Remarks</span></span>

<span data-ttu-id="f0034-131">Сервер — это расположение, в котором находится **RDS. Обработка запроса DataControl** (то есть запроса или обновления).</span><span class="sxs-lookup"><span data-stu-id="f0034-131">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="f0034-132">По умолчанию все запросы обрабатываются объектом [RDSServer.DataFactory](datafactory-object-rdsserver.md) [MSDFMAP. Компонент обработки](datafactory-customization.md) и [MSDFMAP.INI](understanding-the-customization-file.md) на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="f0034-132">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="f0034-133">Помните, что при изменении серверов для согласования параметров в старых и **MSDFMAP.INI** файлов.</span><span class="sxs-lookup"><span data-stu-id="f0034-133">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="f0034-134">Несовместимость может привести к сбойу запросов, которые были успешно на одном сервере, на другом.</span><span class="sxs-lookup"><span data-stu-id="f0034-134">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="f0034-135">Если для свойства Server установлено "", эти объекты будут использоваться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="f0034-135">If the Server property is set to "", these objects will be used on the local machine.</span></span>

