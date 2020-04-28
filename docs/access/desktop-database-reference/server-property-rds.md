---
title: Свойство Server (RDS)
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
# <a name="server-property-rds"></a><span data-ttu-id="6a7a0-102">Свойство Server (RDS)</span><span class="sxs-lookup"><span data-stu-id="6a7a0-102">Server property (RDS)</span></span>

<span data-ttu-id="6a7a0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a7a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a7a0-104">Указывает имя служб IIS и протокол связи.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-104">Indicates the Internet Information Services (IIS) name and communication protocol.</span></span>

<span data-ttu-id="6a7a0-105">Свойство **Server** можно задать во время создания в элементе [ActiveX RDS. Объектные теги объекта DataObject или](datacontrol-object-rds.md) во время выполнения в коде скрипта.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-105">You can set the **Server** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7a0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a7a0-106">Syntax</span></span>

|<span data-ttu-id="6a7a0-107">Протокол</span><span class="sxs-lookup"><span data-stu-id="6a7a0-107">Protocol</span></span>|<span data-ttu-id="6a7a0-108">Синтаксис времени конструирования</span><span class="sxs-lookup"><span data-stu-id="6a7a0-108">Design-time syntax</span></span>|
|:-------|:-----------------|
|<span data-ttu-id="6a7a0-109">HTTP</span><span class="sxs-lookup"><span data-stu-id="6a7a0-109">HTTP</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="6a7a0-110">HTTPS</span><span class="sxs-lookup"><span data-stu-id="6a7a0-110">HTTPS</span></span>|`<PARAM NAME="Server" VALUE="https://awebsrvr:port">`|
|<span data-ttu-id="6a7a0-111">ТРАФИК</span><span class="sxs-lookup"><span data-stu-id="6a7a0-111">DCOM</span></span>|`<PARAM NAME="Server" VALUE="computername">`|
|<span data-ttu-id="6a7a0-112">Внутрипроцессный</span><span class="sxs-lookup"><span data-stu-id="6a7a0-112">In-process</span></span>|`<PARAM NAME="Server" VALUE="">`|


|<span data-ttu-id="6a7a0-113">Протокол</span><span class="sxs-lookup"><span data-stu-id="6a7a0-113">Protocol</span></span>|<span data-ttu-id="6a7a0-114">Синтаксис времени выполнения</span><span class="sxs-lookup"><span data-stu-id="6a7a0-114">Run-time syntax</span></span>|
|:-------|:--------------|
|<span data-ttu-id="6a7a0-115">HTTP</span><span class="sxs-lookup"><span data-stu-id="6a7a0-115">HTTP</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="6a7a0-116">HTTPS</span><span class="sxs-lookup"><span data-stu-id="6a7a0-116">HTTPS</span></span>|`DataControl.Server="https://awebsrvr:port"`|
|<span data-ttu-id="6a7a0-117">ТРАФИК</span><span class="sxs-lookup"><span data-stu-id="6a7a0-117">DCOM</span></span>|`DataControl.Server="computername"`|
|<span data-ttu-id="6a7a0-118">Внутрипроцессный</span><span class="sxs-lookup"><span data-stu-id="6a7a0-118">In-process</span></span>|`DataControl.Server=""`|


## <a name="parameters"></a><span data-ttu-id="6a7a0-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="6a7a0-119">Parameters</span></span>

|<span data-ttu-id="6a7a0-120">Параметр</span><span class="sxs-lookup"><span data-stu-id="6a7a0-120">Parameter</span></span>|<span data-ttu-id="6a7a0-121">Описание</span><span class="sxs-lookup"><span data-stu-id="6a7a0-121">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6a7a0-122">*авебсрвр* или *ComputerName*</span><span class="sxs-lookup"><span data-stu-id="6a7a0-122">*awebsrvr* or *computername*</span></span> |<span data-ttu-id="6a7a0-123">**Строковое** значение, содержащее путь в Интернете или интрасети, или имя компьютера, если сервер находится на удаленном компьютере; или пустая строка, если сервер находится на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-123">A **String** value that contains an Internet or intranet path, or computer name, if the server is on a remote computer; or, an empty string if the server is on the local computer.</span></span>|
|<span data-ttu-id="6a7a0-124">*порта*</span><span class="sxs-lookup"><span data-stu-id="6a7a0-124">*port*</span></span> |<span data-ttu-id="6a7a0-125">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-125">Optional.</span></span> <span data-ttu-id="6a7a0-126">Порт, используемый для подключения к серверу IIS.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-126">A port that is used to connect to an IIS server.</span></span> <span data-ttu-id="6a7a0-127">Номер порта задается в Internet Explorer (в меню **Сервис** выберите пункт **Свойства браузера**, а затем перейдите на вкладку **Подключение** ) или в IIS.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-127">The port number is set in Internet Explorer (on the **Tools** menu, click **Internet Options**, and then select the **Connection** tab) or in IIS.</span></span>|
|<span data-ttu-id="6a7a0-128">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="6a7a0-128">*DataControl*</span></span> |<span data-ttu-id="6a7a0-129">Объектная переменная, представляющая **RDS. Объект управления** DataObject.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-129">An object variable that represents an **RDS.DataControl** object.</span></span>|

## <a name="remarks"></a><span data-ttu-id="6a7a0-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="6a7a0-130">Remarks</span></span>

<span data-ttu-id="6a7a0-131">Сервер — это расположение, в котором \*\*RDS. \*\*Обрабатывается запрос на получение доступа к управлению запросами (то есть запрос или обновление).</span><span class="sxs-lookup"><span data-stu-id="6a7a0-131">The server is the location where the **RDS.DataControl** request (that is, a query or update) is processed.</span></span> <span data-ttu-id="6a7a0-132">По умолчанию все запросы обрабатываются объектом [рдссервер.](datafactory-object-rdsserver.md) DataObject, [мсдфмап. Компонент обработчика](datafactory-customization.md) и [мсдфмап. INI](understanding-the-customization-file.md) -файл на указанном сервере.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-132">By default, all requests are processed by the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, [MSDFMAP.Handler](datafactory-customization.md) component, and [MSDFMAP.INI](understanding-the-customization-file.md) file on the specified server.</span></span> 

<span data-ttu-id="6a7a0-133">Помните, что при изменении серверов для согласования параметров в старых и новых **мсдфмап. INI** -файлы.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-133">Remember that when changing servers to reconcile settings in the old and new **MSDFMAP.INI** files.</span></span> <span data-ttu-id="6a7a0-134">Несовместимость может привести к сбою запросов, которые успешно выполняются на одном сервере.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-134">Incompatibilities may cause requests that succeed on one server to fail on another.</span></span> <span data-ttu-id="6a7a0-135">Если для свойства Server задано значение "", эти объекты будут использоваться на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="6a7a0-135">If the Server property is set to "", these objects will be used on the local machine.</span></span>

