---
title: Метод Recordset2. Edit (DAO)
TOCTitle: Edit method
ms:assetid: 34c51eee-274d-3511-b5e2-cb74e4925ec8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192452(v=office.15)
ms:contentKeyID: 48544137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052869
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2742b6558c555673937666ea7d27cae1a54fdf73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309438"
---
# <a name="recordset2edit-method-dao"></a><span data-ttu-id="82662-102">Метод Recordset2. Edit (DAO)</span><span class="sxs-lookup"><span data-stu-id="82662-102">Recordset2.Edit method (DAO)</span></span>

<span data-ttu-id="82662-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82662-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82662-104">Копирует текущую запись с обновляемым объектом **[Recordset](recordset-object-dao.md)** в буфер обмена для последующего редактирования.</span><span class="sxs-lookup"><span data-stu-id="82662-104">Copies the current record from an updatable **[Recordset](recordset-object-dao.md)** object to the copy buffer for subsequent editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="82662-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82662-105">Syntax</span></span>

<span data-ttu-id="82662-106">*Expression* . Правка</span><span class="sxs-lookup"><span data-stu-id="82662-106">*expression* .Edit</span></span>

<span data-ttu-id="82662-107">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="82662-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="82662-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="82662-108">Remarks</span></span>

<span data-ttu-id="82662-109">После использования метода **Edit** изменения, внесенные в поля текущей записи, копируются в буфер копирования.</span><span class="sxs-lookup"><span data-stu-id="82662-109">Once you use the **Edit** method, changes made to the current record's fields are copied to the copy buffer.</span></span> <span data-ttu-id="82662-110">После внесения требуемых изменений в запись используйте метод **[Update](recordset2-update-method-dao.md)** , чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="82662-110">After you make the desired changes to the record, use the **[Update](recordset2-update-method-dao.md)** method to save your changes.</span></span>

<span data-ttu-id="82662-111">Текущая запись остается текущей, после того как вы используете **Edit**.</span><span class="sxs-lookup"><span data-stu-id="82662-111">The current record remains current after you use **Edit**.</span></span>

> [!NOTE]
> <span data-ttu-id="82662-112">Если изменить запись и затем выполнить любую операцию, которая перемещается в другую запись, но без предварительного **обновления**, изменения будут потеряны без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="82662-112">If you edit a record and then perform any operation that moves to another record, but without first using **Update**, your changes are lost without warning.</span></span> <span data-ttu-id="82662-113">Кроме того, если закрывать набор записей или завершать процедуру, в которой объявляется **набор записей** или родительский объект **[базы данных](database-object-dao.md)** или **[подключения](connection-object-dao.md)** , отредактированная запись удаляется без предупреждения.</span><span class="sxs-lookup"><span data-stu-id="82662-113">In addition, if you close recordset or end the procedure which declares the **Recordset** or the parent **[Database](database-object-dao.md)** or **[Connection](connection-object-dao.md)** object, your edited record is discarded without warning.</span></span>

<span data-ttu-id="82662-114">При использовании метода **Edit** выдается сообщение об ошибке, если:</span><span class="sxs-lookup"><span data-stu-id="82662-114">Using **Edit** produces an error if:</span></span>

- <span data-ttu-id="82662-115">Нет текущей записи.</span><span class="sxs-lookup"><span data-stu-id="82662-115">There is no current record.</span></span>

- <span data-ttu-id="82662-116">Объект **подключения**, **базы данных**или объекта **Recordset** открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82662-116">The **Connection**, **Database**, or **Recordset** object was opened as read-only.</span></span>

- <span data-ttu-id="82662-117">Поля в записи не обновляются.</span><span class="sxs-lookup"><span data-stu-id="82662-117">No fields in the record are updatable.</span></span>

- <span data-ttu-id="82662-118">**База данных** или **набор записей** были открыты для монопольного использования другим пользователем (рабочей областью Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82662-118">The **Database** or **Recordset** was opened for exclusive use by another user (Microsoft Access workspace).</span></span>

- <span data-ttu-id="82662-119">Другой пользователь заблокировал страницу, содержащую запись (Рабочая область Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="82662-119">Another user has locked the page containing your record (Microsoft Access workspace).</span></span>

<span data-ttu-id="82662-120">В рабочей области Microsoft Access, когда значение свойства **[LockEdits](recordset2-lockedits-property-dao.md)** объекта **Recordset** (пессимистикалли заблокировано) в многопользовательской среде, запись остается заблокированной, пока не будет установлено обновление. \*\*\*\* \*\*\*\* заполнить.</span><span class="sxs-lookup"><span data-stu-id="82662-120">In a Microsoft Access workspace, when the **Recordset** object's **[LockEdits](recordset2-lockedits-property-dao.md)** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the update is complete.</span></span> <span data-ttu-id="82662-121">Если для свойства **LockEdits** задано **значение false** (оптимистикалли заблокировано), запись блокируется и сравнивается с предварительно измененной записью непосредственно перед ее обновлением в базе данных.</span><span class="sxs-lookup"><span data-stu-id="82662-121">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it's updated in the database.</span></span> <span data-ttu-id="82662-122">Если после использования метода **Edit** запись изменилась, операция **обновления** завершается с ошибкой во время выполнения, если вы используете **OpenRecordset** без указания **дбсичанжес**.</span><span class="sxs-lookup"><span data-stu-id="82662-122">If the record has changed since you used the **Edit** method, the **Update** operation fails with a run-time error if you use **OpenRecordset** without specifying **dbSeeChanges**.</span></span> <span data-ttu-id="82662-123">По умолчанию ODBC и устанавливаемые базы данных ISAM, подключенные к ядру СУБД Microsoft Access, всегда используют оптимистическую блокировку.</span><span class="sxs-lookup"><span data-stu-id="82662-123">By default, Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span>

> [!NOTE]
> <span data-ttu-id="82662-124">Чтобы запись можно было добавить, изменить или удалить, в базовом источнике данных должен быть указан ее уникальный индекс.</span><span class="sxs-lookup"><span data-stu-id="82662-124">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source.</span></span> <span data-ttu-id="82662-125">В противном случае при вызове метода **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)** или **Edit** в рабочей области Microsoft Access произойдет ошибка "отказано в разрешении".</span><span class="sxs-lookup"><span data-stu-id="82662-125">If not, a "Permission denied" error will occur on the **[AddNew](recordset2-addnew-method-dao.md)**, **[Delete](fields-delete-method-dao.md)**, or **Edit** method call in a Microsoft Access workspace.</span></span>

## <a name="example"></a><span data-ttu-id="82662-126">Пример</span><span class="sxs-lookup"><span data-stu-id="82662-126">Example</span></span>

<span data-ttu-id="82662-127">В этом примере с помощью метода **Edit** заменяются текущие данные с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="82662-127">This example uses the **Edit** method to replace the current data with the specified name.</span></span> <span data-ttu-id="82662-128">Для выполнения этой процедуры требуется процедура Едитнаме.</span><span class="sxs-lookup"><span data-stu-id="82662-128">The EditName procedure is required for this procedure to run.</span></span>

```vb
    Sub EditX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Sub EditName(rstTemp As Recordset2, _ 
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
