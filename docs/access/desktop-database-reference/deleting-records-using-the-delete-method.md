---
title: Удаление записей с помощью метода Delete
TOCTitle: Deleting Records Using the Delete Method
ms:assetid: 22917c33-4d14-ebab-d85c-2cbe7f68c560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249003(v=office.15)
ms:contentKeyID: 48543708
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca39f78a69c31d45ecab57b297d8b6eaf9031d92
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875366"
---
# <a name="deleting-records-using-the-delete-method"></a><span data-ttu-id="7c4ed-102">Удаление записей с помощью метода Delete</span><span class="sxs-lookup"><span data-stu-id="7c4ed-102">Deleting Records Using the Delete Method</span></span>


<span data-ttu-id="7c4ed-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c4ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c4ed-104">С помощью метода **Delete** помечает текущую запись или группу из записей в объекте **набора записей** для удаления.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-104">Using the **Delete** method marks the current record or a group of records in a **Recordset** object for deletion.</span></span> <span data-ttu-id="7c4ed-105">Если объект **набора записей** не допускается удаление записи, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-105">If the **Recordset** object does not allow record deletion, an error occurs.</span></span> <span data-ttu-id="7c4ed-106">Если вы используете режим немедленное обновление, удаление происходит в базе данных немедленно.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-106">If you are in immediate update mode, deletions occur in the database immediately.</span></span> <span data-ttu-id="7c4ed-107">Если запись не может успешно удалены (из-за нарушения целостности базы данных, например), запись будет оставаться в режиме редактирования после вызова **обновления**.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-107">If a record cannot be successfully deleted (due to database integrity violations, for example), the record will remain in edit mode after the call to **Update**.</span></span> <span data-ttu-id="7c4ed-108">Это означает, что необходимо отменить обновления с помощью [CancelUpdate](cancelupdate-method-ado.md) перед перемещением текущей записи (например, с помощью [Закрыть](close-method-ado.md), [Перемещение](move-method-ado.md)или [NextRecordset](nextrecordset-method-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="7c4ed-108">This means that you must cancel the update using [CancelUpdate](cancelupdate-method-ado.md) before moving off the current record (for example, using [Close](close-method-ado.md), [Move](move-method-ado.md), or [NextRecordset](nextrecordset-method-ado.md)).</span></span>

<span data-ttu-id="7c4ed-109">Если вы используете режим пакетного обновления, записи помечаются для удаления из кэша и фактическое удаление происходит при вызове метода **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-109">If you are in batch update mode, the records are marked for deletion from the cache and the actual deletion happens when you call the **UpdateBatch** method.</span></span> <span data-ttu-id="7c4ed-110">(Чтобы просмотреть список удаленных записей, значение свойства **фильтра** **adFilterAffectedRecords** после **удаления** вызова.)</span><span class="sxs-lookup"><span data-stu-id="7c4ed-110">(To view the deleted records, set the **Filter** property to **adFilterAffectedRecords** after **Delete** is called.)</span></span>

<span data-ttu-id="7c4ed-111">Попытка получения значения полей из удаленной записи приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-111">Attempting to retrieve field values from the deleted record generates an error.</span></span> <span data-ttu-id="7c4ed-112">После удаления текущей записи удаленной записи остается текущей до перехода к другой записи.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-112">After deleting the current record, the deleted record remains current until you move to a different record.</span></span> <span data-ttu-id="7c4ed-113">Один раз удалении от удаленной записи, он больше не доступен.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-113">Once you move away from the deleted record, it is no longer accessible.</span></span>

<span data-ttu-id="7c4ed-114">Если вложить удалений в транзакции, можно восстановить удаленные записи с помощью метода **RollbackTrans** .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-114">If you nest deletions in a transaction, you can recover deleted records by using the **RollbackTrans** method.</span></span> <span data-ttu-id="7c4ed-115">Если вы используете режим пакетного обновления, можно отменить ожидающие удаления или группой ожидающих удалений с помощью метода **CancelBatch** .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-115">If you are in batch update mode, you can cancel a pending deletion or group of pending deletions by using the **CancelBatch** method.</span></span>

<span data-ttu-id="7c4ed-116">Если происходит сбой попытки для удаления записей из-за конфликта с базовыми данными (например, запись уже была удалена другим пользователем), поставщик возвращает предупреждений в коллекцию **ошибок** , но не останавливается выполнение программы.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-116">If the attempt to delete records fails because of a conflict with the underlying data (for example, a record has already been deleted by another user), the provider returns warnings to the **Errors** collection but does not halt program execution.</span></span> <span data-ttu-id="7c4ed-117">Только в том случае, если все запрошенные записи конфликтуют возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-117">A run-time error occurs only if there are conflicts on all the requested records.</span></span>

<span data-ttu-id="7c4ed-118">Если свойство **Уникальной таблицы** установлено и **записей** производится в результате выполнения операции СОЕДИНЕНИЯ на несколько таблиц, метод **Delete** приведет к удалению строк только из таблицы с именем в свойстве **Уникальной таблицы** .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-118">If the **Unique Table** dynamic property is set and the **Recordset** is the result of executing a JOIN operation on multiple tables, the **Delete** method will delete rows only from the table named in the **Unique Table** property.</span></span>

<span data-ttu-id="7c4ed-119">Метод **удаления** принимает необязательный аргумент, который позволяет указать, какие записи затронуты операцию **удаления** .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-119">The **Delete** method takes an optional argument that allows you to specify which records are affected by the **Delete** operation.</span></span> <span data-ttu-id="7c4ed-120">Только допустимые значения для этого аргумента: один из следующих констант перечисления ADO **AffectEnum** :</span><span class="sxs-lookup"><span data-stu-id="7c4ed-120">The only valid values for this argument are either of the following ADO **AffectEnum** enumerated constants:</span></span>

  - <span data-ttu-id="7c4ed-121">**adAffectCurrent** Влияет только текущей записи.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-121">**adAffectCurrent**Affects only the current record.</span></span>

  - <span data-ttu-id="7c4ed-122">**adAffectGroup** Влияет только записи, которые удовлетворяют текущего значения свойства **фильтра** .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-122">**adAffectGroup**Affects only records that satisfy the current **Filter** property setting.</span></span> <span data-ttu-id="7c4ed-123">Свойства **фильтра** должно быть присвоено значение **FilterGroupEnum** или массив **закладки** этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-123">The **Filter** property must be set to a **FilterGroupEnum** value or an array of **Bookmarks** to use this option.</span></span>

<span data-ttu-id="7c4ed-124">Ниже показан пример указания **adAffectGroup** при вызове метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="7c4ed-124">The following code shows an example of specifying **adAffectGroup** when calling the **Delete** method.</span></span> <span data-ttu-id="7c4ed-125">В этом примере добавляется несколько записей для примера **набора записей** и обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-125">This example adds some records to the sample **Recordset** and updates the database.</span></span> <span data-ttu-id="7c4ed-126">Затем фильтр **набора записей** с помощью константа перечисления фильтра **adFilterAffectedRecords** , что делает видимой в **набор записей**только новые записи.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-126">Then it filters the **Recordset** using the **adFilterAffectedRecords** filter enumerated constant, which leaves only the newly added records visible in the **Recordset**.</span></span> <span data-ttu-id="7c4ed-127">И, наконец он вызывает метод **Delete** и указывает, что все записи, которые удовлетворяют текущего значения свойства **фильтра** (новые записи) должны быть удалены.</span><span class="sxs-lookup"><span data-stu-id="7c4ed-127">Finally, it calls the **Delete** method and specifies that all of the records that satisfy the current **Filter** property setting (the new records) should be deleted.</span></span>

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

