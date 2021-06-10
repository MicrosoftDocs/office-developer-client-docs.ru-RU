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
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="052be-102">Метод Delete (Recordset в ADO)</span><span class="sxs-lookup"><span data-stu-id="052be-102">Delete method (ADO Recordset)</span></span>

<span data-ttu-id="052be-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="052be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="052be-104">Удаляет текущую запись или группу записей.</span><span class="sxs-lookup"><span data-stu-id="052be-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="052be-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="052be-105">Syntax</span></span>

<span data-ttu-id="052be-106">*набор записей.* Удаление *AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="052be-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="052be-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="052be-107">Parameters</span></span>

|<span data-ttu-id="052be-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="052be-108">Parameter</span></span>|<span data-ttu-id="052be-109">Описание</span><span class="sxs-lookup"><span data-stu-id="052be-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="052be-110">*AffectRecords*</span><span class="sxs-lookup"><span data-stu-id="052be-110">*AffectRecords*</span></span> |<span data-ttu-id="052be-111">Значение [AffectEnum,](affectenum.md) определя которое определяет количество записей, на которые повлияет метод **Delete.**</span><span class="sxs-lookup"><span data-stu-id="052be-111">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect.</span></span> <span data-ttu-id="052be-112">По умолчанию значение **adAffectCurrent**.</span><span class="sxs-lookup"><span data-stu-id="052be-112">The default value is **adAffectCurrent**.</span></span>|

> [!NOTE]
> <span data-ttu-id="052be-113">**adAffectAll и** **adAffectAllChapters** не являются допустимым аргументом для **удаления**.</span><span class="sxs-lookup"><span data-stu-id="052be-113">**adAffectAll** and **adAffectAllChapters** are not valid arguments to **Delete**.</span></span>

## <a name="remarks"></a><span data-ttu-id="052be-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="052be-114">Remarks</span></span>

<span data-ttu-id="052be-115">Метод **Delete** отмечает текущую запись или группу записей в [объекте Recordset](recordset-object-ado.md) для удаления.</span><span class="sxs-lookup"><span data-stu-id="052be-115">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion.</span></span> <span data-ttu-id="052be-116">Если объект **Recordset** не разрешает удаление записей, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="052be-116">If the **Recordset** object doesn't allow record deletion, an error occurs.</span></span> <span data-ttu-id="052be-117">Если вы находитесь в режиме немедленного обновления, в базе данных немедленно происходят удаления.</span><span class="sxs-lookup"><span data-stu-id="052be-117">If you are in immediate update mode, deletions occur in the database immediately.</span></span> <span data-ttu-id="052be-118">Если запись не удается успешно удалить (например, из-за нарушений целостности базы данных), запись останется в режиме редактирования после вызова **обновления.**</span><span class="sxs-lookup"><span data-stu-id="052be-118">If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**.</span></span> <span data-ttu-id="052be-119">Это означает, что необходимо отменить обновление с [помощью CancelUpdate,](cancelupdate-method-ado.md) прежде чем отменить текущую запись (например, с [Close,](close-method-ado.md) [Move](move-method-ado.md)или [NextRecordset).](nextrecordset-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="052be-119">This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="052be-120">Если вы находитесь в режиме пакетного обновления, записи помечены для удаления из кэша, а фактическое удаление происходит при вызове метода [UpdateBatch.](updatebatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="052be-120">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="052be-121">(Используйте свойство [Filter](filter-property-ado.md) для просмотра удаленных записей.)</span><span class="sxs-lookup"><span data-stu-id="052be-121">(Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="052be-122">Удаление значений поля из удаленной записи создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="052be-122">Retrieving field values from the deleted record generates an error.</span></span> <span data-ttu-id="052be-123">После удаления текущей записи удаленная запись остается текущей до тех пор, пока вы не перейдете к другой записи.</span><span class="sxs-lookup"><span data-stu-id="052be-123">After deleting the current record, the deleted record remains current until you move to a different record.</span></span> <span data-ttu-id="052be-124">После удаления от удаленной записи она больше недоступна.</span><span class="sxs-lookup"><span data-stu-id="052be-124">Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="052be-125">При вложении удалений в транзакцию можно восстановить удаленные записи с помощью метода [RollbackTrans.](begintrans-committrans-and-rollbacktrans-methods-ado.md)</span><span class="sxs-lookup"><span data-stu-id="052be-125">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="052be-126">Если вы находитесь в режиме пакетного обновления, можно отменить ожидающих удаления или группу ожидающих удалений с помощью метода [CancelBatch.](cancelbatch-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="052be-126">If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="052be-127">Если попытка удалить записи не удалась из-за конфликта с данными( например, запись уже удалена другим пользователем), [](errors-collection-ado.md) поставщик возвращает предупреждения в коллекцию Ошибок, но не прекращает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="052be-127">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="052be-128">Ошибка во время запуска возникает только в том случае, если во всех запрашиваемых записях имеются конфликты.</span><span class="sxs-lookup"><span data-stu-id="052be-128">A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="052be-129">Если [динамическое](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) свойство Unique Table установлено, а набор **recordset** является результатом выполнения операции JOIN на нескольких таблицах, метод **Delete** удаляет строки из таблицы, названной в свойстве [Unique Table.](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="052be-129">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

