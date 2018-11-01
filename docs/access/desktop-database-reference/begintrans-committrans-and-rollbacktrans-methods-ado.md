---
title: BeginTrans CommitTrans и методы RollbackTrans (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68e827f6177c0ea90d4dd8d74c9782d552b3fdd2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884669"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="94fe4-102">BeginTrans CommitTrans и методы RollbackTrans (ADO)</span><span class="sxs-lookup"><span data-stu-id="94fe4-102">BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)</span></span>


<span data-ttu-id="94fe4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94fe4-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="94fe4-104">Эти методы транзакций управление транзакций обработка объект [подключения](connection-object-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="94fe4-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

  - <span data-ttu-id="94fe4-105">**BeginTrans** — начало новой транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-105">**BeginTrans** — Begins a new transaction.</span></span>

  - <span data-ttu-id="94fe4-106">**CommitTrans** — сохраняет все изменения и заканчивающейся текущей операции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-106">**CommitTrans** — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="94fe4-107">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="94fe4-107">It may also start a new transaction.</span></span>

  - <span data-ttu-id="94fe4-108">**RollbackTrans** — показано, как отменить все изменения, внесенные во время текущей операции и заканчивающейся транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-108">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction.</span></span> <span data-ttu-id="94fe4-109">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="94fe4-109">It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="94fe4-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94fe4-110">Syntax</span></span>

<span data-ttu-id="94fe4-111">*уровень* = *объектов*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="94fe4-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="94fe4-112">*объект*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="94fe4-112">*object*.BeginTrans</span></span>

<span data-ttu-id="94fe4-113">*объект*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="94fe4-113">*object*.CommitTrans</span></span>

<span data-ttu-id="94fe4-114">*объект*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="94fe4-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="94fe4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94fe4-115">Return value</span></span>

<span data-ttu-id="94fe4-116">**BeginTrans** можно вызывать как функцию, которая возвращает **длинный** переменной, указывающее уровень вложенности транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="94fe4-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="94fe4-117">Parameters</span></span>

  - <span data-ttu-id="94fe4-118">*object*</span><span class="sxs-lookup"><span data-stu-id="94fe4-118">*object*</span></span>

  - <span data-ttu-id="94fe4-119">Объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="94fe4-119">A **Connection** object.</span></span>

<span data-ttu-id="94fe4-120">**Подключение**</span><span class="sxs-lookup"><span data-stu-id="94fe4-120">**Connection**</span></span>

<span data-ttu-id="94fe4-121">Использование этих методов с объектом **подключения** необходимо сохранить или отменить ряд изменений, внесенных в источник данных как единый элемент.</span><span class="sxs-lookup"><span data-stu-id="94fe4-121">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit.</span></span> <span data-ttu-id="94fe4-122">К примеру деньги переключение между учетными записями, вы вычесть сумму из одного и добавьте совпадает со значением в другой.</span><span class="sxs-lookup"><span data-stu-id="94fe4-122">For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</span></span> <span data-ttu-id="94fe4-123">Если либо обновить возникает ошибка, больше не сбалансировать учетные записи.</span><span class="sxs-lookup"><span data-stu-id="94fe4-123">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="94fe4-124">Эти изменения в открытую операцию гарантирует, что все или изменения проходят через.</span><span class="sxs-lookup"><span data-stu-id="94fe4-124">Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>


> [!NOTE]
> <span data-ttu-id="94fe4-125">Не все поставщики поддерживают транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-125">Not all providers support transactions.</span></span> <span data-ttu-id="94fe4-126">Убедитесь, что поставщик, определенный «**DDL транзакций**» отображается в коллекции [свойств](properties-collection-ado.md) объекта **подключения** , указывающего на то, что поставщик поддерживает транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-126">Verify that the provider-defined property "**Transaction DDL**" appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions.</span></span> <span data-ttu-id="94fe4-127">Если поставщик поддерживает транзакции, вызвав один из этих методов возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="94fe4-127">If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="94fe4-128">После вызова метода **BeginTrans** поставщик фиксируется больше не мгновенно изменения, внесенные, пока не будет вызван **CommitTrans** или **RollbackTrans** для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-128">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="94fe4-129">Для поставщиков, которые поддерживают вложенные транзакции вызов метода **BeginTrans** open транзакции начинается новый, вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="94fe4-129">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction.</span></span> <span data-ttu-id="94fe4-130">Возвращаемое значение указывает уровня вложенности: возвращаемое значение «1» указывает, был открыт верхнего уровня транзакций (то есть транзакция не вложен в другой транзакции), «2» указывает, что был открыт второго уровня транзакций ( транзакций, включенная в верхнего уровня транзакций), и т. д.</span><span class="sxs-lookup"><span data-stu-id="94fe4-130">The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</span></span> <span data-ttu-id="94fe4-131">Вызов **CommitTrans** или **RollbackTrans** влияет на недавно открытых транзакций; необходимо закрыть или отката текущей операции, чтобы связать любой транзакции более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="94fe4-131">Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="94fe4-132">Вызов метода **CommitTrans** сохраняет изменения, внесенные в открытую операцию для подключения и заканчивающейся транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-132">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction.</span></span> <span data-ttu-id="94fe4-133">Вызов метода **RollbackTrans** отменяет все изменения, внесенные в открытую операцию и заканчивающейся транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-133">Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction.</span></span> <span data-ttu-id="94fe4-134">Вызов любой из методов, когда нет open транзакции приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="94fe4-134">Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="94fe4-135">В зависимости от того, свойство [Attributes](attributes-property-ado.md) объект **подключения** вызов методов параметр **CommitTrans** или **RollbackTrans** автоматически запускать новые транзакции.</span><span class="sxs-lookup"><span data-stu-id="94fe4-135">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction.</span></span> <span data-ttu-id="94fe4-136">Если свойство **Attributes** **adXactCommitRetaining**, поставщик автоматически запускает новую транзакцию после **CommitTrans** вызова.</span><span class="sxs-lookup"><span data-stu-id="94fe4-136">If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call.</span></span> <span data-ttu-id="94fe4-137">Если свойство **Attributes** **adXactAbortRetaining**, поставщик автоматически запускает новую транзакцию после вызова **RollbackTrans** .</span><span class="sxs-lookup"><span data-stu-id="94fe4-137">If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

<span data-ttu-id="94fe4-138">**Службы удаленных данных**</span><span class="sxs-lookup"><span data-stu-id="94fe4-138">**Remote Data Service**</span></span>

<span data-ttu-id="94fe4-139">Методы **BeginTrans** **CommitTrans**и **RollbackTrans** недоступны на объект **подключения** со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="94fe4-139">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

