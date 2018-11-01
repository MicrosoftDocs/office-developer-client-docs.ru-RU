---
title: Событие WillConnect (ADO)
TOCTitle: WillConnect Event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51d9d0b11d137fbca8bf5efdddfe51469642c405
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887175"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="34f65-102">Событие WillConnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="34f65-102">WillConnect Event (ADO)</span></span>


<span data-ttu-id="34f65-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34f65-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="34f65-104">Событие **WillConnect** вызывается до начала подключения.</span><span class="sxs-lookup"><span data-stu-id="34f65-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="34f65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34f65-105">Syntax</span></span>

<span data-ttu-id="34f65-106">WillConnect*ConnectionString*, *идентификатор пользователя*, *пароль*, *Параметры*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="34f65-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="34f65-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34f65-107">Parameters</span></span>

  - <span data-ttu-id="34f65-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="34f65-108">*ConnectionString*</span></span>

  - <span data-ttu-id="34f65-109">**Строка** , которая содержит сведения о подключении для ожидания подключения.</span><span class="sxs-lookup"><span data-stu-id="34f65-109">A **String** that contains connection information for the pending connection.</span></span>

  - <span data-ttu-id="34f65-110">*Идентификатор пользователя*</span><span class="sxs-lookup"><span data-stu-id="34f65-110">*UserID*</span></span>

  - <span data-ttu-id="34f65-111">**Строка** , содержащая имя пользователя для подключения к ожидающие.</span><span class="sxs-lookup"><span data-stu-id="34f65-111">A **String** that contains a user name for the pending connection.</span></span>

  - <span data-ttu-id="34f65-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="34f65-112">*Password*</span></span>

  - <span data-ttu-id="34f65-113">**Строка** , содержащая пароль для ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="34f65-113">A **String** that contains a password for the pending connection.</span></span>

  - <span data-ttu-id="34f65-114">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="34f65-114">*Options*</span></span>

  - <span data-ttu-id="34f65-115">**Длинное** значение, которое указывает, как поставщик необходимо решить, *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="34f65-115">A **Long** value that indicates how the provider should evaluate the *ConnectionString*.</span></span> <span data-ttu-id="34f65-116">Единственным вариантом является **adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="34f65-116">Your only option is **adAsyncOpen**.</span></span>

  - <span data-ttu-id="34f65-117">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="34f65-117">*adStatus*</span></span>

  - [<span data-ttu-id="34f65-118">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="34f65-118">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="34f65-119">Когда это событие вызывается, этот параметр имеет значение **adStatusOK** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34f65-119">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="34f65-120">Если событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="34f65-120">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="34f65-121">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="34f65-121">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="34f65-122">Присвойте этому параметру значение **adStatusCancel** для запроса операции подключения, в которой обнаружен отмены это уведомление.</span><span class="sxs-lookup"><span data-stu-id="34f65-122">Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>

  - <span data-ttu-id="34f65-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="34f65-123">*pConnection*</span></span>

  - <span data-ttu-id="34f65-124">Объект [подключения](connection-object-ado.md) , для которого применяется этого уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="34f65-124">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span> <span data-ttu-id="34f65-125">Изменения параметров **подключения** обработчика событий **WillConnect** не повлияет на **подключение**.</span><span class="sxs-lookup"><span data-stu-id="34f65-125">Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>

## <a name="remarks"></a><span data-ttu-id="34f65-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="34f65-126">Remarks</span></span>

<span data-ttu-id="34f65-127">При вызове **WillConnect** *ConnectionString*, *идентификатор пользователя*, *пароль*и *Параметры* — значение значения, заданные в операцию, которая вызвала это событие (ожидающие подключения) и может быть изменено Прежде чем возвращает события.</span><span class="sxs-lookup"><span data-stu-id="34f65-127">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</span></span> <span data-ttu-id="34f65-128">**WillConnect** может возвратить запрос на отменить ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="34f65-128">**WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="34f65-129">Когда это событие отменяется, **ConnectComplete** вызывается с его *adStatus* параметру присвоено значение **adStatusErrorsOccurred**.</span><span class="sxs-lookup"><span data-stu-id="34f65-129">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

