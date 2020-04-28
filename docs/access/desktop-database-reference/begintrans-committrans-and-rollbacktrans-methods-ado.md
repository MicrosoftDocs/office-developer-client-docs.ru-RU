---
title: Методы BeginTrans, CommitTrans и RollbackTrans (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d9dc28bd64966e85d16ee2d8cb62fdebc3ba942
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296873"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="5d5bc-102">Методы BeginTrans, CommitTrans и RollbackTrans (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d5bc-102">BeginTrans, CommitTrans, and RollbackTrans methods (ADO)</span></span>

<span data-ttu-id="5d5bc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d5bc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d5bc-104">Эти методы транзакции управляют обработкой транзакций в объекте [Connection](connection-object-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5d5bc-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

- <span data-ttu-id="5d5bc-105">**BeginTrans** — начинает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-105">**BeginTrans** — Begins a new transaction.</span></span>

- <span data-ttu-id="5d5bc-106">**CommitTrans** — сохраняет все изменения и завершает текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-106">**CommitTrans** — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="5d5bc-107">Кроме того, может начаться новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-107">It may also start a new transaction.</span></span>

- <span data-ttu-id="5d5bc-108">**RollbackTrans** — отменяет все изменения, внесенные во время текущей транзакции, и завершает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-108">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction.</span></span> <span data-ttu-id="5d5bc-109">Кроме того, может начаться новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-109">It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d5bc-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d5bc-110">Syntax</span></span>

<span data-ttu-id="5d5bc-111">*level* = *объект*Level. BeginTrans ()</span><span class="sxs-lookup"><span data-stu-id="5d5bc-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="5d5bc-112">*объект*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="5d5bc-112">*object*.BeginTrans</span></span>

<span data-ttu-id="5d5bc-113">*объект*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="5d5bc-113">*object*.CommitTrans</span></span>

<span data-ttu-id="5d5bc-114">*объект*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="5d5bc-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="5d5bc-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d5bc-115">Return value</span></span>

<span data-ttu-id="5d5bc-116">**BeginTrans** может вызываться в качестве функции, возвращающей **длинную** переменную, указывающую уровень вложенности транзакции.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d5bc-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d5bc-117">Parameters</span></span>

|<span data-ttu-id="5d5bc-118">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d5bc-118">Parameter</span></span>|<span data-ttu-id="5d5bc-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5d5bc-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5d5bc-120">*object*</span><span class="sxs-lookup"><span data-stu-id="5d5bc-120">*object*</span></span> |<span data-ttu-id="5d5bc-121">Объект **Connection** .</span><span class="sxs-lookup"><span data-stu-id="5d5bc-121">A **Connection** object.</span></span>|

### <a name="connection"></a><span data-ttu-id="5d5bc-122">Connection</span><span class="sxs-lookup"><span data-stu-id="5d5bc-122">Connection</span></span>

<span data-ttu-id="5d5bc-123">Используйте эти методы вместе с объектом **Connection** , если необходимо сохранить или отменить серию изменений, внесенных в источник данных, как единое целое.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-123">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit.</span></span> <span data-ttu-id="5d5bc-124">Например, чтобы перенести деньги между учетными записями, можно вычесть сумму из единицы и добавить одинаковую сумму к другому.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-124">For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</span></span> <span data-ttu-id="5d5bc-125">Если обновление завершается сбоем, учетные записи больше не сбалансированы.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-125">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="5d5bc-126">Внесение этих изменений в открытую транзакцию гарантирует, что все изменения не проходят или не проходят какие либо никакие изменения.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-126">Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>

> [!NOTE]
> <span data-ttu-id="5d5bc-127">Не все поставщики поддерживают транзакции.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-127">Not all providers support transactions.</span></span> <span data-ttu-id="5d5bc-128">Убедитесь, что в коллекции [свойств](properties-collection-ado.md) объекта **Connection** отображается **DDL** -свойство, заданное поставщиком, указывая, что поставщик поддерживает транзакции.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-128">Verify that the provider-defined property **Transaction DDL** appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions.</span></span> <span data-ttu-id="5d5bc-129">Если поставщик не поддерживает транзакции, то при вызове одного из этих методов возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-129">If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="5d5bc-130">После вызова метода **BeginTrans** поставщик больше не будет выполнять изменения, пока не будет вызвана **CommitTrans** или **RollbackTrans** для завершения транзакции.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-130">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="5d5bc-131">Для поставщиков, поддерживающих вложенные транзакции, вызов метода **BeginTrans** в открытой транзакции начинает новую вложенную транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-131">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction.</span></span> <span data-ttu-id="5d5bc-132">Возвращаемое значение указывает уровень вложенности: возвращаемое значение "1" указывает на то, что вы открыли транзакцию верхнего уровня (то есть транзакция не является вложенной в другую транзакцию), "2" означает, что вы открыли транзакцию второго уровня (транзакция, вложенная в транзакцию верхнего уровня) и так далее.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-132">The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</span></span> <span data-ttu-id="5d5bc-133">Вызов **CommitTrans** или **RollbackTrans** влияет только на самую последнюю открытую транзакцию; Прежде чем можно будет разрешить транзакции верхнего уровня, необходимо закрыть или откатить текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-133">Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="5d5bc-134">При вызове метода **CommitTrans** сохраняются изменения, внесенные в открытую транзакцию для подключения, и завершается транзакция.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-134">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction.</span></span> <span data-ttu-id="5d5bc-135">Вызов метода **RollbackTrans** отменяет все изменения, внесенные в открытую транзакцию, и завершает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-135">Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction.</span></span> <span data-ttu-id="5d5bc-136">Вызов любого метода при отсутствии открытой транзакции приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-136">Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="5d5bc-137">В зависимости от свойства [Attribute](attributes-property-ado.md) объекта **Connection** , вызов методов **CommitTrans** или **RollbackTrans** может автоматически запустить новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-137">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction.</span></span> <span data-ttu-id="5d5bc-138">Если для свойства **Attributes** задано значение **адксакткоммитретаининг**, поставщик автоматически запускает новую транзакцию после вызова **CommitTrans** .</span><span class="sxs-lookup"><span data-stu-id="5d5bc-138">If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call.</span></span> <span data-ttu-id="5d5bc-139">Если для свойства **Attributes** задано значение **адксактабортретаининг**, поставщик автоматически запускает новую транзакцию после вызова **RollbackTrans** .</span><span class="sxs-lookup"><span data-stu-id="5d5bc-139">If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

### <a name="remote-data-service"></a><span data-ttu-id="5d5bc-140">Удаленная служба данных</span><span class="sxs-lookup"><span data-stu-id="5d5bc-140">Remote Data Service</span></span>

<span data-ttu-id="5d5bc-141">Методы **BeginTrans**, **CommitTrans**и **RollbackTrans** недоступны для объекта **подключения** на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="5d5bc-141">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

