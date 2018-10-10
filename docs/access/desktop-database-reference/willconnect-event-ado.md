---
title: WillConnect Event (ADO)
TOCTitle: WillConnect Event (ADO)
ms:assetid: 8b0e9955-4e7a-7af8-ce6c-7a4ba569a5bb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249611(v=office.15)
ms:contentKeyID: 48546208
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c5493593998bf5484bd2247b32e114809b805fda
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483114"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="beda4-102">WillConnect Event (ADO)</span><span class="sxs-lookup"><span data-stu-id="beda4-102">WillConnect Event (ADO)</span></span>


<span data-ttu-id="beda4-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="beda4-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="beda4-104">Событие **WillConnect** вызывается до начала подключения.</span><span class="sxs-lookup"><span data-stu-id="beda4-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="beda4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="beda4-105">Syntax</span></span>

<span data-ttu-id="beda4-106">WillConnect*ConnectionString*, *идентификатор пользователя*, *пароль*, *Параметры*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="beda4-106">WillConnect*ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="beda4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="beda4-107">Parameters</span></span>

  - <span data-ttu-id="beda4-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="beda4-108">*ConnectionString*</span></span>

  - <span data-ttu-id="beda4-109">**Строка** , которая содержит сведения о подключении для ожидания подключения.</span><span class="sxs-lookup"><span data-stu-id="beda4-109">A **String** that contains connection information for the pending connection.</span></span>

  - <span data-ttu-id="beda4-110">*Идентификатор пользователя*</span><span class="sxs-lookup"><span data-stu-id="beda4-110">*UserID*</span></span>

  - <span data-ttu-id="beda4-111">**Строка** , содержащая имя пользователя для подключения к ожидающие.</span><span class="sxs-lookup"><span data-stu-id="beda4-111">A **String** that contains a user name for the pending connection.</span></span>

  - <span data-ttu-id="beda4-112">*Password*</span><span class="sxs-lookup"><span data-stu-id="beda4-112">*Password*</span></span>

  - <span data-ttu-id="beda4-113">**Строка** , содержащая пароль для ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="beda4-113">A **String** that contains a password for the pending connection.</span></span>

  - <span data-ttu-id="beda4-114">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="beda4-114">*Options*</span></span>

  - <span data-ttu-id="beda4-115">**Длинное** значение, которое указывает, как поставщик необходимо решить, *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="beda4-115">A **Long** value that indicates how the provider should evaluate the *ConnectionString*.</span></span> <span data-ttu-id="beda4-116">Единственным вариантом является **adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="beda4-116">Your only option is **adAsyncOpen**.</span></span>

  - <span data-ttu-id="beda4-117">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="beda4-117">*adStatus*</span></span>

  - [<span data-ttu-id="beda4-118">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="beda4-118">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="beda4-119">Когда это событие вызывается, этот параметр имеет значение **adStatusOK** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="beda4-119">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="beda4-120">Если событие не могут запрашивать отмену ожидающие операции перейдут в **adStatusCantDeny** .</span><span class="sxs-lookup"><span data-stu-id="beda4-120">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="beda4-121">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="beda4-121">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="beda4-122">Присвойте этому параметру значение **adStatusCancel** для запроса операции подключения, в которой обнаружен отмены это уведомление.</span><span class="sxs-lookup"><span data-stu-id="beda4-122">Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>

  - <span data-ttu-id="beda4-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="beda4-123">*pConnection*</span></span>

  - <span data-ttu-id="beda4-124">Объект [подключения](connection-object-ado.md) , для которого применяется этого уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="beda4-124">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span> <span data-ttu-id="beda4-125">Изменения параметров **подключения** обработчика событий **WillConnect** не повлияет на **подключение**.</span><span class="sxs-lookup"><span data-stu-id="beda4-125">Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>

## <a name="remarks"></a><span data-ttu-id="beda4-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="beda4-126">Remarks</span></span>

<span data-ttu-id="beda4-127">При вызове **WillConnect** *ConnectionString*, *идентификатор пользователя*, *пароль*и *Параметры* — значение значения, заданные в операцию, которая вызвала это событие (ожидающие подключения) и может быть изменено Прежде чем возвращает события.</span><span class="sxs-lookup"><span data-stu-id="beda4-127">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</span></span> <span data-ttu-id="beda4-128">**WillConnect** может возвратить запрос на отменить ожидающие подключения.</span><span class="sxs-lookup"><span data-stu-id="beda4-128">**WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="beda4-129">Когда это событие отменяется, **ConnectComplete** вызывается с его *adStatus* параметру присвоено значение **adStatusErrorsOccurred**.</span><span class="sxs-lookup"><span data-stu-id="beda4-129">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

