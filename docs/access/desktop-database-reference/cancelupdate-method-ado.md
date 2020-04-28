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
# <a name="cancelupdate-method-ado"></a><span data-ttu-id="c21af-102">Метод CancelUpdate (ADO)</span><span class="sxs-lookup"><span data-stu-id="c21af-102">CancelUpdate method (ADO)</span></span>


<span data-ttu-id="c21af-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c21af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c21af-104">Отменяет любые изменения, внесенные в текущую или новую строку объекта [Recordset](recordset-object-ado.md) , или коллекцию [Fields](fields-collection-ado.md) объекта [Record](record-object-ado.md) перед вызовом метода [Update](update-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c21af-104">Cancels any changes made to the current or new row of a [Recordset](recordset-object-ado.md) object, or the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, before calling the [Update](update-method-ado.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c21af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c21af-105">Syntax</span></span>

<span data-ttu-id="c21af-106">*набор записей*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="c21af-106">*recordset*.CancelUpdate</span></span>

<span data-ttu-id="c21af-107">*запись*. *Поля*. CancelUpdate</span><span class="sxs-lookup"><span data-stu-id="c21af-107">*record*.*Fields*.CancelUpdate</span></span>

## <a name="remarks"></a><span data-ttu-id="c21af-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="c21af-108">Remarks</span></span>

<span data-ttu-id="c21af-109">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="c21af-109">**Recordset**</span></span>

<span data-ttu-id="c21af-110">Используйте метод **CancelUpdate** , чтобы отменить все изменения, внесенные в текущую строку, или удалить только что добавленную строку.</span><span class="sxs-lookup"><span data-stu-id="c21af-110">Use the **CancelUpdate** method to cancel any changes made to the current row or to discard a newly added row.</span></span> <span data-ttu-id="c21af-111">Вы не можете отменить изменения в текущей строке или новой строке после вызова метода **Update** , если изменения не являются частью транзакции, которую можно откатить методом [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) или частью пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="c21af-111">You cannot cancel changes to the current row or a new row after you call the **Update** method, unless the changes are either part of a transaction that you can roll back with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method, or part of a batch update.</span></span> <span data-ttu-id="c21af-112">В случае пакетного обновления вы можете отменить **Обновление** с помощью метода **CancelUpdate** или [CancelBatch](cancelbatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c21af-112">In the case of a batch update, you can cancel the **Update** with the **CancelUpdate** or [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="c21af-113">Если вы добавляете новую строку при вызове метода **CancelUpdate** , текущая строка становится текущей строкой до вызова [AddNew](addnew-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="c21af-113">If you are adding a new row when you call the **CancelUpdate** method, the current row becomes the row that was current before the [AddNew](addnew-method-ado.md) call.</span></span>

<span data-ttu-id="c21af-114">Если вы переходите в режим правки и хотите переместиться из текущей записи (например, с помощью [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md)или [Close](close-method-ado.md)), можно отменить ожидающие изменения с помощью **CancelUpdate** .</span><span class="sxs-lookup"><span data-stu-id="c21af-114">If you are in edit mode and want to move off the current record (for example, with [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md), or [Close](close-method-ado.md)), you can use **CancelUpdate** to cancel any pending changes.</span></span> <span data-ttu-id="c21af-115">Это может потребоваться, если обновление невозможно успешно отправить в источник данных (например, попытка удалить, которая не удалась из-за нарушений целостности данных, оставляет объект **Recordset** в режиме редактирования после вызова [Delete](delete-method-ado-recordset.md)).</span><span class="sxs-lookup"><span data-stu-id="c21af-115">You may need to do this if the update cannot successfully be posted to the data source (for example, an attempted delete that fails due to referential integrity violations will leave the **Recordset** in edit mode after a call to [Delete](delete-method-ado-recordset.md)).</span></span>

<span data-ttu-id="c21af-116">**Record**</span><span class="sxs-lookup"><span data-stu-id="c21af-116">**Record**</span></span>

<span data-ttu-id="c21af-117">Метод **CancelUpdate** отменяет все ожидающие вставки или удаления объектов [field](field-object-ado.md) , а также отменяет ожидающие обновления существующих полей и восстанавливает их исходные значения.</span><span class="sxs-lookup"><span data-stu-id="c21af-117">The **CancelUpdate** method cancels any pending insertions or deletions of [Field](field-object-ado.md) objects, and cancels pending updates of existing fields and restores them to their original values.</span></span> <span data-ttu-id="c21af-118">Свойству [Status](status-property-ado-recordset.md) всех полей в коллекции **Fields** присвоено значение **адфиелдок**.</span><span class="sxs-lookup"><span data-stu-id="c21af-118">The [Status](status-property-ado-recordset.md) property of all fields in the **Fields** collection is set to **adFieldOK**.</span></span>

