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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305889"
---
# <a name="willconnect-event-ado"></a><span data-ttu-id="12dc0-102">Событие WillConnect (ADO)</span><span class="sxs-lookup"><span data-stu-id="12dc0-102">WillConnect event (ADO)</span></span>

<span data-ttu-id="12dc0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="12dc0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="12dc0-104">Событие **WillConnect** вызвано перед началом подключения.</span><span class="sxs-lookup"><span data-stu-id="12dc0-104">The **WillConnect** event is called before a connection starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="12dc0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12dc0-105">Syntax</span></span>

<span data-ttu-id="12dc0-106">WillConnect *ConnectionString*, *UserID*, *Пароль*, *Параметры*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="12dc0-106">WillConnect *ConnectionString*, *UserID*, *Password*, *Options*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="12dc0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="12dc0-107">Parameters</span></span>

|<span data-ttu-id="12dc0-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="12dc0-108">Parameter</span></span>|<span data-ttu-id="12dc0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="12dc0-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="12dc0-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="12dc0-110">*ConnectionString*</span></span> |<span data-ttu-id="12dc0-111">**Строка,** содержаная сведения о подключении для ожидающих подключения.</span><span class="sxs-lookup"><span data-stu-id="12dc0-111">A **String** that contains connection information for the pending connection.</span></span>|
|<span data-ttu-id="12dc0-112">*UserID*</span><span class="sxs-lookup"><span data-stu-id="12dc0-112">*UserID*</span></span> |<span data-ttu-id="12dc0-113">**Строка,** которая содержит имя пользователя для ожидающих подключения.</span><span class="sxs-lookup"><span data-stu-id="12dc0-113">A **String** that contains a user name for the pending connection.</span></span>|
|<span data-ttu-id="12dc0-114">*Password*</span><span class="sxs-lookup"><span data-stu-id="12dc0-114">*Password*</span></span> |<span data-ttu-id="12dc0-115">**Строка,** которая содержит пароль для ожидающих подключения.</span><span class="sxs-lookup"><span data-stu-id="12dc0-115">A **String** that contains a password for the pending connection.</span></span>|
|<span data-ttu-id="12dc0-116">*Options*</span><span class="sxs-lookup"><span data-stu-id="12dc0-116">*Options*</span></span> |<span data-ttu-id="12dc0-117">**Длинное** значение, которое указывает, как поставщик должен оценивать *ConnectionString.*</span><span class="sxs-lookup"><span data-stu-id="12dc0-117">A **Long** value that indicates how the provider should evaluate the *ConnectionString*.</span></span> <span data-ttu-id="12dc0-118">Единственным вариантом **является adAsyncOpen**.</span><span class="sxs-lookup"><span data-stu-id="12dc0-118">Your only option is **adAsyncOpen**.</span></span>|
|<span data-ttu-id="12dc0-119">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="12dc0-119">*adStatus*</span></span> |<span data-ttu-id="12dc0-120">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="12dc0-120">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="12dc0-121">Когда это событие называется, этот параметр по умолчанию задан **adStatusOK.**</span><span class="sxs-lookup"><span data-stu-id="12dc0-121">When this event is called, this parameter is set to **adStatusOK** by default.</span></span> <span data-ttu-id="12dc0-122">Он задается **adStatusCantDeny,** если событие не может запросить отмену ожидающей операции.</span><span class="sxs-lookup"><span data-stu-id="12dc0-122">It is set to **adStatusCantDeny** if the event cannot request cancellation of the pending operation.</span></span><br/><br/><span data-ttu-id="12dc0-123">Перед возвращением этого события установите этот параметр **adStatusUnwantedEvent,** чтобы предотвратить последующие уведомления.</span><span class="sxs-lookup"><span data-stu-id="12dc0-123">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span> <span data-ttu-id="12dc0-124">Установите этот параметр **в adStatusCancel** для запроса операции подключения, которая вызвала отмену этого уведомления.</span><span class="sxs-lookup"><span data-stu-id="12dc0-124">Set this parameter to **adStatusCancel** to request the connection operation that caused cancellation of this notification.</span></span>|
|<span data-ttu-id="12dc0-125">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="12dc0-125">*pConnection*</span></span> |<span data-ttu-id="12dc0-126">Объект [Connection,](connection-object-ado.md) для которого применяется это уведомление о событии.</span><span class="sxs-lookup"><span data-stu-id="12dc0-126">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span> <span data-ttu-id="12dc0-127">Изменения параметров подключения  обработиктором **событий WillConnect** не влияют на **подключение.**</span><span class="sxs-lookup"><span data-stu-id="12dc0-127">Changes to the parameters of the **Connection** by the **WillConnect** event handler will have no effect on the **Connection**.</span></span>|

## <a name="remarks"></a><span data-ttu-id="12dc0-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="12dc0-128">Remarks</span></span>

<span data-ttu-id="12dc0-129">Когда **вызывается WillConnect,** параметры *ConnectionString,* *UserID,* *Password* и *Options* заданы значениям, установленным операцией, которая вызвала это событие (ожидающий подключения), и могут быть изменены до возвращения события.</span><span class="sxs-lookup"><span data-stu-id="12dc0-129">When **WillConnect** is called, the *ConnectionString*, *UserID*, *Password*, and *Options* parameters are set to the values established by the operation that caused this event (the pending connection), and can be changed before the event returns.</span></span> <span data-ttu-id="12dc0-130">**WillConnect** может вернуть запрос об отмене ожидаемой подключения.</span><span class="sxs-lookup"><span data-stu-id="12dc0-130">**WillConnect** may return a request that the pending connection be canceled.</span></span>

<span data-ttu-id="12dc0-131">Когда это событие отменяется, **connectComplete** будет вызван с его *параметром adStatus,* заданным **adStatusErrorsOccurred**.</span><span class="sxs-lookup"><span data-stu-id="12dc0-131">When this event is canceled, **ConnectComplete** will be called with its *adStatus* parameter set to **adStatusErrorsOccurred**.</span></span>

