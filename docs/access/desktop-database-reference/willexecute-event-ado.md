---
title: Событие WillExecute (ADO)
TOCTitle: WillExecute event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e4025645e5f8b12325ba20497ca6ef2b70175df
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919453"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="e8b41-102">Событие WillExecute (ADO)</span><span class="sxs-lookup"><span data-stu-id="e8b41-102">WillExecute event (ADO)</span></span>


<span data-ttu-id="e8b41-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8b41-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="e8b41-104">Событие **WillExecute** называется просто до выполнения ожидающие команды для подключения.</span><span class="sxs-lookup"><span data-stu-id="e8b41-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8b41-105">Syntax</span></span>

<span data-ttu-id="e8b41-106">*Источник*, *CursorType*WillExecute *LockType для*, *Параметры*, *adStatus*, *командной*, *pRecordset*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="e8b41-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="e8b41-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8b41-107">Parameters</span></span>

  - <span data-ttu-id="e8b41-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="e8b41-108">*Source*</span></span>

  - <span data-ttu-id="e8b41-109">**Строка** , содержащая команду SQL или хранимую процедуру имя.</span><span class="sxs-lookup"><span data-stu-id="e8b41-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="e8b41-110">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="e8b41-110">*CursorType*</span></span>

  - <span data-ttu-id="e8b41-111">[CursorTypeEnum](cursortypeenum.md) , которая содержит тип текущей позиции для **набора записей** , который будет открыт.</span><span class="sxs-lookup"><span data-stu-id="e8b41-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="e8b41-112">С помощью этого параметра можно изменить курсор к любому типу во время операции [открытия](open-method-ado-recordset.md) **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8b41-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="e8b41-113">*CursorType* будет игнорироваться для другой операции.</span><span class="sxs-lookup"><span data-stu-id="e8b41-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="e8b41-114">*LockType для*</span><span class="sxs-lookup"><span data-stu-id="e8b41-114">*LockType*</span></span>

  - <span data-ttu-id="e8b41-115">[LockTypeEnum](locktypeenum.md) , которая содержит тип блокировки для **набора записей** , который будет открыт.</span><span class="sxs-lookup"><span data-stu-id="e8b41-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="e8b41-116">С помощью этого параметра можно изменить блокировки к любому типу во время операции **открытия** **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e8b41-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="e8b41-117">*LockType для* будет игнорироваться для другой операции.</span><span class="sxs-lookup"><span data-stu-id="e8b41-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="e8b41-118">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="e8b41-118">*Options*</span></span>

  - <span data-ttu-id="e8b41-119">Значение типа **Long** , указывает параметры, которые можно использовать для выполнения команды или открыть **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="e8b41-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="e8b41-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="e8b41-120">*adStatus*</span></span>

  - [<span data-ttu-id="e8b41-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="e8b41-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="e8b41-122">Прежде чем возвращает это событие, присвойте этому параметру значение **adStatusUnwantedEvent** , чтобы запретить последующие уведомления или **adStatusCancel** для запроса отмены операцию, которая вызвала событие.</span><span class="sxs-lookup"><span data-stu-id="e8b41-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="e8b41-123">*Командной*</span><span class="sxs-lookup"><span data-stu-id="e8b41-123">*pCommand*</span></span>

  - <span data-ttu-id="e8b41-124">Объект [команды](command-object-ado.md) , для которого применяется этого уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="e8b41-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="e8b41-125">*pRecordset*</span><span class="sxs-lookup"><span data-stu-id="e8b41-125">*pRecordset*</span></span>

  - <span data-ttu-id="e8b41-126">Объект [набора записей](recordset-object-ado.md) , к которому применяется этот уведомления о событии.</span><span class="sxs-lookup"><span data-stu-id="e8b41-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="e8b41-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="e8b41-127">*pConnection*</span></span>

  - <span data-ttu-id="e8b41-128">Объект [подключения](connection-object-ado.md) , для которого применяется этого уведомления о событиях.</span><span class="sxs-lookup"><span data-stu-id="e8b41-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8b41-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8b41-129">Remarks</span></span>

<span data-ttu-id="e8b41-130">Событие **WillExecute** могут возникнуть из-за **подключения.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **команда.** [Выполнение](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), или **набора записей.** Метод [Open](open-method-ado-recordset.md) параметр *pConnection* всегда должен содержать ссылку на допустимый объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="e8b41-130">A **WillExecute** event may occur due to a **Connection.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection), **Command.**[Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="e8b41-131">Если событие из-за **Connection.Execute** *pRecordset* и *командной* — значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="e8b41-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="e8b41-132">Если событие из-за **Recordset.Open**параметр *pRecordset* ссылается на объект **набора записей** , параметр *командной* задано значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="e8b41-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="e8b41-133">Если событие из-за **Command.Execute**, параметр *командной* ссылаются на объект **команды** и *pRecordset* параметру присвоено значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="e8b41-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="e8b41-134">**WillExecute** позволяет проверять и изменять параметры ожидающих выполнения.</span><span class="sxs-lookup"><span data-stu-id="e8b41-134">**WillExecute** allows you to examine and modify the pending execution parameters.</span></span> <span data-ttu-id="e8b41-135">Это событие может возвратить запрос на отменить ожидающие команды.</span><span class="sxs-lookup"><span data-stu-id="e8b41-135">This event may return a request that the pending command be canceled.</span></span>

