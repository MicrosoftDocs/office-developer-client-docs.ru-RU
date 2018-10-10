---
title: Recordset.RecordStatus Property (DAO)
TOCTitle: RecordStatus Property
ms:assetid: 6fbd6909-6191-d7be-9a3a-1e9908dacc2b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195591(v=office.15)
ms:contentKeyID: 48545543
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1102617
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ada7c1dfa4b71a0f455a4e596de1bd4a037d5d59
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482060"
---
# <a name="recordsetrecordstatus-property-dao"></a><span data-ttu-id="1e238-102">Recordset.RecordStatus Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1e238-102">Recordset.RecordStatus Property (DAO)</span></span>


<span data-ttu-id="1e238-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e238-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="1e238-104">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e238-104">Syntax</span></span>

<span data-ttu-id="1e238-105">*выражение* . RecordStatus</span><span class="sxs-lookup"><span data-stu-id="1e238-105">*expression* .RecordStatus</span></span>

<span data-ttu-id="1e238-106">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="1e238-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e238-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="1e238-107">Remarks</span></span>

<span data-ttu-id="1e238-108">Значение свойства **RecordStatus** указывает ли текущей записи будут принимать участие в следующее обновление оптимистичный пакета.</span><span class="sxs-lookup"><span data-stu-id="1e238-108">The value of the **RecordStatus** property indicates whether and how the current record will be involved in the next optimistic batch update.</span></span>

<span data-ttu-id="1e238-109">Когда пользователь изменяет запись, **RecordStatus** для этой записи автоматически изменяет **dbRecordModified**.</span><span class="sxs-lookup"><span data-stu-id="1e238-109">When a user changes a record, the **RecordStatus** for that record automatically changes to **dbRecordModified**.</span></span> <span data-ttu-id="1e238-110">Аналогично Если добавить или удалить записи **RecordStatus** отражает соответствующие константу.</span><span class="sxs-lookup"><span data-stu-id="1e238-110">Similarly, if a record is added or deleted, **RecordStatus** reflects the appropriate constant.</span></span> <span data-ttu-id="1e238-111">При использовании метода **[обновления](recordset-update-method-dao.md)** пакетного режима DAO будут отправлять соответствующие операции к удаленному серверу для каждой записи на основе свойства **RecordStatus** эту запись.</span><span class="sxs-lookup"><span data-stu-id="1e238-111">When you then use a batch-mode **[Update](recordset-update-method-dao.md)** method, DAO will submit an appropriate operation to the remote server for each record, based on the record's **RecordStatus** property.</span></span>

## <a name="example"></a><span data-ttu-id="1e238-112">Пример</span><span class="sxs-lookup"><span data-stu-id="1e238-112">Example</span></span>

<span data-ttu-id="1e238-113">В этом примере с помощью свойства **RecordStatus** и **DefaultCursorDriver** для отображения способ отслеживания изменений в локальном **набора записей** во время обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="1e238-113">This example uses the **RecordStatus** and **DefaultCursorDriver** properties to show how changes to a local **Recordset** are tracked during batch updating.</span></span> <span data-ttu-id="1e238-114">Функция RecordStatusOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="1e238-114">The RecordStatusOutput function is required for this procedure to run.</span></span>

```vb 
Sub RecordStatusX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
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

