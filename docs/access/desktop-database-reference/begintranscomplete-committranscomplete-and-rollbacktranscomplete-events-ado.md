---
title: События BeginTransComplete, CommitTransComplete, RollbackTransComplete (ADO)
TOCTitle: BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)
ms:assetid: 9d0ae38e-530a-7a89-a344-f3ab401c2e35
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249713(v=office.15)
ms:contentKeyID: 48546615
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6a49b08c1b4f7879d50f9dd1d29cfcf89ded50c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928083"
---
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="434ff-102">События BeginTransComplete, CommitTransComplete и RollbackTransComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="434ff-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>


<span data-ttu-id="434ff-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="434ff-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="434ff-104">Эти события будет вызван после завершения выполнения операцию связанный объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="434ff-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

  - <span data-ttu-id="434ff-105">После выполнения операции [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) называется **BeginTransComplete** .</span><span class="sxs-lookup"><span data-stu-id="434ff-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="434ff-106">После выполнения операции [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) называется **CommitTransComplete** .</span><span class="sxs-lookup"><span data-stu-id="434ff-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

  - <span data-ttu-id="434ff-107">**RollbackTransComplete** вызывается после операции [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="434ff-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="434ff-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="434ff-108">Syntax</span></span>

<span data-ttu-id="434ff-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="434ff-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="434ff-110">CommitTransComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="434ff-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="434ff-111">RollbackTransComplete*pError*, *adStatus* *pConnection*</span><span class="sxs-lookup"><span data-stu-id="434ff-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="434ff-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="434ff-112">Parameters</span></span>

  - <span data-ttu-id="434ff-113">*TransactionLevel*</span><span class="sxs-lookup"><span data-stu-id="434ff-113">*TransactionLevel*</span></span>

  - <span data-ttu-id="434ff-114">Значение типа **Long** , содержит новый уровень транзакций **BeginTrans** , вызвавшего это событие.</span><span class="sxs-lookup"><span data-stu-id="434ff-114">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>

  - <span data-ttu-id="434ff-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="434ff-115">*pError*</span></span>

  - <span data-ttu-id="434ff-116">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="434ff-116">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="434ff-117">Описание ошибки, возникшей при имеет значение EventStatusEnum **adStatusErrorsOccurred**; в противном случае он не задан.</span><span class="sxs-lookup"><span data-stu-id="434ff-117">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="434ff-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="434ff-118">*adStatus*</span></span>

  - [<span data-ttu-id="434ff-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="434ff-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="434ff-120">Эти события могут запретить последующие уведомления по этому параметру **adStatusUnwantedEvent** перед Возвращает событие.</span><span class="sxs-lookup"><span data-stu-id="434ff-120">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>

  - <span data-ttu-id="434ff-121">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="434ff-121">*pConnection*</span></span>

  - <span data-ttu-id="434ff-122">Объект **подключения** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="434ff-122">The **Connection** object for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="434ff-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="434ff-123">Remarks</span></span>

<span data-ttu-id="434ff-124">В Visual C++ несколько **подключения** могут совместно использовать же метод обработки событий.</span><span class="sxs-lookup"><span data-stu-id="434ff-124">In Visual C++, multiple **Connections** can share the same event handling method.</span></span> <span data-ttu-id="434ff-125">Метод использует возвращенный объект **подключения** для определения, какой объект вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="434ff-125">The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="434ff-126">Если свойство [Attributes](attributes-property-ado.md) **adXactCommitRetaining** или **adXactAbortRetaining**, новые транзакции начинается после фиксации или откате транзакции.</span><span class="sxs-lookup"><span data-stu-id="434ff-126">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction.</span></span> <span data-ttu-id="434ff-127">Используйте событие **BeginTransComplete** игнорировать все, но первое событие начала операции.</span><span class="sxs-lookup"><span data-stu-id="434ff-127">Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

