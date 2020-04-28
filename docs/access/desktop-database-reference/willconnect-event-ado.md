---
title: Событие событие willconnect (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305889"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="e88d3-102">Событие событие willconnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="e88d3-102">WillConnect event (ADO)</span></span>

<span data-ttu-id="e88d3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e88d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e88d3-104">Событие **событие willconnect** вызывается до начала подключения.</span><span class="sxs-lookup"><span data-stu-id="e88d3-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="e88d3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e88d3-105">Syntax</span></span>

<span data-ttu-id="e88d3-106">Событие willconnect*ConnectionString*, *UserID*, *Password*, *Options*, *адстатус*, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="e88d3-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="e88d3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e88d3-107">Parameters</span></span>

|<span data-ttu-id="e88d3-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="e88d3-108">Parameter</span></span>|<span data-ttu-id="e88d3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e88d3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e88d3-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="e88d3-110">*ConnectionString*</span></span> |<span data-ttu-id="e88d3-111">**Строка** , содержащая сведения о подключении для ожидающего подключения.</span><span class="sxs-lookup"><span data-stu-id="e88d3-111">A **String** that contains connection information for the pending connection.</span></span>|
|<span data-ttu-id="e88d3-112">*UserID*</span><span class="sxs-lookup"><span data-stu-id="e88d3-112">*UserID*</span></span> |<span data-ttu-id="e88d3-113">**Строка** , содержащая имя пользователя для ожидающего подключения.</span><span class="sxs-lookup"><span data-stu-id="e88d3-113">A **String** that contains a user name for the pending connection.</span></span>|
|<span data-ttu-id="e88d3-114">*Password*</span><span class="sxs-lookup"><span data-stu-id="e88d3-114">*Password*</span></span> |<span data-ttu-id="e88d3-115">**Строка** , содержащая пароль для ожидающего подключения.</span><span class="sxs-lookup"><span data-stu-id="e88d3-115">A **String** that contains a password for the pending connection.</span></span>|
|<span data-ttu-id="e88d3-116">*Параметры*</span><span class="sxs-lookup"><span data-stu-id="e88d3-116">*Options*</span></span> |<span data-ttu-id="e88d3-117">**Длинное** значение, указывающее, как поставщик должен оценивать *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="e88d3-117">A **Long** value that indicates how the provider should evaluate the *ConnectionString*.</span></span> <span data-ttu-id="e88d3-118">Единственный вариант — **адасинкопен**.</span><span class="sxs-lookup"><span data-stu-id="e88d3-118">Your only option is **adAsyncOpen**.</span></span>|
|<span data-ttu-id="e88d3-119">*адстатус*</span><span class="sxs-lookup"><span data-stu-id="e88d3-119">*adStatus*</span></span> |<span data-ttu-id="e88d3-120">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="e88d3-120">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="e88d3-121">При вызове этого события для этого параметра по умолчанию задано значение **адстатусок** .</span><span class="sxs-lookup"><span data-stu-id="e88d3-121">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="e88d3-122">Он имеет значение **адстатускантдени** , если событие не может запрашивать отмену ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="e88d3-122">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span><br/><br/><span data-ttu-id="e88d3-123">Перед возвращением этого события установите для этого параметра значение **адстатусунвантедевент** , чтобы предотвратить появление последующих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e88d3-123">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="e88d3-124">Присвойте этому параметру значение **адстатусканцел** , чтобы запросить операцию подключения, которая привела к отмене этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="e88d3-124">Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>|
|<span data-ttu-id="e88d3-125">*пконнектион*</span><span class="sxs-lookup"><span data-stu-id="e88d3-125">*pConnection*</span></span> |<span data-ttu-id="e88d3-126">Объект [Connection](connection-object-ado.md) , для которого применяется это уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="e88d3-126">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span> <span data-ttu-id="e88d3-127">Изменения параметров **подключения** с помощью обработчика событий **событие willconnect** не приведут к **подключению**.</span><span class="sxs-lookup"><span data-stu-id="e88d3-127">Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="e88d3-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="e88d3-128">Remarks</span></span>

<span data-ttu-id="e88d3-129">При вызове **событие willconnect** параметры *ConnectionString*, *UserID*, *Password*и *Options* задаются значениями, установленными операцией, которая вызвала это событие (ожидающее подключение), и может быть изменено до того, как событие будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="e88d3-129">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</span></span> <span data-ttu-id="e88d3-130">**Событие willconnect** может вернуть запрос на отмену ожидающего подключения.</span><span class="sxs-lookup"><span data-stu-id="e88d3-130">**WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="e88d3-131">При отмене этого события вызывается метод **события connectcomplete** с параметром *адстатус* , для которого задано значение **адстатусеррорсоккурред**.</span><span class="sxs-lookup"><span data-stu-id="e88d3-131">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

