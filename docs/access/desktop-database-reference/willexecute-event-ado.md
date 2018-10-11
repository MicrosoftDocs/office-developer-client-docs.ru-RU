---
title: WillExecute Event (ADO)
TOCTitle: WillExecute Event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a5c739ffd408a1f53539c88a3bdc4169eb4cebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480103"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="bbd74-102">WillExecute Event (ADO)</span><span class="sxs-lookup"><span data-stu-id="bbd74-102">WillExecute Event (ADO)</span></span>


<span data-ttu-id="bbd74-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbd74-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="bbd74-104">Событие **WillExecute** называется просто до выполнения ожидающие команды для подключения.</span><span class="sxs-lookup"><span data-stu-id="bbd74-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbd74-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bbd74-105">Syntax</span></span>

<span data-ttu-id="bbd74-106">*Источник*, *CursorType*WillExecute *LockType для*, *Параметры*, *adStatus*, *командной*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="bbd74-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="bbd74-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbd74-107">Parameters</span></span>

  - <span data-ttu-id="bbd74-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="bbd74-108">*Source*</span></span>

  - <span data-ttu-id="bbd74-109">**Строка** , содержащая команду SQL или хранимую процедуру имя.</span><span class="sxs-lookup"><span data-stu-id="bbd74-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="bbd74-110">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="bbd74-110">*CursorType*</span></span>

  - <span data-ttu-id="bbd74-111">[CursorTypeEnum](cursortypeenum.md) , которая содержит тип текущей позиции для **набора записей** , который будет открыт.</span><span class="sxs-lookup"><span data-stu-id="bbd74-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="bbd74-112">С помощью этого параметра можно изменить курсор к любому типу во время операции [открытия](open-method-ado-recordset.md) **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="bbd74-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="bbd74-113">*CursorType* будет игнорироваться для другой операции.</span><span class="sxs-lookup"><span data-stu-id="bbd74-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="bbd74-114">*LockType для*</span><span class="sxs-lookup"><span data-stu-id="bbd74-114">*LockType*</span></span>

  - <span data-ttu-id="bbd74-115">[LockTypeEnum](locktypeenum.md) , которая содержит тип блокировки для **набора записей** , который будет открыт.</span><span class="sxs-lookup"><span data-stu-id="bbd74-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="bbd74-116">С помощью этого параметра можно изменить блокировки к любому типу во время операции **открытия** **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="bbd74-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="bbd74-117">*LockType для* будет игнорироваться для другой операции.</span><span class="sxs-lookup"><span data-stu-id="bbd74-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="bbd74-118">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="bbd74-118">*Options*</span></span>

  - <span data-ttu-id="bbd74-119">Значение типа **Long** , указывает параметры, которые можно использовать для выполнения команды или открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="bbd74-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="bbd74-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="bbd74-120">*adStatus*</span></span>

  - [<span data-ttu-id="bbd74-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="bbd74-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="bbd74-122">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления или **adStatusCancel** для запроса отмены операцию, которая вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="bbd74-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="bbd74-123">*Командной*</span><span class="sxs-lookup"><span data-stu-id="bbd74-123">*pCommand*</span></span>

  - <span data-ttu-id="bbd74-124">Объект [команды](command-object-ado.md) , для которого применяется этого уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="bbd74-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="bbd74-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="bbd74-125">*pRecordset*</span></span>

  - <span data-ttu-id="bbd74-126">Объект [набора записей](recordset-object-ado.md) , к которому применяется этот уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="bbd74-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="bbd74-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="bbd74-127">*pConnection*</span></span>

  - <span data-ttu-id="bbd74-128">Объект [подключения](connection-object-ado.md) , для которого применяется этого уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="bbd74-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbd74-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="bbd74-129">Remarks</span></span>

<span data-ttu-id="bbd74-130">Событие **WillExecute** могут возникнуть из-за **подключения.** [Выполнение](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **команда.** [Выполнение](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), или **набора записей.** Метод [Open](open-method-ado-recordset.md) параметр *pConnection* всегда должен содержать ссылку на допустимый объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="bbd74-130">A **WillExecute** event may occur due to a **Connection.**[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **Command.**[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="bbd74-131">Если событие из-за **Connection.Execute** *pRecordset* и *командной* — значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="bbd74-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="bbd74-132">Если событие из-за **Recordset.Open**параметр *pRecordset* ссылается на объект **набора записей** , параметр *командной* задано значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="bbd74-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="bbd74-133">Если событие из-за **Command.Execute**, параметр *командной* ссылаются на объект **команды** и *pRecordset* параметру присвоено значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="bbd74-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="bbd74-134">**WillExecute** позволяет проверять и изменять параметры ожидающих выполнения.</span><span class="sxs-lookup"><span data-stu-id="bbd74-134">**WillExecute** allows you to examine and modify the pending execution parameters.</span></span> <span data-ttu-id="bbd74-135">Это событие может возвратить запрос на отменить ожидающие команды.</span><span class="sxs-lookup"><span data-stu-id="bbd74-135">This event may return a request that the pending command be canceled.</span></span>

