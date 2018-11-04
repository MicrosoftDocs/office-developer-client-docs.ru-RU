---
title: Методы BeginTrans, CommitTrans и RollbackTrans (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f6e797865889bcf52c6f13e4411e945a72b978e8
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949994"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="0fbc8-102">Методы BeginTrans, CommitTrans и RollbackTrans (ADO)</span><span class="sxs-lookup"><span data-stu-id="0fbc8-102">BeginTrans, CommitTrans, and RollbackTrans methods (ADO)</span></span>

<span data-ttu-id="0fbc8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fbc8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0fbc8-104">Эти методы транзакций управление транзакций обработка объект [подключения](connection-object-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0fbc8-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

- <span data-ttu-id="0fbc8-105">**BeginTrans** — начало новой транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-105">**BeginTrans** — Begins a new transaction.</span></span>

- <span data-ttu-id="0fbc8-106">**CommitTrans** — сохраняет все изменения и заканчивающейся текущей операции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-106">**CommitTrans** — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="0fbc8-107">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-107">It may also start a new transaction.</span></span>

- <span data-ttu-id="0fbc8-108">**RollbackTrans** — показано, как отменить все изменения, внесенные во время текущей операции и заканчивающейся транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-108">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction.</span></span> <span data-ttu-id="0fbc8-109">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-109">It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fbc8-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fbc8-110">Syntax</span></span>

<span data-ttu-id="0fbc8-111">*уровень* = *объектов*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="0fbc8-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="0fbc8-112">*объект*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="0fbc8-112">*object*.BeginTrans</span></span>

<span data-ttu-id="0fbc8-113">*объект*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="0fbc8-113">*object*.CommitTrans</span></span>

<span data-ttu-id="0fbc8-114">*объект*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="0fbc8-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="0fbc8-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fbc8-115">Return value</span></span>

<span data-ttu-id="0fbc8-116">**BeginTrans** можно вызывать как функцию, которая возвращает **длинный** переменной, указывающее уровень вложенности транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fbc8-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fbc8-117">Parameters</span></span>

|<span data-ttu-id="0fbc8-118">Параметр</span><span class="sxs-lookup"><span data-stu-id="0fbc8-118">Parameter</span></span>|<span data-ttu-id="0fbc8-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0fbc8-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="0fbc8-120">*object*</span><span class="sxs-lookup"><span data-stu-id="0fbc8-120">*object*</span></span> |<span data-ttu-id="0fbc8-121">Объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="0fbc8-121">A **Connection** object.</span></span>|

### <a name="connection"></a><span data-ttu-id="0fbc8-122">Подключение</span><span class="sxs-lookup"><span data-stu-id="0fbc8-122">Connection</span></span>

<span data-ttu-id="0fbc8-123">Использование этих методов с объектом **подключения** необходимо сохранить или отменить ряд изменений, внесенных в источник данных как единый элемент.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-123">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit.</span></span> <span data-ttu-id="0fbc8-124">К примеру деньги переключение между учетными записями, вы вычесть сумму из одного и добавьте совпадает со значением в другой.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-124">For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</span></span> <span data-ttu-id="0fbc8-125">Если либо обновить возникает ошибка, больше не сбалансировать учетные записи.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-125">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="0fbc8-126">Эти изменения в открытую операцию гарантирует, что все или изменения проходят через.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-126">Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>

> [!NOTE]
> <span data-ttu-id="0fbc8-127">Не все поставщики поддерживают транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-127">Not all providers support transactions.</span></span> <span data-ttu-id="0fbc8-128">Убедитесь, что поставщик, определенный **DDL транзакций** отображается в коллекции [свойств](properties-collection-ado.md) объекта **подключения** , указывающего на то, что поставщик поддерживает транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-128">Verify that the provider-defined property **Transaction DDL** appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions.</span></span> <span data-ttu-id="0fbc8-129">Если поставщик поддерживает транзакции, вызвав один из этих методов возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-129">If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="0fbc8-130">После вызова метода **BeginTrans** поставщик фиксируется больше не мгновенно изменения, внесенные, пока не будет вызван **CommitTrans** или **RollbackTrans** для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-130">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="0fbc8-131">Для поставщиков, которые поддерживают вложенные транзакции вызов метода **BeginTrans** open транзакции начинается новый, вложенных транзакций.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-131">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction.</span></span> <span data-ttu-id="0fbc8-132">Возвращаемое значение указывает уровня вложенности: возвращаемое значение «1» указывает, был открыт верхнего уровня транзакций (то есть транзакция не вложен в другой транзакции), «2» указывает, что был открыт второго уровня транзакций ( транзакций, включенная в верхнего уровня транзакций), и т. д.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-132">The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</span></span> <span data-ttu-id="0fbc8-133">Вызов **CommitTrans** или **RollbackTrans** влияет на недавно открытых транзакций; необходимо закрыть или отката текущей операции, чтобы связать любой транзакции более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-133">Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="0fbc8-134">Вызов метода **CommitTrans** сохраняет изменения, внесенные в открытую операцию для подключения и заканчивающейся транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-134">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction.</span></span> <span data-ttu-id="0fbc8-135">Вызов метода **RollbackTrans** отменяет все изменения, внесенные в открытую операцию и заканчивающейся транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-135">Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction.</span></span> <span data-ttu-id="0fbc8-136">Вызов любой из методов, когда нет open транзакции приведет к ошибке.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-136">Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="0fbc8-137">В зависимости от того, свойство [Attributes](attributes-property-ado.md) объект **подключения** вызов методов параметр **CommitTrans** или **RollbackTrans** автоматически запускать новые транзакции.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-137">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction.</span></span> <span data-ttu-id="0fbc8-138">Если свойство **Attributes** **adXactCommitRetaining**, поставщик автоматически запускает новую транзакцию после **CommitTrans** вызова.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-138">If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call.</span></span> <span data-ttu-id="0fbc8-139">Если свойство **Attributes** **adXactAbortRetaining**, поставщик автоматически запускает новую транзакцию после вызова **RollbackTrans** .</span><span class="sxs-lookup"><span data-stu-id="0fbc8-139">If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

### <a name="remote-data-service"></a><span data-ttu-id="0fbc8-140">Службы удаленных данных</span><span class="sxs-lookup"><span data-stu-id="0fbc8-140">Remote Data Service</span></span>

<span data-ttu-id="0fbc8-141">Методы **BeginTrans** **CommitTrans**и **RollbackTrans** недоступны на объект **подключения** со стороны клиента.</span><span class="sxs-lookup"><span data-stu-id="0fbc8-141">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

