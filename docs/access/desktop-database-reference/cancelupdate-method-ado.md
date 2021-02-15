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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296628"
---
# <a name="cancelupdate-method-ado"></a><span data-ttu-id="1b91b-102">Метод CancelUpdate (ADO)</span><span class="sxs-lookup"><span data-stu-id="1b91b-102">CancelUpdate method (ADO)</span></span>


<span data-ttu-id="1b91b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1b91b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1b91b-104">Отменяет все изменения, внесенные в текущую или новую строку объекта [Recordset](recordset-object-ado.md) или коллекцию [Fields](fields-collection-ado.md) объекта [Record,](record-object-ado.md) перед вызовом [метода Update.](update-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1b91b-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, before calling the [Update](update-method-ado.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b91b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b91b-105">Syntax</span></span>

<span data-ttu-id="1b91b-106">*recordset*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="1b91b-106">*recordset*.CancelUpdate</span></span>

<span data-ttu-id="1b91b-107">*record*. *Поля*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="1b91b-107">*record*.*Fields*.CancelUpdate</span></span>

## <a name="remarks"></a><span data-ttu-id="1b91b-108">Заметки</span><span class="sxs-lookup"><span data-stu-id="1b91b-108">Remarks</span></span>

<span data-ttu-id="1b91b-109">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="1b91b-109">**Recordset**</span></span>

<span data-ttu-id="1b91b-110">Используйте метод **CancelUpdate,** чтобы отменить все изменения, внесенные в текущую строку, или отменить добавленную строку.</span><span class="sxs-lookup"><span data-stu-id="1b91b-110">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row.</span></span> <span data-ttu-id="1b91b-111">После вызова метода **Update** нельзя отменить изменения текущей или новой строки, если изменения не являются частью транзакции, которую можно откатить с помощью метода [RollbackTrans,](begintrans-committrans-and-rollbacktrans-methods-ado.md) или пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="1b91b-111">You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method, or part of a batch update.</span></span> <span data-ttu-id="1b91b-112">В случае пакетного обновления можно отменить обновление с помощью метода **CancelUpdate** или [CancelBatch.](cancelbatch-method-ado.md) </span><span class="sxs-lookup"><span data-stu-id="1b91b-112">In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="1b91b-113">При добавлении новой строки при вызове метода **CancelUpdate** текущая строка становится текущей перед вызовом [AddNew.](addnew-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1b91b-113">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the [AddNew](addnew-method-ado.md) call.</span></span>

<span data-ttu-id="1b91b-114">Если вы находитесь в режиме редактирования и хотите отключить текущую запись (например, с помощью [Move,](move-method-ado.md) [NextRecordset](nextrecordset-method-ado.md)или [Close),](close-method-ado.md)можно использовать **CancelUpdate,** чтобы отменить ожидающих изменений.</span><span class="sxs-lookup"><span data-stu-id="1b91b-114">If you are in edit mode and want to move off the current record (for example, with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md)), you can use **CancelUpdate** to cancel any pending changes.</span></span> <span data-ttu-id="1b91b-115">Это может потребоваться, если не удается успешно опубликовать обновление в источнике данных (например, попытка удаления, которая не удалась из-за нарушения целостности, оставляет набор **записей** в режиме редактирования после вызова [delete).](delete-method-ado-recordset.md)</span><span class="sxs-lookup"><span data-stu-id="1b91b-115">You may need to do this if the update cannot successfully be posted to the data source (for example, an attempted delete that fails due to referential integrity violations will leave the **Recordset** in edit mode after a call to [Delete](delete-method-ado-recordset.md)).</span></span>

<span data-ttu-id="1b91b-116">**Record**</span><span class="sxs-lookup"><span data-stu-id="1b91b-116">**Record**</span></span>

<span data-ttu-id="1b91b-117">Метод **CancelUpdate** отменяет ожидающих вставки или удаления объектов [Field](field-object-ado.md) и отменяет ожидающих обновлений существующих полей и восстанавливает их исходные значения.</span><span class="sxs-lookup"><span data-stu-id="1b91b-117">The **CancelUpdate** method cancels any pending insertions or deletions of [Field](field-object-ado.md) objects, and cancels pending updates of existing fields and restores them to their original values.</span></span> <span data-ttu-id="1b91b-118">Для [свойства Status](status-property-ado-recordset.md) всех полей в коллекции **Fields** задается свойство **adFieldOK.**</span><span class="sxs-lookup"><span data-stu-id="1b91b-118">The [Status](status-property-ado-recordset.md) property of all fields in the **Fields** collection is set to **adFieldOK**.</span></span>

