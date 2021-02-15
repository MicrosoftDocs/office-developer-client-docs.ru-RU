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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294101"
---
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="30f65-102">Метод Delete (Recordset в ADO)</span><span class="sxs-lookup"><span data-stu-id="30f65-102">Delete method (ADO Recordset)</span></span>

<span data-ttu-id="30f65-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30f65-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30f65-104">Удаляет текущую запись или группу записей.</span><span class="sxs-lookup"><span data-stu-id="30f65-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="30f65-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30f65-105">Syntax</span></span>

<span data-ttu-id="30f65-106">*recordset*. Удаление *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="30f65-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="30f65-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="30f65-107">Parameters</span></span>

|<span data-ttu-id="30f65-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="30f65-108">Parameter</span></span>|<span data-ttu-id="30f65-109">Описание</span><span class="sxs-lookup"><span data-stu-id="30f65-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="30f65-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="30f65-110">*AffectRecords*</span></span> |<span data-ttu-id="30f65-111">Значение [AffectEnum,](affectenum.md) которое определяет количество записей, на которые влияет метод **Delete.**</span><span class="sxs-lookup"><span data-stu-id="30f65-111">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect.</span></span> <span data-ttu-id="30f65-112">Значение по умолчанию **— adAffectCurrent.**</span><span class="sxs-lookup"><span data-stu-id="30f65-112">The default value is **adAffectCurrent**.</span></span>|

> [!NOTE]
> <span data-ttu-id="30f65-113">**adAffectAll** и **adAffectAllChapters** не являются допустимыми аргументами для **удаления.**</span><span class="sxs-lookup"><span data-stu-id="30f65-113">**adAffectAll** and **adAffectAllChapters** are not valid arguments to **Delete**.</span></span>

## <a name="remarks"></a><span data-ttu-id="30f65-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="30f65-114">Remarks</span></span>

<span data-ttu-id="30f65-115">Метод **Delete** пометит текущую запись или группу записей в [объекте Recordset](recordset-object-ado.md) для удаления.</span><span class="sxs-lookup"><span data-stu-id="30f65-115">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion.</span></span> <span data-ttu-id="30f65-116">Если объект **Recordset** не разрешает удаление записей, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="30f65-116">If the **Recordset** object doesn't allow record deletion, an error occurs.</span></span> <span data-ttu-id="30f65-117">Если вы находитесь в режиме немедленного обновления, немедленное удаление происходит в базе данных.</span><span class="sxs-lookup"><span data-stu-id="30f65-117">If you are in immediate update mode, deletions occur in the database immediately.</span></span> <span data-ttu-id="30f65-118">Если запись не удается успешно удалить (например, из-за нарушений целостности базы данных), запись останется в режиме редактирования после вызова **"Обновить".**</span><span class="sxs-lookup"><span data-stu-id="30f65-118">If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**.</span></span> <span data-ttu-id="30f65-119">Это означает, что перед перемещением текущей записи (например, с [close,](close-method-ado.md) [Move](move-method-ado.md)или [NextRecordset)](nextrecordset-method-ado.md)необходимо отменить обновление с помощью [CancelUpdate.](cancelupdate-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="30f65-119">This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="30f65-120">Если вы находитесь в режиме пакетного обновления, записи помечаются для удаления из кэша, а фактическое удаление происходит при вызове метода [UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="30f65-120">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="30f65-121">(Используйте свойство [Filter](filter-property-ado.md) для просмотра удаленных записей.)</span><span class="sxs-lookup"><span data-stu-id="30f65-121">(Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="30f65-122">При искомом значении поля из удаленной записи создается ошибка.</span><span class="sxs-lookup"><span data-stu-id="30f65-122">Retrieving field values from the deleted record generates an error.</span></span> <span data-ttu-id="30f65-123">После удаления текущей записи удаленная запись остается текущей, пока вы не перейдете к другой записи.</span><span class="sxs-lookup"><span data-stu-id="30f65-123">After deleting the current record, the deleted record remains current until you move to a different record.</span></span> <span data-ttu-id="30f65-124">После перемещения от удаленной записи она будет недоступна.</span><span class="sxs-lookup"><span data-stu-id="30f65-124">Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="30f65-125">При вложении удалений в транзакцию можно восстановить удаленные записи с помощью метода [RollbackTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="30f65-125">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="30f65-126">Если вы находитесь в режиме пакетного обновления, вы можете отменить ожидающих удаления или группу ожидающих удаления с помощью метода [CancelBatch.](cancelbatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="30f65-126">If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="30f65-127">Если попытка удалить записи не удалась из-за конфликта с данными, которые находятся в ее реализации (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию [ошибок,](errors-collection-ado.md) но не останавливает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="30f65-127">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="30f65-128">Ошибка во время запуска возникает только при конфликтах всех запрашиваемых записей.</span><span class="sxs-lookup"><span data-stu-id="30f65-128">A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="30f65-129">Если за установлено динамическое свойство Unique [Table,](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) а **recordset** является результатом выполнения операции JOIN в нескольких таблицах, метод **Delete** удаляет только строки из таблицы, именуемой в свойстве [Unique Table.](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="30f65-129">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

