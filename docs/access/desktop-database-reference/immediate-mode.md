---
title: Режим интерпретации (Справочник по базам данных Access на компьютере)
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
# <a name="immediate-mode"></a><span data-ttu-id="51cc9-102">Режим немедленного обновления</span><span class="sxs-lookup"><span data-stu-id="51cc9-102">Immediate mode</span></span>


<span data-ttu-id="51cc9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51cc9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51cc9-104">Режим интерпретации вступает в силу, если для свойства **LockType** задано значение **адлоккоптимистик** или **адлоккпессимистик**.</span><span class="sxs-lookup"><span data-stu-id="51cc9-104">Immediate mode is in effect when the **LockType** property is set to **adLockOptimistic** or **adLockPessimistic**.</span></span> <span data-ttu-id="51cc9-105">В режиме интерпретации изменения записи передаются в источник данных сразу после того, как вы объявили работу по строке завершенным, вызвав метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="51cc9-105">In immediate mode, changes to a record are propagated to the data source as soon as you declare the work on a row complete by calling the **Update** method.</span></span>

## <a name="calling-update"></a><span data-ttu-id="51cc9-106">Вызов обновления</span><span class="sxs-lookup"><span data-stu-id="51cc9-106">Calling Update</span></span>

<span data-ttu-id="51cc9-107">Если вы перейдете из записи, которую вы добавляете или редактируете перед вызовом метода **Update** , ADO автоматически выполнит вызов **Update** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="51cc9-107">If you move from the record you are adding or editing before calling the **Update** method, ADO will automatically call **Update** to save the changes.</span></span> <span data-ttu-id="51cc9-108">Перед навигацией необходимо вызвать метод **CancelUpdate** , чтобы отменить все изменения, внесенные в текущую запись, или удалить только что добавленную запись.</span><span class="sxs-lookup"><span data-stu-id="51cc9-108">You must call the **CancelUpdate** method before navigation if you want to cancel any changes made to the current record or discard a newly added record.</span></span>

<span data-ttu-id="51cc9-109">Текущая запись остается текущей, когда вы вызываете метод **Update** .</span><span class="sxs-lookup"><span data-stu-id="51cc9-109">The current record remains current after you call the **Update** method.</span></span>

## <a name="cancelupdate"></a><span data-ttu-id="51cc9-110">CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="51cc9-110">CancelUpdate</span></span>

<span data-ttu-id="51cc9-111">Используйте метод **CancelUpdate** , чтобы отменить все изменения, внесенные в текущую строку, или удалить только что добавленную строку.</span><span class="sxs-lookup"><span data-stu-id="51cc9-111">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row.</span></span> <span data-ttu-id="51cc9-112">После вызова метода **Update** невозможно отменить изменения текущей строки или новой строки, если эти изменения не являются частью транзакции, которую можно откатить методом **RollbackTrans** или частью пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="51cc9-112">You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the **RollbackTrans** method or part of a batch update.</span></span> <span data-ttu-id="51cc9-113">В случае пакетного обновления вы можете отменить **Обновление** с помощью метода **CancelUpdate** или **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="51cc9-113">In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or **CancelBatch** method.</span></span>

<span data-ttu-id="51cc9-114">Если вы добавляете новую строку при вызове метода **CancelUpdate** , текущая строка становится текущей строкой до вызова **AddNew** .</span><span class="sxs-lookup"><span data-stu-id="51cc9-114">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the **AddNew** call.</span></span>

<span data-ttu-id="51cc9-115">Если вы не изменили текущую строку или добавили новую строку, вызов метода **CancelUpdate** создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="51cc9-115">If you have not changed the current row or added a new row, calling the **CancelUpdate** method generates an error.</span></span>

