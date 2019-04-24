---
title: Удаление записей с помощью метода Delete
TOCTitle: Deleting records using the Delete method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a476e9bc57224b0e46afb31bf092450c26de0a17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293968"
---
# <a name="deleting-records-using-the-delete-method"></a><span data-ttu-id="ba0ac-102">Удаление записей с помощью метода Delete</span><span class="sxs-lookup"><span data-stu-id="ba0ac-102">Deleting records using the Delete method</span></span>


<span data-ttu-id="ba0ac-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba0ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba0ac-104">С помощью метода **Delete** вы помечаете текущую запись или группу записей в объекте **Recordset** для удаления.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-104">Using the **Delete** method marks the current record or a group of records in a **Recordset** object for deletion.</span></span> <span data-ttu-id="ba0ac-105">Если объект **Recordset** не разрешает удаление записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-105">If the **Recordset** object does not allow record deletion, an error occurs.</span></span> <span data-ttu-id="ba0ac-106">Если вы используете режим немедленного обновления, немедленное удаление происходит в базе данных.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-106">If you are in immediate update mode, deletions occur in the database immediately.</span></span> <span data-ttu-id="ba0ac-107">Если запись не может быть успешно удалена (например, из-за нарушений целостности базы данных), запись остается в режиме редактирования после вызова **Update**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-107">If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**.</span></span> <span data-ttu-id="ba0ac-108">Это означает, что необходимо отменить обновление с помощью [CancelUpdate](cancelupdate-method-ado.md) , прежде чем переходить к текущей записи (например, с помощью [Close](close-method-ado.md), [Move](move-method-ado.md)или [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="ba0ac-108">This means that you must cancel the update using [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, using [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="ba0ac-109">Если вы используете режим пакетного обновления, записи помечаются для удаления из кэша, а фактическое удаление происходит при вызове метода **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-109">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the **UpdateBatch** method.</span></span> <span data-ttu-id="ba0ac-110">(Чтобы просмотреть удаленные записи, установите свойство **Filter** в **Адфилтераффектедрекордс** после вызова **Delete** .)</span><span class="sxs-lookup"><span data-stu-id="ba0ac-110">(To view the deleted records, set the **Filter** property to **adFilterAffectedRecords** after **Delete** is called.)</span></span>

<span data-ttu-id="ba0ac-111">При попытке получить значения полей из удаленной записи возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-111">Attempting to retrieve field values from the deleted record generates an error.</span></span> <span data-ttu-id="ba0ac-112">После удаления текущей записи удаленная запись остается текущей до тех пор, пока не будет перемещена на другую запись.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-112">After deleting the current record, the deleted record remains current until you move to a different record.</span></span> <span data-ttu-id="ba0ac-113">После выхода из удаленной записи она становится недоступной.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-113">Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="ba0ac-114">При вложении удалений в транзакцию можно восстановить удаленные записи с помощью метода **RollbackTrans** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-114">If you nest deletions in a transaction, you can recover deleted records by using the **RollbackTrans** method.</span></span> <span data-ttu-id="ba0ac-115">Если вы используете режим пакетного обновления, вы можете отменить ожидающее удаление или группу ожидающих удалений с помощью метода **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-115">If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the **CancelBatch** method.</span></span>

<span data-ttu-id="ba0ac-116">Если попытка удалить записи не удалась из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждения в коллекцию Errors, но \*\*\*\* не приостанавливает выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-116">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the **Errors** collection but does not halt program execution.</span></span> <span data-ttu-id="ba0ac-117">Ошибка во время выполнения возникает только в том случае, если имеются конфликты со всеми запрошенными записями.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-117">A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="ba0ac-118">Если задано динамическое свойство **Table** , а **набор записей** является результатом выполнения операции присоединения к нескольким таблицам, метод **Delete** удалит строки только из таблицы, имя которой указано в свойстве **UNIQUE Table** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-118">If the **Unique Table** dynamic property is set and the **Recordset** is the result of executing a JOIN operation on multiple tables, the **Delete** method will delete rows only from the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="ba0ac-119">Метод **Delete** принимает необязательный аргумент, который позволяет указать, какие записи будут затронуты операцией **Delete** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-119">The **Delete** method takes an optional argument that allows you to specify which records are affected by the **Delete** operation.</span></span> <span data-ttu-id="ba0ac-120">Единственным допустимым значением для этого аргумента является одна из перечисленных констант **аффектенум** в ADO:</span><span class="sxs-lookup"><span data-stu-id="ba0ac-120">The only valid values for this argument are either of the following ADO **AffectEnum** enumerated constants:</span></span>

  - <span data-ttu-id="ba0ac-121">**адаффекткуррент** Влияет только на текущую запись.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-121">**adAffectCurrent**Affects only the current record.</span></span>

  - <span data-ttu-id="ba0ac-122">**адаффектграуп** Влияет только на записи, которые соответствуют текущему значению свойства **Filter** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-122">**adAffectGroup**Affects only records that satisfy the current **Filter** property setting.</span></span> <span data-ttu-id="ba0ac-123">Для использования этого параметра свойству **Filter** должно быть присвоено значение **Филтерграупенум** или массив **закладок** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span></span>

<span data-ttu-id="ba0ac-124">В приведенном ниже коде показан пример указания **адаффектграуп** при вызове метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="ba0ac-124">The following code shows an example of specifying **adAffectGroup** when calling the **Delete** method.</span></span> <span data-ttu-id="ba0ac-125">В этом примере показано, как добавить некоторые записи в образец **набора записей** и обновить базу данных.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-125">This example adds some records to the sample **Recordset** and updates the database.</span></span> <span data-ttu-id="ba0ac-126">Затем он фильтрует **набор записей** с помощью перечислимой константы **адфилтераффектедрекордс** Filter, который оставляет только недавно добавленные записи, отображаемЫе в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-126">Then it filters the **Recordset** using the **adFilterAffectedRecords** filter enumerated constant, which leaves only the newly added records visible in the **Recordset**.</span></span> <span data-ttu-id="ba0ac-127">Наконец, вызывается метод **Delete** и задается, что все записи, которые соответствуют текущему значению свойства **Filter** (новые записи), должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="ba0ac-127">Finally, it calls the **Delete** method and specifies that all of the records that satisfy the current **Filter** property setting (the new records) should be deleted.</span></span>

```vb 
 
'BeginDeleteGroup 
 'add some bogus records 
 With objRs1 
 For i = 0 To 8 
 .AddNew 
 .Fields("CompanyName") = "Shipper Number " & i + 1 
 .Fields("Phone") = "(425) 555-000" & (i + 1) 
 .Update 
 Next i 
 
 're-connect & update 
 .ActiveConnection = GetNewConnection 
 .UpdateBatch 
 
 'filter on newly added records 
 .Filter = adFilterAffectedRecords 
 Debug.Print "Deleting the " & .RecordCount & _ 
 " records you just added." 
 
 'delete the newly added bogus records 
 .Delete adAffectGroup 
 .Filter = adFilterNone 
 Debug.Print .RecordCount & " records remain." 
 
 .Close 
 End With 
'EndDeleteGroup 
```

