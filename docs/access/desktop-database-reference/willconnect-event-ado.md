---
title: WillConnect event (ADO)
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
# <a name="willconnect-event-ado"></a><span data-ttu-id="cc546-102">WillConnect event (ADO)</span><span class="sxs-lookup"><span data-stu-id="cc546-102">WillConnect event (ADO)</span></span>

<span data-ttu-id="cc546-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cc546-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cc546-104">Событие **WillConnect** вызвано перед началом подключения.</span><span class="sxs-lookup"><span data-stu-id="cc546-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc546-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cc546-105">Syntax</span></span>

<span data-ttu-id="cc546-106">WillConnect *ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="cc546-106">WillConnect *ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="cc546-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="cc546-107">Parameters</span></span>

|<span data-ttu-id="cc546-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="cc546-108">Parameter</span></span>|<span data-ttu-id="cc546-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cc546-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="cc546-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="cc546-110">*ConnectionString*</span></span> |<span data-ttu-id="cc546-111">**Строка,** содержаная сведения о под соединении для ожидающих подключений.</span><span class="sxs-lookup"><span data-stu-id="cc546-111">A **String** that contains connection information for the pending connection.</span></span>|
|<span data-ttu-id="cc546-112">*UserID*</span><span class="sxs-lookup"><span data-stu-id="cc546-112">*UserID*</span></span> |<span data-ttu-id="cc546-113">**Строка,** содержаная имя пользователя для ожидающих подключений.</span><span class="sxs-lookup"><span data-stu-id="cc546-113">A **String** that contains a user name for the pending connection.</span></span>|
|<span data-ttu-id="cc546-114">*Password*</span><span class="sxs-lookup"><span data-stu-id="cc546-114">*Password*</span></span> |<span data-ttu-id="cc546-115">**Строка,** содержаная пароль для ожидающих подключений.</span><span class="sxs-lookup"><span data-stu-id="cc546-115">A **String** that contains a password for the pending connection.</span></span>|
|<span data-ttu-id="cc546-116">*Options*</span><span class="sxs-lookup"><span data-stu-id="cc546-116">*Options*</span></span> |<span data-ttu-id="cc546-117">**Длинное** значение, которое указывает, как поставщик должен оценить *ConnectionString.*</span><span class="sxs-lookup"><span data-stu-id="cc546-117">A **Long** value that indicates how the provider should evaluate the *ConnectionString*.</span></span> <span data-ttu-id="cc546-118">Единственным вариантом **является adAsyncOpen.**</span><span class="sxs-lookup"><span data-stu-id="cc546-118">Your only option is **adAsyncOpen**.</span></span>|
|<span data-ttu-id="cc546-119">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="cc546-119">*adStatus*</span></span> |<span data-ttu-id="cc546-120">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="cc546-120">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="cc546-121">При этом событии этот параметр по умолчанию имеет значение **adStatusOK.**</span><span class="sxs-lookup"><span data-stu-id="cc546-121">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="cc546-122">Если событие не может запросить отмену ожидающей операции, ему задается **adStatusCantDeny.**</span><span class="sxs-lookup"><span data-stu-id="cc546-122">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span><br/><br/><span data-ttu-id="cc546-123">Перед возвращением этого события установите для этого параметра **параметр adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="cc546-123">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="cc546-124">Установите для этого параметра **параметр adStatusCancel,** чтобы запросить операцию подключения, которая вызвала отмену этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="cc546-124">Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>|
|<span data-ttu-id="cc546-125">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="cc546-125">*pConnection*</span></span> |<span data-ttu-id="cc546-126">Объект [Connection,](connection-object-ado.md) к которому применяется это уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="cc546-126">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span> <span data-ttu-id="cc546-127">Изменения параметров подключения  с помощью обработера **событий WillConnect** не влияют на **подключение.**</span><span class="sxs-lookup"><span data-stu-id="cc546-127">Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="cc546-128">Заметки</span><span class="sxs-lookup"><span data-stu-id="cc546-128">Remarks</span></span>

<span data-ttu-id="cc546-129">Когда **вызывается WillConnect,** параметры *ConnectionString,* *UserID,* *Password* и *Options* устанавливаются в значения, установленные операцией, которая вызвала это событие (ожидающие подключения), и могут быть изменены до возврата события.</span><span class="sxs-lookup"><span data-stu-id="cc546-129">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</span></span> <span data-ttu-id="cc546-130">**WillConnect** может возвращать запрос на отмену ожидающих подключений.</span><span class="sxs-lookup"><span data-stu-id="cc546-130">**WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="cc546-131">При отмене этого события будет вызван **ConnectComplete** с параметром *adStatus,* заданным **как adStatusErrorsOccurred.**</span><span class="sxs-lookup"><span data-stu-id="cc546-131">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

