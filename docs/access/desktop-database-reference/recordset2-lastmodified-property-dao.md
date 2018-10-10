---
title: Recordset2.LastModified Property (DAO)
TOCTitle: LastModified Property
ms:assetid: 1c13cb43-23b5-73b6-af00-a3676cc37cc7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845726(v=office.15)
ms:contentKeyID: 48543557
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 09562d9bcdffb85d3e97a6aca72fa3b34411e5a7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481658"
---
# <a name="recordset2lastmodified-property-dao"></a><span data-ttu-id="8dd56-102">Recordset2.LastModified Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="8dd56-102">Recordset2.LastModified Property (DAO)</span></span>


<span data-ttu-id="8dd56-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8dd56-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8dd56-104">Возвращает ookmark, указывающее наиболее недавно добавлены или изменены записи.</span><span class="sxs-lookup"><span data-stu-id="8dd56-104">Returns a ookmark indicating the most recently added or changed record.</span></span>

## <a name="syntax"></a><span data-ttu-id="8dd56-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8dd56-105">Syntax</span></span>

<span data-ttu-id="8dd56-106">*выражение* . Дата изменения</span><span class="sxs-lookup"><span data-stu-id="8dd56-106">*expression* .LastModified</span></span>

<span data-ttu-id="8dd56-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="8dd56-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dd56-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="8dd56-108">Remarks</span></span>

<span data-ttu-id="8dd56-109">Свойство **LastModified** перейти с самыми последними добавлены или обновленные записи.</span><span class="sxs-lookup"><span data-stu-id="8dd56-109">You can use the **LastModified** property to move to the most recently added or updated record.</span></span> <span data-ttu-id="8dd56-110">Используйте свойство **LastModified** с таблице - и добавляющий объекты **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="8dd56-110">Use the **LastModified** property with table- and dynaset-type **[Recordset](recordset-object-dao.md)** objects.</span></span> <span data-ttu-id="8dd56-111">Записи должны быть добавлены или изменены в объекте **набора записей** в порядке для свойства **LastModified** , которое должно иметь значение.</span><span class="sxs-lookup"><span data-stu-id="8dd56-111">A record must be added or modified in the **Recordset** object itself in order for the **LastModified** property to have a value.</span></span>

## <a name="example"></a><span data-ttu-id="8dd56-112">Пример</span><span class="sxs-lookup"><span data-stu-id="8dd56-112">Example</span></span>

<span data-ttu-id="8dd56-113">В этом примере используется свойство **LastModified** для перемещения указатель текущей записи запись, которая была изменена и только что созданная запись.</span><span class="sxs-lookup"><span data-stu-id="8dd56-113">This example uses the **LastModified** property to move the current record pointer to both a record that has been modified and a newly created record.</span></span>

```vb
    Sub LastModifiedX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirst As String 
     Dim strLast As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Store current data. 
     strFirst = !FirstName 
     strLast = !LastName 
     ' Change data in current record. 
     .Edit 
     !FirstName = "Julie" 
     !LastName = "Warren" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after Edit: " & _ 
     !FirstName & " " & !LastName 
     
     ' Restore original data because this is a demonstration. 
     .Edit 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     
     ' Add new record. 
     .AddNew 
     !FirstName = "Roger" 
     !LastName = "Harui" 
     .Update 
     ' Move current record pointer to the most recently 
     ' changed or added record. 
     .Bookmark = .LastModified 
     Debug.Print _ 
     "Data in LastModified record after AddNew: " & _ 
     !FirstName & " " & !LastName 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="8dd56-114">В этом примере используется метод **AddNew** , чтобы создать новую запись с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="8dd56-114">This example uses the **AddNew** method to create a new record with the specified name.</span></span> <span data-ttu-id="8dd56-115">Функция AddName является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="8dd56-115">The AddName function is required for this procedure to run.</span></span>

```vb
    Sub AddNewX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim strFirstName As String 
     Dim strLastName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", dbOpenDynaset) 
     
     ' Get data from the user. 
     strFirstName = Trim(InputBox( _ 
     "Enter first name:")) 
     strLastName = Trim(InputBox( _ 
     "Enter last name:")) 
     
     ' Proceed only if the user actually entered something 
     ' for both the first and last names. 
     If strFirstName <> "" and strLastName <> "" Then 
     
     ' Call the function that adds the record. 
     AddName rstEmployees, strFirstName, strLastName 
     
     ' Show the newly added data. 
     With rstEmployees 
     Debug.Print "New record: " & !FirstName & _ 
     " " & !LastName 
     ' Delete new record because this is a demonstration. 
     .Delete 
     End With 
     
     Else 
     Debug.Print _ 
     "You must input a string for first and last name!" 
     End If 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function AddName(rstTemp As Recordset, _ 
     strFirst As String, strLast As String) 
     
     ' Adds a new record to a Recordset using the data passed 
     ' by the calling procedure. The new record is then made 
     ' the current record. 
     With rstTemp 
     .AddNew 
     !FirstName = strFirst 
     !LastName = strLast 
     .Update 
     .Bookmark = .LastModified 
     End With 
     
    End Function
```
