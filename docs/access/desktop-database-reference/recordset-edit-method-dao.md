---
title: Метод Recordset.Edit (DAO)
TOCTitle: Edit Method
ms:assetid: a64d601b-f446-da40-0020-b99110a72872
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821175(v=office.15)
ms:contentKeyID: 48546850
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 82dc6e175c7168d5c1b042e85dce7b77aa96b575
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300541"
---
# <a name="recordsetedit-method-dao"></a><span data-ttu-id="012c6-102">Метод Recordset.Edit (DAO)</span><span class="sxs-lookup"><span data-stu-id="012c6-102">Recordset.Edit method (DAO)</span></span>

<span data-ttu-id="012c6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="012c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="012c6-104">Копирует текущую запись с обновляемым объектом **[Recordset](recordset-object-dao.md)** в буфер обмена для последующего редактирования.</span><span class="sxs-lookup"><span data-stu-id="012c6-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="012c6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="012c6-105">Syntax</span></span>

<span data-ttu-id="012c6-106">*выражение* .Edit</span><span class="sxs-lookup"><span data-stu-id="012c6-106">*expression* .Edit</span></span>

<span data-ttu-id="012c6-107">*выражение*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="012c6-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="012c6-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="012c6-108">Remarks</span></span>

<span data-ttu-id="012c6-109">После использования метода **Edit** изменения, внесенные в поля текущей записи, копируются в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="012c6-109">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer.</span></span> <span data-ttu-id="012c6-110">После внесения нужных изменений в запись используйте метод **[Update](recordset-update-method-dao.md)**, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="012c6-110">After you make the desired changes to the record, use the **[Update](recordset-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="012c6-111">После использования метода **Edit** текущая запись остается текущей.</span><span class="sxs-lookup"><span data-stu-id="012c6-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="012c6-112">Если изменить запись, а затем выполнить какую-либо операцию, переходящую к другой записи, но без предварительного использования метода **Update**, изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="012c6-112">If you issue an AddNew and then perform any operation that moves to another record, but without using Update, your changes are lost without warning.</span></span> <span data-ttu-id="012c6-113">Кроме того, если закрыть набор записей или завершить процедуру, которая объявляет объект **Recordset** или родительский объект **[Database](database-object-dao.md)** или **[Connection](connection-object-dao.md)**, измененная запись удаляется без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="012c6-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="012c6-114">Использование метода **Edit** вызывает ошибку, если:</span><span class="sxs-lookup"><span data-stu-id="012c6-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="012c6-115">Отсутствует текущая запись.</span><span class="sxs-lookup"><span data-stu-id="012c6-115">There is no current record.</span></span>

- <span data-ttu-id="012c6-116">Объект **Connection**, **Database** или **Recordset** был открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="012c6-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="012c6-117">В записи нет обновляемых полей.</span><span class="sxs-lookup"><span data-stu-id="012c6-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="012c6-118">Объект **Database** или **Recordset** был открыт для монопольного использования другим пользователем (рабочая область Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="012c6-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="012c6-119">Другой пользователь заблокировал страницу, содержащую запись (рабочая область Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="012c6-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="012c6-120">Если в рабочей области Microsoft Access свойству **[LockEdits](recordset-lockedits-property-dao.md)** объекта **Recordset** задано значение **True** (пессимистичная блокировка) в многопользовательской среде, запись останется заблокированной с момента использования метода **Edit** до завершения обновления.</span><span class="sxs-lookup"><span data-stu-id="012c6-120">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete.</span></span> <span data-ttu-id="012c6-121">Если свойству **LockEdits** задано значение **False** (оптимистичная блокировка), запись заблокирована и сравнивается с состоянием записи до изменения непосредственно перед обновлением в базе данных.</span><span class="sxs-lookup"><span data-stu-id="012c6-121">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database.</span></span> <span data-ttu-id="012c6-122">Если запись была изменена после использования метода **Edit**, операция **Update** завершается ошибкой во время выполнения, если используется **OpenRecordset** без указания **dbSeeChanges**.</span><span class="sxs-lookup"><span data-stu-id="012c6-122">If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**.</span></span> <span data-ttu-id="012c6-123">По умолчанию в ODBC с подключением к ядру СУБД Microsoft Access и устанавливаемых базах данных ISAM всегда используется оптимистичная блокировка.</span><span class="sxs-lookup"><span data-stu-id="012c6-123">By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="012c6-124">Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="012c6-124">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="012c6-125">Если это не так, при вызове метода **[AddNew](recordset-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** или **Edit** возникнет ошибка "Отказано в разрешении" в рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="012c6-125">If not, a "Permission denied" error will occur on the AddNew, Delete, or Edit method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="012c6-126">Пример</span><span class="sxs-lookup"><span data-stu-id="012c6-126">Example</span></span>

<span data-ttu-id="012c6-127">В этом примере используется метод **Edit** для замены текущих данных указанным именем.</span><span class="sxs-lookup"><span data-stu-id="012c6-127">This example uses the **Edit** method to replace the current data with the specified name.</span></span> <span data-ttu-id="012c6-128">Процедура EditName является обязательной для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="012c6-128">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

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
