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
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="14586-102">Методы BeginTrans, CommitTrans и RollbackTrans (ADO)</span><span class="sxs-lookup"><span data-stu-id="14586-102">BeginTrans, CommitTrans, and RollbackTrans methods (ADO)</span></span>

<span data-ttu-id="14586-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14586-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14586-104">Эти методы транзакции управляют обработкой транзакций в [объекте Подключения](connection-object-ado.md) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="14586-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

- <span data-ttu-id="14586-105">**BeginTrans** — начинается новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="14586-105">**BeginTrans** — Begins a new transaction.</span></span>

- <span data-ttu-id="14586-106">**CommitTrans** — сохраняет все изменения и завершает текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="14586-106">**CommitTrans** — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="14586-107">Кроме того, может начаться новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="14586-107">It may also start a new transaction.</span></span>

- <span data-ttu-id="14586-108">**RollbackTrans** — отменяет изменения, внесенные во время текущей транзакции, и завершает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="14586-108">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction.</span></span> <span data-ttu-id="14586-109">Кроме того, может начаться новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="14586-109">It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="14586-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14586-110">Syntax</span></span>

<span data-ttu-id="14586-111">*уровень*  =  *объект*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="14586-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="14586-112">*объект*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="14586-112">*object*.BeginTrans</span></span>

<span data-ttu-id="14586-113">*объект*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="14586-113">*object*.CommitTrans</span></span>

<span data-ttu-id="14586-114">*объект*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="14586-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="14586-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14586-115">Return value</span></span>

<span data-ttu-id="14586-116">**BeginTrans** можно назвать функцией, возвращаемой переменной **Long,** указывающей уровень вложения транзакции.</span><span class="sxs-lookup"><span data-stu-id="14586-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="14586-117">Параметры</span><span class="sxs-lookup"><span data-stu-id="14586-117">Parameters</span></span>

|<span data-ttu-id="14586-118">Параметр</span><span class="sxs-lookup"><span data-stu-id="14586-118">Parameter</span></span>|<span data-ttu-id="14586-119">Описание</span><span class="sxs-lookup"><span data-stu-id="14586-119">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="14586-120">*object*</span><span class="sxs-lookup"><span data-stu-id="14586-120">*object*</span></span> |<span data-ttu-id="14586-121">Объект **Подключения.**</span><span class="sxs-lookup"><span data-stu-id="14586-121">A **Connection** object.</span></span>|

### <a name="connection"></a><span data-ttu-id="14586-122">Connection</span><span class="sxs-lookup"><span data-stu-id="14586-122">Connection</span></span>

<span data-ttu-id="14586-123">Используйте эти методы с объектом **Connection,** если необходимо сохранить или отменить ряд изменений, внесенных в исходные данные в качестве единого блока.</span><span class="sxs-lookup"><span data-stu-id="14586-123">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit.</span></span> <span data-ttu-id="14586-124">Например, чтобы перевести деньги между счетами, вычитайте сумму из одной и добавьте ту же сумму в другую.</span><span class="sxs-lookup"><span data-stu-id="14586-124">For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other.</span></span> <span data-ttu-id="14586-125">Если обновление не удается, учетные записи перестают балансировать.</span><span class="sxs-lookup"><span data-stu-id="14586-125">If either update fails, the accounts no longer balance.</span></span> <span data-ttu-id="14586-126">Внесение этих изменений в открытую транзакцию гарантирует, что все или никакие изменения не будут проходить.</span><span class="sxs-lookup"><span data-stu-id="14586-126">Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>

> [!NOTE]
> <span data-ttu-id="14586-127">Не все поставщики поддерживают транзакции.</span><span class="sxs-lookup"><span data-stu-id="14586-127">Not all providers support transactions.</span></span> <span data-ttu-id="14586-128">Убедитесь, что **DDL** транзакции с определенным поставщиком свойства отображается в коллекции [свойств](properties-collection-ado.md) объекта **Connection,** указав, что поставщик поддерживает транзакции.</span><span class="sxs-lookup"><span data-stu-id="14586-128">Verify that the provider-defined property **Transaction DDL** appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions.</span></span> <span data-ttu-id="14586-129">Если поставщик не поддерживает транзакции, вызов одного из этих методов возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="14586-129">If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="14586-130">После вызова метода **BeginTrans** поставщик больше не будет мгновенно совершать изменения, внесенные до вызова **CommitTrans** или **RollbackTrans** для окончания транзакции.</span><span class="sxs-lookup"><span data-stu-id="14586-130">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="14586-131">Для поставщиков, которые поддерживают вложенные транзакции, вызов метода **BeginTrans** в рамках открытой транзакции запускает новую вложенную транзакцию.</span><span class="sxs-lookup"><span data-stu-id="14586-131">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction.</span></span> <span data-ttu-id="14586-132">Возвращаемая величина указывает уровень вложения: значение возврата "1" указывает, что вы открыли транзакцию верхнего уровня (то есть транзакция не вложена в другую транзакцию), "2" указывает, что вы открыли транзакцию второго уровня (транзакция, вложенная в транзакцию верхнего уровня) и так далее.</span><span class="sxs-lookup"><span data-stu-id="14586-132">The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth.</span></span> <span data-ttu-id="14586-133">Вызов **CommitTrans или** **RollbackTrans** влияет только на недавно открытую транзакцию; необходимо закрыть или откатить текущую транзакцию, прежде чем разрешить любые транзакции более высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="14586-133">Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="14586-134">Вызов метода **CommitTrans позволяет** сохранить изменения, внесенные в открытой транзакции, на подключении и завершает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="14586-134">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction.</span></span> <span data-ttu-id="14586-135">Вызов метода **RollbackTrans отменяет** все изменения, внесенные в открытой транзакции, и завершает транзакцию.</span><span class="sxs-lookup"><span data-stu-id="14586-135">Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction.</span></span> <span data-ttu-id="14586-136">Вызов любого метода при отсутствие открытой транзакции создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="14586-136">Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="14586-137">В зависимости от свойства [](attributes-property-ado.md) **Атрибуты** объекта Подключения вызов методов **CommitTrans** или **RollbackTrans** может автоматически запускать новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="14586-137">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction.</span></span> <span data-ttu-id="14586-138">Если свойство **Attributes** настроено на **adXactCommitRetaining,** поставщик автоматически запускает новую транзакцию после вызова **CommitTrans.**</span><span class="sxs-lookup"><span data-stu-id="14586-138">If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call.</span></span> <span data-ttu-id="14586-139">Если свойство **Attributes** настроено на **adXactAbortRetaining,** поставщик автоматически запускает новую транзакцию после вызова **RollbackTrans.**</span><span class="sxs-lookup"><span data-stu-id="14586-139">If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

### <a name="remote-data-service"></a><span data-ttu-id="14586-140">Служба удаленных данных</span><span class="sxs-lookup"><span data-stu-id="14586-140">Remote Data Service</span></span>

<span data-ttu-id="14586-141">Методы **BeginTrans,** **CommitTrans** и **RollbackTrans** недоступны для объекта клиентского **подключения.**</span><span class="sxs-lookup"><span data-stu-id="14586-141">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

