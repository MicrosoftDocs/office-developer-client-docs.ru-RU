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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296824"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="0fe6f-102">События BeginTransComplete, CommitTransComplete и RollbackTransComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="0fe6f-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>

<span data-ttu-id="0fe6f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fe6f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fe6f-104">Эти события будут вызваны после выполнения связанной операции на [объекте Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0fe6f-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

- <span data-ttu-id="0fe6f-105">**BeginTransComplete** вызван после операции [BeginTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0fe6f-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="0fe6f-106">**CommitTransComplete** вызван после операции [CommitTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0fe6f-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="0fe6f-107">**RollbackTransComplete** вызван после операции [RollbackTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0fe6f-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fe6f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fe6f-108">Syntax</span></span>

<span data-ttu-id="0fe6f-109">BeginTransComplete *TransactionLevel*, *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="0fe6f-109">BeginTransComplete *TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="0fe6f-110">CommitTransComplete *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="0fe6f-110">CommitTransComplete *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="0fe6f-111">RollbackTransComplete *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="0fe6f-111">RollbackTransComplete *pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="0fe6f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fe6f-112">Parameters</span></span>

|<span data-ttu-id="0fe6f-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="0fe6f-113">Parameter</span></span>|<span data-ttu-id="0fe6f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="0fe6f-114">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0fe6f-115">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="0fe6f-115">*TransactionLevel*</span></span> |<span data-ttu-id="0fe6f-116">**Длинное** значение, содержаное новый уровень транзакции **BeginTrans,** вызвав этот случай.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-116">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>|
|<span data-ttu-id="0fe6f-117">*pError*</span><span class="sxs-lookup"><span data-stu-id="0fe6f-117">*pError*</span></span> |<span data-ttu-id="0fe6f-118">Объект [Ошибки.](error-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0fe6f-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="0fe6f-119">Он описывает ошибку, которая произошла, если значение EventStatusEnum **adStatusErrorsOccurred;** в противном случае это не установлено.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-119">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise, it is not set.</span></span>|
|<span data-ttu-id="0fe6f-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="0fe6f-120">*adStatus*</span></span> |<span data-ttu-id="0fe6f-121">[EventStatusEnum](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="0fe6f-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="0fe6f-122">Эти события могут предотвратить последующие уведомления, задав этот параметр **adStatusUnwantedEvent** перед возвращением события.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-122">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>|
|<span data-ttu-id="0fe6f-123">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="0fe6f-123">*pConnection*</span></span> |<span data-ttu-id="0fe6f-124">Объект **Connection,** для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-124">The **Connection** object for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="0fe6f-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="0fe6f-125">Remarks</span></span>

<span data-ttu-id="0fe6f-126">В Visual C++несколько **подключений** могут использовать один и тот же метод обработки событий.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-126">In Visual C++, multiple **Connections** can share the same event handling method.</span></span> <span data-ttu-id="0fe6f-127">Метод использует возвращенный объект **Подключения,** чтобы определить, какой объект вызвал событие.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-127">The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="0fe6f-128">Если свойство [Attributes](attributes-property-ado.md) настроено на **adXactCommitRetaining** или **adXactAbortRetaining,** после совершения или отката транзакции начинается новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-128">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction.</span></span> <span data-ttu-id="0fe6f-129">Используйте событие **StartTransComplete,** чтобы игнорировать все события, кроме первого запуска транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fe6f-129">Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

