---
title: События BeginTransComplete, CommitTransComplete, RollbackTransComplete (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6f86e17a44ec0813176a023a02710fded627488
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702896"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="62b72-102">События BeginTransComplete, CommitTransComplete и RollbackTransComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="62b72-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>

<span data-ttu-id="62b72-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62b72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62b72-104">Эти события будет вызван после завершения выполнения операцию связанный объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="62b72-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

- <span data-ttu-id="62b72-105">После выполнения операции [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) называется **BeginTransComplete** .</span><span class="sxs-lookup"><span data-stu-id="62b72-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="62b72-106">После выполнения операции [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) называется **CommitTransComplete** .</span><span class="sxs-lookup"><span data-stu-id="62b72-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="62b72-107">**RollbackTransComplete** вызывается после операции [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="62b72-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b72-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62b72-108">Syntax</span></span>

<span data-ttu-id="62b72-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="62b72-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="62b72-110">CommitTransComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="62b72-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="62b72-111">RollbackTransComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="62b72-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="62b72-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="62b72-112">Parameters</span></span>

|<span data-ttu-id="62b72-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="62b72-113">Parameter</span></span>|<span data-ttu-id="62b72-114">Описание</span><span class="sxs-lookup"><span data-stu-id="62b72-114">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="62b72-115">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="62b72-115">*TransactionLevel*</span></span> |<span data-ttu-id="62b72-116">Значение типа **Long** , содержит новый уровень транзакций **BeginTrans** , вызвавшего это событие.</span><span class="sxs-lookup"><span data-stu-id="62b72-116">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>|
|<span data-ttu-id="62b72-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="62b72-117">*pError*</span></span> |<span data-ttu-id="62b72-118">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="62b72-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="62b72-119">Описание ошибки, возникшей при имеет значение EventStatusEnum **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="62b72-119">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise, it is not set.</span></span>|
|<span data-ttu-id="62b72-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="62b72-120">*adStatus*</span></span> |<span data-ttu-id="62b72-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="62b72-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="62b72-122">Эти события могут запретить последующие уведомления по этому параметру **adStatusUnwantedEvent** перед Возвращает событие.</span><span class="sxs-lookup"><span data-stu-id="62b72-122">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>|
|<span data-ttu-id="62b72-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="62b72-123">*pConnection*</span></span> |<span data-ttu-id="62b72-124">Объект **подключения** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="62b72-124">The **Connection** object for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="62b72-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="62b72-125">Remarks</span></span>

<span data-ttu-id="62b72-126">В Visual C++ несколько **подключения** могут совместно использовать же метод обработки событий.</span><span class="sxs-lookup"><span data-stu-id="62b72-126">In Visual C++, multiple **Connections** can share the same event handling method.</span></span> <span data-ttu-id="62b72-127">Метод использует возвращенный объект **подключения** для определения, какой объект вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="62b72-127">The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="62b72-128">Если свойство [Attributes](attributes-property-ado.md) **adXactCommitRetaining** или **adXactAbortRetaining**, новые транзакции начинается после фиксации или откате транзакции.</span><span class="sxs-lookup"><span data-stu-id="62b72-128">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction.</span></span> <span data-ttu-id="62b72-129">Используйте событие **BeginTransComplete** игнорировать все, но первое событие начала операции.</span><span class="sxs-lookup"><span data-stu-id="62b72-129">Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

