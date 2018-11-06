---
title: Метод Recordset.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76868140d9f6f1b16a35219864d054ed1f742e84
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996484"
---
# <a name="recordsetedit-method-dao"></a><span data-ttu-id="e44cd-102">Метод Recordset.Edit (DAO)</span><span class="sxs-lookup"><span data-stu-id="e44cd-102">Recordset.Edit method (DAO)</span></span>

<span data-ttu-id="e44cd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e44cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e44cd-104">Копирует текущей записи из обновляемый объект **[набора записей](recordset-object-dao.md)** в буфер копирования для последующего редактирования.</span><span class="sxs-lookup"><span data-stu-id="e44cd-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e44cd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e44cd-105">Syntax</span></span>

<span data-ttu-id="e44cd-106">*выражение* . Изменение</span><span class="sxs-lookup"><span data-stu-id="e44cd-106">*expression* .Edit</span></span>

<span data-ttu-id="e44cd-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="e44cd-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e44cd-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="e44cd-108">Remarks</span></span>

<span data-ttu-id="e44cd-109">После использования метода **Edit** изменений, внесенных в текущей записи полей копируются буфера копирования.</span><span class="sxs-lookup"><span data-stu-id="e44cd-109">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer.</span></span> <span data-ttu-id="e44cd-110">Внеся необходимые изменения в запись, используйте метод **[Update](recordset-update-method-dao.md)** для сохранения изменений.</span><span class="sxs-lookup"><span data-stu-id="e44cd-110">After you make the desired changes to the record, use the **[Update](recordset-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="e44cd-111">Текущая запись остается текущей после **изменения**.</span><span class="sxs-lookup"><span data-stu-id="e44cd-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="e44cd-112">Если изменить запись и затем выполнять любые операции, перемещает к другой записи, но не с помощью **обновления**, изменения не сохраняются без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="e44cd-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="e44cd-113">Кроме того при закрытии набора записей или завершение процедуры, которая объявляет **записей** или родительский объект **[базы данных](database-object-dao.md)** или **[подключения к](connection-object-dao.md)** измененной записи удаляется без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="e44cd-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="e44cd-114">Применить **изменения** вызовет ошибку, если:</span><span class="sxs-lookup"><span data-stu-id="e44cd-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="e44cd-115">Нет нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="e44cd-115">There is no current record.</span></span>

- <span data-ttu-id="e44cd-116">Объект **подключения**, **базы данных**или **набора записей** , был открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e44cd-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="e44cd-117">Нет поля в записи, обновляемые.</span><span class="sxs-lookup"><span data-stu-id="e44cd-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="e44cd-118">**Базы данных** или **набора записей** была открыта в монопольном режиме другим пользователем (Microsoft Access в рабочей области).</span><span class="sxs-lookup"><span data-stu-id="e44cd-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="e44cd-119">Другой пользователь заблокировал страницу, содержащую записи (Microsoft Access в рабочей области).</span><span class="sxs-lookup"><span data-stu-id="e44cd-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="e44cd-120">В рабочей области Microsoft Access когда объекта **набора записей** **[LockEdits](recordset-lockedits-property-dao.md)** задается **значение True** (pessimistically заблокирован) в многопользовательской среде запись остается заблокированным с момента **Изменение** используется до обновления Завершите.</span><span class="sxs-lookup"><span data-stu-id="e44cd-120">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete.</span></span> <span data-ttu-id="e44cd-121">Если значение свойства **LockEdits** равно **False** (оптимистичном случае заблокирован), запись блокируется и по сравнению с предварительно измененной записи непосредственно перед обновляется в базе данных.</span><span class="sxs-lookup"><span data-stu-id="e44cd-121">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database.</span></span> <span data-ttu-id="e44cd-122">При изменении записи так, как использовать метод **Edit** операции **обновления** происходит сбой с ошибкой во время выполнения при использовании **OpenRecordset** без указания **dbSeeChanges**.</span><span class="sxs-lookup"><span data-stu-id="e44cd-122">If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**.</span></span> <span data-ttu-id="e44cd-123">По умолчанию базы данных Microsoft Access модуль подключения ODBC, а устанавливаемый драйвер ISAM баз данных всегда использовать оптимистичный блокировки.</span><span class="sxs-lookup"><span data-stu-id="e44cd-123">By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="e44cd-124">Чтобы добавить, изменить или удалить записи, должен существовать уникальный индекс на запись в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="e44cd-124">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="e44cd-125">В противном случае ошибку «Отказано в доступе» произойдет на вызов метода **[AddNew](recordset-addnew-method-dao.md)**, **[Удаление](fields-delete-method-dao.md)** или **Изменение** в рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="e44cd-125">If not, a "Permission denied" error will occur on the **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="e44cd-126">Пример</span><span class="sxs-lookup"><span data-stu-id="e44cd-126">Example</span></span>

<span data-ttu-id="e44cd-127">В этом примере используется метод **Изменить** для замены текущих данных с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="e44cd-127">This example uses the **Edit** method to replace the current data with the specified name.</span></span> <span data-ttu-id="e44cd-128">Процедура EditName является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="e44cd-128">The EditName procedure is required for this procedure to run.</span></span>

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strOldFirst As String 
     Dim strOldLast As String 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     ' Store original data. 
     strOldFirst = rstEmployees!FirstName 
     strOldLast = rstEmployees!LastName 
     
     ' Get new data for record. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed if the user entered something for both fields. 
     If strFirstName <> "" and strLastName <> "" Then 
     ' Update record with new data. 
     EditName rstEmployees, strFirstName, strLastName 
     
     With rstEmployees 
     ' Show old and new data. 
     Debug.Print "Old data: " & strOldFirst & _ 
     " " & strOldLast 
     Debug.Print "New data: " & !FirstName & _ 
     " " & !LastName 
     ' Restore original data because this is a 
     ' demonstration. 
     .Edit 
     !FirstName = strOldFirst 
     !LastName = strOldLast 
     .Update 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub EditName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Make changes to record and set the bookmark to keep 
     ' the same record current. 
     With rstTemp 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Sub
```
