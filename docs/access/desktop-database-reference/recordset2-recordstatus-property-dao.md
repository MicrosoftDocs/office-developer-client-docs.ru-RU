---
title: Recordset2.RecordStatus Property (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 178872a9-e361-f277-627d-f91b01ceb6d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845575(v=office.15)
ms:contentKeyID: 48543451
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57ecd9c74777ef8aa0515b7bcdb0c1f28050e8a9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883731"
---
# <a name="recordset2recordstatus-property-dao"></a><span data-ttu-id="d3602-102">Recordset2.RecordStatus Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="d3602-102">Recordset2.RecordStatus Property (DAO)</span></span>


<span data-ttu-id="d3602-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d3602-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d3602-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d3602-104">Syntax</span></span>

<span data-ttu-id="d3602-105">*выражение* . RecordStatus</span><span class="sxs-lookup"><span data-stu-id="d3602-105">*expression* .RecordStatus</span></span>

<span data-ttu-id="d3602-106">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="d3602-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3602-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="d3602-107">Remarks</span></span>

<span data-ttu-id="d3602-108">Значение свойства **RecordStatus** указывает ли текущей записи будут принимать участие в следующее обновление оптимистичный пакета.</span><span class="sxs-lookup"><span data-stu-id="d3602-108">The value of the **RecordStatus** property indicates whether and how the current record will be involved in the next optimistic batch update.</span></span>

<span data-ttu-id="d3602-109">Когда пользователь изменяет запись, **RecordStatus** для этой записи автоматически изменяет **dbRecordModified**.</span><span class="sxs-lookup"><span data-stu-id="d3602-109">When a user changes a record, the **RecordStatus** for that record automatically changes to **dbRecordModified**.</span></span> <span data-ttu-id="d3602-110">Аналогично Если добавить или удалить записи **RecordStatus** отражает соответствующие константу.</span><span class="sxs-lookup"><span data-stu-id="d3602-110">Similarly, if a record is added or deleted, **RecordStatus** reflects the appropriate constant.</span></span> <span data-ttu-id="d3602-111">При использовании метода **[обновления](recordset2-update-method-dao.md)** пакетного режима DAO будут отправлять соответствующие операции к удаленному серверу для каждой записи на основе свойства **RecordStatus** эту запись.</span><span class="sxs-lookup"><span data-stu-id="d3602-111">When you then use a batch-mode **[Update](recordset2-update-method-dao.md)** method, DAO will submit an appropriate operation to the remote server for each record, based on the record's **RecordStatus** property.</span></span>

## <a name="example"></a><span data-ttu-id="d3602-112">Пример</span><span class="sxs-lookup"><span data-stu-id="d3602-112">Example</span></span>

<span data-ttu-id="d3602-113">В этом примере с помощью свойства **RecordStatus** и **DefaultCursorDriver** для отображения способ отслеживания изменений в локальном **набора записей** во время обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="d3602-113">This example uses the **RecordStatus** and **DefaultCursorDriver** properties to show how changes to a local **Recordset** are tracked during batch updating.</span></span> <span data-ttu-id="d3602-114">Функция RecordStatusOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d3602-114">The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM authors", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 .MoveFirst 
 Debug.Print "Original record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Edit 
 !au_lname = "Bowen" 
 .Update 
 Debug.Print "Edited record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .AddNew 
 !au_lname = "NewName" 
 .Update 
 Debug.Print "New record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 .Delete 
 Debug.Print "Deleted record: " & !au_lname 
 Debug.Print , RecordStatusOutput2(.RecordStatus) 
 
 ' Close the local recordset without updating the 
 ' data on the server. 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
Function RecordStatusOutput(lngTemp As Long) As String 
 
 Dim strTemp As String 
 
 strTemp = "" 
 
 ' Construct an output string based on the RecordStatus 
 ' value. 
If lngTemp = dbRecordUnmodified Then _ 
 strTemp = "[dbRecordUnmodified]" 
 If lngTemp = dbRecordModified Then _ 
 strTemp = "[dbRecordModified]" 
 If lngTemp = dbRecordNew Then _ 
 strTemp = "[dbRecordNew]" 
 If lngTemp = dbRecordDeleted Then _ 
 strTemp = "[dbRecordDeleted]" 
 If lngTemp = dbRecordDBDeleted Then _ 
 strTemp = "[dbRecordDBDeleted]" 
 
 RecordStatusOutput = strTemp 
 
End Function 
 
```

