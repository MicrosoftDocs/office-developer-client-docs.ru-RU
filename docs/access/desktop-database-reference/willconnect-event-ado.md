---
title: Событие WillConnect (ADO)
TOCTitle: WillConnect event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6e62a01d274752b33f7bf3f6f4af6171e7efb16b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703435"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="d3ab9-102">Событие WillConnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="d3ab9-102">WillConnect event (ADO)</span></span>

<span data-ttu-id="d3ab9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3ab9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d3ab9-104">Событие **WillConnect** вызывается до начала подключения.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3ab9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3ab9-105">Syntax</span></span>

<span data-ttu-id="d3ab9-106">WillConnect*ConnectionString*, *идентификатор пользователя*, *пароль*, *Параметры*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="d3ab9-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="d3ab9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d3ab9-107">Parameters</span></span>

|<span data-ttu-id="d3ab9-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d3ab9-108">Parameter</span></span>|<span data-ttu-id="d3ab9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d3ab9-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d3ab9-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="d3ab9-110">*ConnectionString*</span></span> |<span data-ttu-id="d3ab9-111">**Строка** , которая содержит сведения о подключении для ожидания подключения.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-111">A **String** that contains connection information for the pending connection.</span></span>|
|<span data-ttu-id="d3ab9-112">*UserID*</span><span class="sxs-lookup"><span data-stu-id="d3ab9-112">*UserID*</span></span> |<span data-ttu-id="d3ab9-113">**Строка** , содержащая имя пользователя для подключения к ожидающие.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-113">A **String** that contains a user name for the pending connection.</span></span>|
|<span data-ttu-id="d3ab9-114">*Password*</span><span class="sxs-lookup"><span data-stu-id="d3ab9-114">*Password*</span></span> |<span data-ttu-id="d3ab9-115">**Строка** , содержащая пароль для ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-115">A **String** that contains a password for the pending connection.</span></span>|
|<span data-ttu-id="d3ab9-116">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="d3ab9-116">*Options*</span></span> |<span data-ttu-id="d3ab9-117">**Длинное** значение, которое указывает, как поставщик необходимо решить, *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-117">A **Long** value that indicates how the provider should evaluate the *ConnectionString*.</span></span> <span data-ttu-id="d3ab9-118">Единственным вариантом является **adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-118">Your only option is **adAsyncOpen**.</span></span>|
|<span data-ttu-id="d3ab9-119">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="d3ab9-119">*adStatus*</span></span> |<span data-ttu-id="d3ab9-120">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="d3ab9-120">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="d3ab9-121">Когда это событие вызывается, этот параметр имеет значение **adStatusOK** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-121">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="d3ab9-122">Если событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="d3ab9-122">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span><br/><br/><span data-ttu-id="d3ab9-123">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-123">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="d3ab9-124">Присвойте этому параметру значение **adStatusCancel** для запроса операции подключения, в которой обнаружен отмены это уведомление.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-124">Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>|
|<span data-ttu-id="d3ab9-125">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="d3ab9-125">*pConnection*</span></span> |<span data-ttu-id="d3ab9-126">Объект [подключения](connection-object-ado.md) , для которого применяется этого уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-126">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span> <span data-ttu-id="d3ab9-127">Изменения параметров **подключения** обработчика событий **WillConnect** не повлияет на **подключение**.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-127">Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d3ab9-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="d3ab9-128">Remarks</span></span>

<span data-ttu-id="d3ab9-129">При вызове **WillConnect** *ConnectionString*, *идентификатор пользователя*, *пароль*и *Параметры* — значение значения, заданные в операцию, которая вызвала это событие (ожидающие подключения) и может быть изменено Прежде чем возвращает события.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-129">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</span></span> <span data-ttu-id="d3ab9-130">**WillConnect** может возвратить запрос на отменить ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-130">**WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="d3ab9-131">Когда это событие отменяется, **ConnectComplete** вызывается с его *adStatus* параметру присвоено значение **adStatusErrorsOccurred**.</span><span class="sxs-lookup"><span data-stu-id="d3ab9-131">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

