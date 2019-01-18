---
title: Метод CancelUpdate (ADO)
TOCTitle: CancelUpdate method (ADO)
ms:assetid: 2bd4d168-ba52-7786-5046-44febeda88e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249065(v=office.15)
ms:contentKeyID: 48543938
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4585679688929532d7f50be9efc71b2830bb6587
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711247"
---
# <a name="cancelupdate-method-ado"></a><span data-ttu-id="e9378-102">Метод CancelUpdate (ADO)</span><span class="sxs-lookup"><span data-stu-id="e9378-102">CancelUpdate method (ADO)</span></span>


<span data-ttu-id="e9378-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e9378-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e9378-104">Отменяет все изменения, внесенные в строку текущей или новый объект [набора записей](recordset-object-ado.md) или коллекции [полей](fields-collection-ado.md) объекта [записи](record-object-ado.md) , прежде чем вызывать метод [Update](update-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e9378-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, before calling the [Update](update-method-ado.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9378-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9378-105">Syntax</span></span>

<span data-ttu-id="e9378-106">*набор записей*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="e9378-106">*recordset*.CancelUpdate</span></span>

<span data-ttu-id="e9378-107">*запись*. *Поля*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="e9378-107">*record*.*Fields*.CancelUpdate</span></span>

## <a name="remarks"></a><span data-ttu-id="e9378-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="e9378-108">Remarks</span></span>

<span data-ttu-id="e9378-109">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="e9378-109">**Recordset**</span></span>

<span data-ttu-id="e9378-110">Используйте метод **CancelUpdate** для отмены всех изменений, внесенных в текущей строке или отменить новые строки.</span><span class="sxs-lookup"><span data-stu-id="e9378-110">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row.</span></span> <span data-ttu-id="e9378-111">Нельзя отменить изменения для текущей строки или новую строку после вызова метода **обновления** , если изменения не являются частью транзакции, можно отменить с помощью метода [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) или в составе пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="e9378-111">You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method, or part of a batch update.</span></span> <span data-ttu-id="e9378-112">В случае пакета обновления можно отменить **обновление** с помощью метода **CancelUpdate** или [CancelBatch](cancelbatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e9378-112">In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="e9378-113">При добавлении новой строки при вызове метода **CancelUpdate** текущей строки становится строку, которая была текущей до вызова [метода AddNew](addnew-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e9378-113">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the [AddNew](addnew-method-ado.md) call.</span></span>

<span data-ttu-id="e9378-114">Если вы находитесь в режиме редактирования и требуется переместить текущей записи (например, с помощью [перемещения](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)или [Закрыть](close-method-ado.md)), чтобы отменить ожидающие изменения можно использовать **CancelUpdate** .</span><span class="sxs-lookup"><span data-stu-id="e9378-114">If you are in edit mode and want to move off the current record (for example, with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md)), you can use **CancelUpdate** to cancel any pending changes.</span></span> <span data-ttu-id="e9378-115">Может появиться в случае, если обновление не может успешно учтены к источнику данных (например, попытка delete, возникает ошибка из-за нарушения целостности данных оставьте **записей** в режиме редактирования после вызова метода для [удаления](delete-method-ado-recordset.md)).</span><span class="sxs-lookup"><span data-stu-id="e9378-115">You may need to do this if the update cannot successfully be posted to the data source (for example, an attempted delete that fails due to referential integrity violations will leave the **Recordset** in edit mode after a call to [Delete](delete-method-ado-recordset.md)).</span></span>

<span data-ttu-id="e9378-116">**Record**</span><span class="sxs-lookup"><span data-stu-id="e9378-116">**Record**</span></span>

<span data-ttu-id="e9378-117">Метод **CancelUpdate** отменяет все ожидающие вставку или удаление объектов [полей](field-object-ado.md) и показано, как отменить ожидающие обновления существующего поля и восстанавливает их значения.</span><span class="sxs-lookup"><span data-stu-id="e9378-117">The **CancelUpdate** method cancels any pending insertions or deletions of [Field](field-object-ado.md) objects, and cancels pending updates of existing fields and restores them to their original values.</span></span> <span data-ttu-id="e9378-118">[Состояние](status-property-ado-recordset.md) всех полей в коллекции **полей** задано значение **adFieldOK**.</span><span class="sxs-lookup"><span data-stu-id="e9378-118">The [Status](status-property-ado-recordset.md) property of all fields in the **Fields** collection is set to **adFieldOK**.</span></span>

