---
title: События begintranscomplete, CommitTransComplete, RollbackTransComplete события (ADO)
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
# <a name="begintranscomplete-committranscomplete-and-rollbacktranscomplete-events-ado"></a><span data-ttu-id="de7aa-102">События события begintranscomplete, CommitTransComplete и RollbackTransComplete (ADO)</span><span class="sxs-lookup"><span data-stu-id="de7aa-102">BeginTransComplete, CommitTransComplete, and RollbackTransComplete events (ADO)</span></span>

<span data-ttu-id="de7aa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="de7aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="de7aa-104">Эти события будут вызваны после завершения выполнения связанной операции над объектом [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="de7aa-104">These events will be called after the associated operation on the [Connection](connection-object-ado.md) object finishes executing.</span></span>

- <span data-ttu-id="de7aa-105">**События begintranscomplete** вызывается после операции [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="de7aa-105">**BeginTransComplete** is called after the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="de7aa-106">**CommitTransComplete** вызывается после операции [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="de7aa-106">**CommitTransComplete** is called after the [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

- <span data-ttu-id="de7aa-107">**RollbackTransComplete** вызывается после операции [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="de7aa-107">**RollbackTransComplete** is called after the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="de7aa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de7aa-108">Syntax</span></span>

<span data-ttu-id="de7aa-109">События begintranscomplete*трансактионлевел*, *перрор*, *адстатус*, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="de7aa-109">BeginTransComplete*TransactionLevel*, *pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="de7aa-110">CommitTransComplete*перрор*, *адстатус*, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="de7aa-110">CommitTransComplete*pError*, *adStatus*, *pConnection*</span></span>

<span data-ttu-id="de7aa-111">RollbackTransComplete*перрор*, *адстатус*, *пконнектион*</span><span class="sxs-lookup"><span data-stu-id="de7aa-111">RollbackTransComplete*pError*, *adStatus*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="de7aa-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="de7aa-112">Parameters</span></span>

|<span data-ttu-id="de7aa-113">Параметр</span><span class="sxs-lookup"><span data-stu-id="de7aa-113">Parameter</span></span>|<span data-ttu-id="de7aa-114">Описание</span><span class="sxs-lookup"><span data-stu-id="de7aa-114">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="de7aa-115">*трансактионлевел*</span><span class="sxs-lookup"><span data-stu-id="de7aa-115">*TransactionLevel*</span></span> |<span data-ttu-id="de7aa-116">**Длинное** значение, которое содержит новый уровень транзакций **BeginTrans** , вызвавших это событие.</span><span class="sxs-lookup"><span data-stu-id="de7aa-116">A **Long** value that contains the new transaction level of the **BeginTrans** that caused this event.</span></span>|
|<span data-ttu-id="de7aa-117">*перрор*</span><span class="sxs-lookup"><span data-stu-id="de7aa-117">*pError*</span></span> |<span data-ttu-id="de7aa-118">Объект [Error](error-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="de7aa-118">An [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="de7aa-119">В нем описывается ошибка, которая возникла, если значение Евентстатусенум равно **адстатусеррорсоккурред**; в противном случае он не задается.</span><span class="sxs-lookup"><span data-stu-id="de7aa-119">It describes the error that occurred if the value of EventStatusEnum is **adStatusErrorsOccurred**; otherwise, it is not set.</span></span>|
|<span data-ttu-id="de7aa-120">*адстатус*</span><span class="sxs-lookup"><span data-stu-id="de7aa-120">*adStatus*</span></span> |<span data-ttu-id="de7aa-121">[Евентстатусенум](eventstatusenum.md).</span><span class="sxs-lookup"><span data-stu-id="de7aa-121">[EventStatusEnum](eventstatusenum.md).</span></span> <span data-ttu-id="de7aa-122">Эти события могут препятствовать последующим уведомлениям, присвоив этому параметру значение **адстатусунвантедевент** , прежде чем событие будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="de7aa-122">These events can prevent subsequent notifications by setting this parameter to **adStatusUnwantedEvent** before the event returns.</span></span>|
|<span data-ttu-id="de7aa-123">*пконнектион*</span><span class="sxs-lookup"><span data-stu-id="de7aa-123">*pConnection*</span></span> |<span data-ttu-id="de7aa-124">Объект **Connection** , для которого произошло это событие.</span><span class="sxs-lookup"><span data-stu-id="de7aa-124">The **Connection** object for which this event occurred.</span></span>|

## <a name="remarks"></a><span data-ttu-id="de7aa-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="de7aa-125">Remarks</span></span>

<span data-ttu-id="de7aa-126">В Visual C++ несколько **подключений** могут совместно использовать один метод обработки события.</span><span class="sxs-lookup"><span data-stu-id="de7aa-126">In Visual C++, multiple **Connections** can share the same event handling method.</span></span> <span data-ttu-id="de7aa-127">Метод использует возвращенный объект **Connection** для определения объекта, вызвавшего событие.</span><span class="sxs-lookup"><span data-stu-id="de7aa-127">The method uses the returned **Connection** object to determine which object caused the event.</span></span>

<span data-ttu-id="de7aa-128">Если для свойства [Attributes](attributes-property-ado.md) задано значение **адксакткоммитретаининг** или **адксактабортретаининг**, Новая транзакция начинается после фиксации или отката транзакции.</span><span class="sxs-lookup"><span data-stu-id="de7aa-128">If the [Attributes](attributes-property-ado.md) property is set to **adXactCommitRetaining** or **adXactAbortRetaining**, a new transaction starts after committing or rolling back a transaction.</span></span> <span data-ttu-id="de7aa-129">Используйте событие **события begintranscomplete** для пропуска всех событий запуска Transaction, кроме первого.</span><span class="sxs-lookup"><span data-stu-id="de7aa-129">Use the **BeginTransComplete** event to ignore all but the first transaction start event.</span></span>

