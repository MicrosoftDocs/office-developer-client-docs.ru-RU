---
title: Метод Delete (Recordset в ADO)
TOCTitle: Delete method (ADO Recordset)
ms:assetid: 62c39b4d-223e-7b48-6780-6cd272e3114e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249374(v=office.15)
ms:contentKeyID: 48545246
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e8142d4fc4fc0036f80693f0bff779d9f3f2a62e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702490"
---
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="1d968-102">Метод Delete (Recordset в ADO)</span><span class="sxs-lookup"><span data-stu-id="1d968-102">Delete method (ADO Recordset)</span></span>

<span data-ttu-id="1d968-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1d968-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1d968-104">Удаление текущей записи или группы записей.</span><span class="sxs-lookup"><span data-stu-id="1d968-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d968-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d968-105">Syntax</span></span>

<span data-ttu-id="1d968-106">*набор записей*. Удаление *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="1d968-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="1d968-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="1d968-107">Parameters</span></span>

|<span data-ttu-id="1d968-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="1d968-108">Parameter</span></span>|<span data-ttu-id="1d968-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1d968-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="1d968-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="1d968-110">*AffectRecords*</span></span> |<span data-ttu-id="1d968-111">Метод **Delete** повлияет от [AffectEnum](affectenum.md) значение, определяющее число записей.</span><span class="sxs-lookup"><span data-stu-id="1d968-111">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect.</span></span> <span data-ttu-id="1d968-112">Значение по умолчанию — **adAffectCurrent**.</span><span class="sxs-lookup"><span data-stu-id="1d968-112">The default value is **adAffectCurrent**.</span></span>|

> [!NOTE]
> <span data-ttu-id="1d968-113">**adAffectAll** и **adAffectAllChapters** не допустимый аргументы, которые нужно **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="1d968-113">**adAffectAll** and **adAffectAllChapters** are not valid arguments to **Delete**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d968-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d968-114">Remarks</span></span>

<span data-ttu-id="1d968-115">С помощью метода **Delete** помечает текущую запись или группу из записей в объекте [набора записей](recordset-object-ado.md) для удаления.</span><span class="sxs-lookup"><span data-stu-id="1d968-115">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion.</span></span> <span data-ttu-id="1d968-116">Если объект **набора записей** не позволяет удаление записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="1d968-116">If the **Recordset** object doesn't allow record deletion, an error occurs.</span></span> <span data-ttu-id="1d968-117">Если вы используете режим немедленное обновление, удаление происходит в базе данных немедленно.</span><span class="sxs-lookup"><span data-stu-id="1d968-117">If you are in immediate update mode, deletions occur in the database immediately.</span></span> <span data-ttu-id="1d968-118">Если запись не может успешно удалены (из-за нарушения целостности базы данных, например), запись будет оставаться в режиме редактирования после вызова **обновления**.</span><span class="sxs-lookup"><span data-stu-id="1d968-118">If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**.</span></span> <span data-ttu-id="1d968-119">Это означает, что необходимо отменить обновление с [CancelUpdate](cancelupdate-method-ado.md) перед перемещением текущей записи (например, с помощью [Закрыть](close-method-ado.md), [Перемещение](move-method-ado.md)или [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="1d968-119">This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="1d968-120">Если вы используете режим пакетного обновления, записи помечаются для удаления из кэша и фактическое удаление происходит при вызове метода [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d968-120">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="1d968-121">(Используйте свойство [фильтра](filter-property-ado.md) для просмотра удаленных записей).</span><span class="sxs-lookup"><span data-stu-id="1d968-121">(Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="1d968-122">Получение значений полей из удаленной записи приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="1d968-122">Retrieving field values from the deleted record generates an error.</span></span> <span data-ttu-id="1d968-123">После удаления текущей записи удаленной записи остается текущей до перехода к другой записи.</span><span class="sxs-lookup"><span data-stu-id="1d968-123">After deleting the current record, the deleted record remains current until you move to a different record.</span></span> <span data-ttu-id="1d968-124">Один раз удалении от удаленной записи, он больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="1d968-124">Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="1d968-125">Если вложить удалений в транзакции, вы можете восстанавливать удаленные записи с помощью метода [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d968-125">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="1d968-126">Если вы используете режим пакетного обновления, можно отменить ожидающие удаления или группой ожидающих удалений с помощью метода [CancelBatch](cancelbatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d968-126">If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="1d968-127">Если происходит сбой попытки для удаления записей из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждений в коллекцию [ошибок](errors-collection-ado.md) , но не останавливается выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="1d968-127">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="1d968-128">Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="1d968-128">A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="1d968-129">Если свойство [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) установлено и **записей** производится в результате выполнения операции СОЕДИНЕНИЯ на несколько таблиц, то метод **Delete** только удаляет строки в таблице с именем в свойстве [Уникальной таблицы](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="1d968-129">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

