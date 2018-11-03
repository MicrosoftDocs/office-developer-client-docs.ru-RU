---
title: Режим интерпретации (Справочник по для настольных баз данных Access)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b6401e7954325eded85b70b9edb5d164e857d113
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947863"
---
# <a name="immediate-mode"></a><span data-ttu-id="48075-102">Режим интерпретации</span><span class="sxs-lookup"><span data-stu-id="48075-102">Immediate mode</span></span>


<span data-ttu-id="48075-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="48075-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="48075-104">Режим интерпретации — в случае **LockType для** задано значение **adLockOptimistic** или **adLockPessimistic**.</span><span class="sxs-lookup"><span data-stu-id="48075-104">Immediate mode is in effect when the **LockType** property is set to **adLockOptimistic** or **adLockPessimistic**.</span></span> <span data-ttu-id="48075-105">В режиме интерпретации распространения изменений, внесенных запись к источнику данных сразу же объявлении работы в строке полный путем вызова метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="48075-105">In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the **Update** method.</span></span>

## <a name="calling-update"></a><span data-ttu-id="48075-106">Вызов обновления</span><span class="sxs-lookup"><span data-stu-id="48075-106">Calling Update</span></span>

<span data-ttu-id="48075-107">При перемещении из записи добавлении или редактировании до вызова метода **Update** , ADO автоматически вызывает **обновления** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="48075-107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes.</span></span> <span data-ttu-id="48075-108">Чтобы отменить все изменения, внесенные в текущую запись или отменить только что добавленный запись, необходимо вызвать метод **CancelUpdate** перед переходом.</span><span class="sxs-lookup"><span data-stu-id="48075-108">You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="48075-109">Текущая запись остается текущей после вызова метода **Update** .</span><span class="sxs-lookup"><span data-stu-id="48075-109">The current record remains current after you call the **Update** method.</span></span>

## <a name="cancelupdate"></a><span data-ttu-id="48075-110">CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="48075-110">CancelUpdate</span></span>

<span data-ttu-id="48075-111">Используйте метод **CancelUpdate** для отмены всех изменений, внесенных в текущей строке или отменить новые строки.</span><span class="sxs-lookup"><span data-stu-id="48075-111">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row.</span></span> <span data-ttu-id="48075-112">Невозможно отменить изменения текущей строки или новую строку после вызова метода **обновления** , если изменения не являются частью транзакции, можно отменить с помощью метода **RollbackTrans** либо в составе пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="48075-112">You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the **RollbackTrans** method or part of a batch update.</span></span> <span data-ttu-id="48075-113">В случае пакета обновления можно отменить **обновление** с помощью метода **CancelUpdate** или **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="48075-113">In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or **CancelBatch** method.</span></span>

<span data-ttu-id="48075-114">При добавлении новой строки при вызове метода **CancelUpdate** текущей строки становится строку, которая была текущей до вызова **метода AddNew** .</span><span class="sxs-lookup"><span data-stu-id="48075-114">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the **AddNew** call.</span></span>

<span data-ttu-id="48075-115">Если вы не изменены текущей строки или добавить новую строку, вызов метода **CancelUpdate** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="48075-115">If you have not changed the current row or added a new row, calling the **CancelUpdate** method generates an error.</span></span>

