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
# <a name="delete-method-ado-recordset"></a><span data-ttu-id="e33d6-102">Метод Delete (Recordset в ADO)</span><span class="sxs-lookup"><span data-stu-id="e33d6-102">Delete method (ADO Recordset)</span></span>

<span data-ttu-id="e33d6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e33d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e33d6-104">Удаляет текущую запись или группу записей.</span><span class="sxs-lookup"><span data-stu-id="e33d6-104">Deletes the current record or a group of records.</span></span>

## <a name="syntax"></a><span data-ttu-id="e33d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e33d6-105">Syntax</span></span>

<span data-ttu-id="e33d6-106">*набор записей*. Удаление *аффектрекордс*</span><span class="sxs-lookup"><span data-stu-id="e33d6-106">*recordset*.Delete *AffectRecords*</span></span>

## <a name="parameters"></a><span data-ttu-id="e33d6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e33d6-107">Parameters</span></span>

|<span data-ttu-id="e33d6-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="e33d6-108">Parameter</span></span>|<span data-ttu-id="e33d6-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e33d6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e33d6-110">*Аффектрекордс*</span><span class="sxs-lookup"><span data-stu-id="e33d6-110">*AffectRecords*</span></span> |<span data-ttu-id="e33d6-111">Значение [аффектенум](affectenum.md) , определяющее количество записей, на которые влияет метод **Delete** .</span><span class="sxs-lookup"><span data-stu-id="e33d6-111">An [AffectEnum](affectenum.md) value that determines how many records the **Delete** method will affect.</span></span> <span data-ttu-id="e33d6-112">Значение по умолчанию — **адаффекткуррент**.</span><span class="sxs-lookup"><span data-stu-id="e33d6-112">The default value is **adAffectCurrent**.</span></span>|

> [!NOTE]
> <span data-ttu-id="e33d6-113">**адаффекталл** и **адаффекталлчаптерс** не являются допустимыми аргументами для **удаления**.</span><span class="sxs-lookup"><span data-stu-id="e33d6-113">**adAffectAll** and **adAffectAllChapters** are not valid arguments to **Delete**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e33d6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="e33d6-114">Remarks</span></span>

<span data-ttu-id="e33d6-115">С помощью метода **Delete** вы помечаете текущую запись или группу записей в объекте [Recordset](recordset-object-ado.md) для удаления.</span><span class="sxs-lookup"><span data-stu-id="e33d6-115">Using the **Delete** method marks the current record or a group of records in a [Recordset](recordset-object-ado.md) object for deletion.</span></span> <span data-ttu-id="e33d6-116">Если объект **Recordset** не допускает удаления записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="e33d6-116">If the **Recordset** object doesn't allow record deletion, an error occurs.</span></span> <span data-ttu-id="e33d6-117">Если вы используете режим немедленного обновления, немедленное удаление происходит в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e33d6-117">If you are in immediate update mode, deletions occur in the database immediately.</span></span> <span data-ttu-id="e33d6-118">Если запись не может быть успешно удалена (например, из-за нарушений целостности базы данных), запись остается в режиме редактирования после вызова **Update**.</span><span class="sxs-lookup"><span data-stu-id="e33d6-118">If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**.</span></span> <span data-ttu-id="e33d6-119">Это означает, что необходимо отменить обновление с помощью [CancelUpdate](cancelupdate-method-ado.md) , прежде чем переходить к текущей записи (например, с помощью [Close](close-method-ado.md), [Move](move-method-ado.md)или [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="e33d6-119">This means that you must cancel the update with [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, with [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="e33d6-120">Если вы используете режим пакетного обновления, записи помечаются для удаления из кэша, а фактическое удаление происходит при вызове метода [UpdateBatch](updatebatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e33d6-120">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the [UpdateBatch](updatebatch-method-ado.md) method.</span></span> <span data-ttu-id="e33d6-121">(Используйте свойство [Filter](filter-property-ado.md) для просмотра удаленных записей.)</span><span class="sxs-lookup"><span data-stu-id="e33d6-121">(Use the [Filter](filter-property-ado.md) property to view the deleted records.)</span></span>

<span data-ttu-id="e33d6-122">Получение значений полей из удаленной записи приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="e33d6-122">Retrieving field values from the deleted record generates an error.</span></span> <span data-ttu-id="e33d6-123">После удаления текущей записи удаленная запись остается текущей до тех пор, пока не будет перемещена на другую запись.</span><span class="sxs-lookup"><span data-stu-id="e33d6-123">After deleting the current record, the deleted record remains current until you move to a different record.</span></span> <span data-ttu-id="e33d6-124">После выхода из удаленной записи она становится недоступной.</span><span class="sxs-lookup"><span data-stu-id="e33d6-124">Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="e33d6-125">При вложении удалений в транзакцию можно восстановить удаленные записи с помощью метода [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e33d6-125">If you nest deletions in a transaction, you can recover deleted records with the [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method.</span></span> <span data-ttu-id="e33d6-126">Если вы используете режим пакетного обновления, вы можете отменить ожидающее удаление или группу ожидающих удалений с помощью метода [CancelBatch](cancelbatch-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e33d6-126">If you are in batch update mode, you can cancel a pending deletion or group of pending deletions with the [CancelBatch](cancelbatch-method-ado.md) method.</span></span>

<span data-ttu-id="e33d6-127">Если попытка удалить записи не удалась из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию Errors, но [](errors-collection-ado.md) не приостанавливает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="e33d6-127">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution.</span></span> <span data-ttu-id="e33d6-128">Ошибка во время выполнения возникает только в том случае, если имеются конфликты со всеми запрошенными записями.</span><span class="sxs-lookup"><span data-stu-id="e33d6-128">A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="e33d6-129">Если задано уникальное динамическое свойство [Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) , а **набор записей** является результатом выполнения операции присоединения к нескольким таблицам, метод **Delete** будет удалять только строки из таблицы, имя которой указано в свойстве [UNIQUE Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e33d6-129">If the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property is set, and the **Recordset** is the result of executing a JOIN operation on multiple tables, then the **Delete** method will only delete rows from the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) property.</span></span>

