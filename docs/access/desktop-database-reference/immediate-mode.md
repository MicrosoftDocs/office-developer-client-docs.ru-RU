---
title: Немедленный режим (справочник по базе данных Access для настольных пк)
TOCTitle: Immediate mode
ms:assetid: 61bd3645-6e84-2e3a-7814-37d8c1247df0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249362(v=office.15)
ms:contentKeyID: 48545220
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3abc2e8365c60987fedc0d306b274df74c7ee551
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291882"
---
# <a name="immediate-mode"></a><span data-ttu-id="70330-102">Режим немедленного обновления</span><span class="sxs-lookup"><span data-stu-id="70330-102">Immediate mode</span></span>


<span data-ttu-id="70330-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70330-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70330-104">Немедленный режим действует, когда свойству **LockType** задают свойство **adLockOptimistic** или **adLockPessimistic.**</span><span class="sxs-lookup"><span data-stu-id="70330-104">Immediate mode is in effect when the **LockType** property is set to **adLockOptimistic** or **adLockPessimistic**.</span></span> <span data-ttu-id="70330-105">В немедленном режиме изменения записи распространяются в источник данных, как только вы объявляете работу над строкой, вызывая метод **Update.**</span><span class="sxs-lookup"><span data-stu-id="70330-105">In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the **Update** method.</span></span>

## <a name="calling-update"></a><span data-ttu-id="70330-106">Обновление вызовов</span><span class="sxs-lookup"><span data-stu-id="70330-106">Calling Update</span></span>

<span data-ttu-id="70330-107">При переходе от добавляемой или редактируемой записи перед вызовом метода **Update** ADO автоматически вызывает **Update,** чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="70330-107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes.</span></span> <span data-ttu-id="70330-108">Необходимо вызвать метод **CancelUpdate** перед переходом, если необходимо отменить все изменения, внесенные в текущую запись, или удалить только что добавленную запись.</span><span class="sxs-lookup"><span data-stu-id="70330-108">You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="70330-109">Текущая запись остается текущей после вызова метода **Update.**</span><span class="sxs-lookup"><span data-stu-id="70330-109">The current record remains current after you call the **Update** method.</span></span>

## <a name="cancelupdate"></a><span data-ttu-id="70330-110">CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="70330-110">CancelUpdate</span></span>

<span data-ttu-id="70330-111">Используйте метод **CancelUpdate,** чтобы отменить все изменения, внесенные в текущую строку, или отменить добавленную строку.</span><span class="sxs-lookup"><span data-stu-id="70330-111">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row.</span></span> <span data-ttu-id="70330-112">После вызова метода **Update** нельзя отменить изменения текущей или новой строки, если изменения не являются частью транзакции, которую можно откатить с помощью метода **RollbackTrans** или пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="70330-112">You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the **RollbackTrans** method or part of a batch update.</span></span> <span data-ttu-id="70330-113">В случае пакетного обновления можно отменить обновление с помощью метода **CancelUpdate** или **CancelBatch.** </span><span class="sxs-lookup"><span data-stu-id="70330-113">In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or **CancelBatch** method.</span></span>

<span data-ttu-id="70330-114">При добавлении новой строки при вызове метода **CancelUpdate** текущая строка становится текущей перед вызовом **AddNew.**</span><span class="sxs-lookup"><span data-stu-id="70330-114">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the **AddNew** call.</span></span>

<span data-ttu-id="70330-115">Если вы не изменили текущую строку или не добавили новую строку, вызов метода **CancelUpdate** создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="70330-115">If you have not changed the current row or added a new row, calling the **CancelUpdate** method generates an error.</span></span>

