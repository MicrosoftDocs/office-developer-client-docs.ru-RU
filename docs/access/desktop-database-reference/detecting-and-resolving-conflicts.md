---
title: Обнаружение и разрешение конфликтов
TOCTitle: Detecting and Resolving Conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76bfc8f81b7f9df3d1b0e759620952f92bb5c8f1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875297"
---
# <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="effb5-102">Обнаружение и разрешение конфликтов</span><span class="sxs-lookup"><span data-stu-id="effb5-102">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="effb5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="effb5-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="effb5-104">Обнаружение и разрешение конфликтов</span><span class="sxs-lookup"><span data-stu-id="effb5-104">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="effb5-105">Если вы имеете дело с вашего **набора записей** в режиме интерпретации, существует значительно снижают вероятность возникновения проблем параллелизма в случае.</span><span class="sxs-lookup"><span data-stu-id="effb5-105">If you are dealing with your **Recordset** in immediate mode, there is much less chance for concurrency problems to arise.</span></span> <span data-ttu-id="effb5-106">С другой стороны, если приложение использует режим обновление пакета, может существовать хорошо вероятность того, что один пользователь будет изменение записи перед сохранением изменений, внесенных другим пользователем, редактирования и той же записи.</span><span class="sxs-lookup"><span data-stu-id="effb5-106">On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes made by another user editing the same record are saved.</span></span> <span data-ttu-id="effb5-107">В этом случае требуется приложение дело конфликта.</span><span class="sxs-lookup"><span data-stu-id="effb5-107">In such a case, you will want your application to gracefully handle the conflict.</span></span> <span data-ttu-id="effb5-108">Может быть нежелательным, последний участник отправить обновление на сервере «wins.»</span><span class="sxs-lookup"><span data-stu-id="effb5-108">It may be your wish that the last person to send an update to the server "wins."</span></span> <span data-ttu-id="effb5-109">Или может понадобиться разрешить самыми последними пользователю решить, какие обновления должны имеют приоритет, предоставляя ему возможность выбора из двух конфликтующие значения.</span><span class="sxs-lookup"><span data-stu-id="effb5-109">Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</span></span>

<span data-ttu-id="effb5-110">В любом случае ADO предоставляет свойства **UnderlyingValue** и **OriginalValue** объекта **поля** для обработки подобных конфликтов.</span><span class="sxs-lookup"><span data-stu-id="effb5-110">Whatever the case, ADO provides the **UnderlyingValue** and **OriginalValue** properties of the **Field** object in order to handle these types of conflicts.</span></span> <span data-ttu-id="effb5-111">Используйте эти свойства в сочетании с **выполнить повторную синхронизацию** методов и свойств **фильтра** набора **записей**.</span><span class="sxs-lookup"><span data-stu-id="effb5-111">Use these properties in combination with the **Resync** method and **Filter** property of the **Recordset**.</span></span>

## <a name="detecting-errors"></a><span data-ttu-id="effb5-112">Обнаружение ошибок</span><span class="sxs-lookup"><span data-stu-id="effb5-112">Detecting Errors</span></span>

<span data-ttu-id="effb5-113">Когда ADO обнаруживает конфликт во время пакетного обновления, предупреждение переводятся в семейство **Errors** .</span><span class="sxs-lookup"><span data-stu-id="effb5-113">When ADO encounters a conflict during a batch update, a warning will be placed in the **Errors** collection.</span></span> <span data-ttu-id="effb5-114">Таким образом следует всегда проверять наличие ошибок сразу же после вызова **BatchUpdate**и если, найти начать тестирование предполагается, что вы столкнулись конфликта.</span><span class="sxs-lookup"><span data-stu-id="effb5-114">Therefore, you should always check for errors immediately after calling **BatchUpdate**, and if you find them, begin testing the assumption that you have encountered a conflict.</span></span> <span data-ttu-id="effb5-115">Первым шагом является установка свойств **фильтра** для **набора записей** равно **adFilterConflictingRecords** (свойство **фильтра** , описывается в предыдущей главе).</span><span class="sxs-lookup"><span data-stu-id="effb5-115">The first step is to set the **Filter** property on the **Recordset** equal to **adFilterConflictingRecords** (the **Filter** property is discussed in the preceding chapter).</span></span> <span data-ttu-id="effb5-116">Этот параметр ограничивает представления на набора **записей** только те записи, которые находятся в конфликта.</span><span class="sxs-lookup"><span data-stu-id="effb5-116">This limits the view on your **Recordset** to only those records that are in conflict.</span></span> <span data-ttu-id="effb5-117">Если свойство **RecordCount** равна нулю после выполнения этого шага, известно, что не конфликта возникшей ошибке.</span><span class="sxs-lookup"><span data-stu-id="effb5-117">If the **RecordCount** property is equal to zero after this step, you know the error was raised by something other than a conflict.</span></span>

<span data-ttu-id="effb5-118">При вызове **BatchUpdate**, ADO и поставщика Создание инструкций SQL для выполнения операций обновления в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="effb5-118">When you call **BatchUpdate**, ADO and the provider are generating SQL statements to perform updates on the data source.</span></span> <span data-ttu-id="effb5-119">Помните, что некоторые источники данных ограничения, на которых можно использовать типы столбцов в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="effb5-119">Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</span></span>

<span data-ttu-id="effb5-120">Затем вызовите метод **выполнить повторную синхронизацию** для **набора записей** с аргументом *AffectRecords* , равным **adAffectGroup** и *ResyncValues* аргумент, равным **adResyncUnderlyingValues**.</span><span class="sxs-lookup"><span data-stu-id="effb5-120">Next, call the **Resync** method on the **Recordset** with the *AffectRecords* argument set equal to **adAffectGroup** and the *ResyncValues* argument set equal to **adResyncUnderlyingValues**.</span></span> <span data-ttu-id="effb5-121">Метод **выполнить повторную синхронизацию** обновляет данные в текущий объект **набора записей** из базы данных.</span><span class="sxs-lookup"><span data-stu-id="effb5-121">The **Resync** method refreshes the data in the current **Recordset** object from the underlying database.</span></span> <span data-ttu-id="effb5-122">С помощью **adAffectGroup**, проверка того, что только записи, видны с текущий фильтр, параметр, то есть только конфликтующие записи заново синхронизируются с базой данных.</span><span class="sxs-lookup"><span data-stu-id="effb5-122">By using **adAffectGroup**, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</span></span> <span data-ttu-id="effb5-123">Это может сделать значительную разницу в производительности при работе с большого **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="effb5-123">This could make a significant performance difference if you are dealing with a large **Recordset**.</span></span> <span data-ttu-id="effb5-124">Путем установки для параметра аргумент *ResyncValues* **adResyncUnderlyingValues** при вызове **выполнить повторную синхронизацию**, убедитесь, что свойство **UnderlyingValue** будет содержать значение (конфликтующие) из базы данных, **значение** свойство будет обрабатывать значения, введенные пользователем, и, что свойство **OriginalValue** будет использоваться для хранения исходное значение для поля (значение, что и до последнего успешного вызова **UpdateBatch** ).</span><span class="sxs-lookup"><span data-stu-id="effb5-124">By setting the *ResyncValues* argument to **adResyncUnderlyingValues** when calling **Resync**, you ensure that the **UnderlyingValue** property will contain the (conflicting) value from the database, that the **Value** property will maintain the value entered by the user, and that the **OriginalValue** property will hold the original value for the field (the value it had before the last successful **UpdateBatch** call was made).</span></span> <span data-ttu-id="effb5-125">Затем можно использовать эти значения программным путем разрешения конфликта или требуют, чтобы выбрать значение, которое будет использоваться пользователь.</span><span class="sxs-lookup"><span data-stu-id="effb5-125">You can then use these values to resolve the conflict programmatically or require the user to choose the value that will be used.</span></span>

<span data-ttu-id="effb5-126">В следующем примере кода показан этот метод.</span><span class="sxs-lookup"><span data-stu-id="effb5-126">This technique is shown in the code example below.</span></span> <span data-ttu-id="effb5-127">Конфликт искусственно создается с помощью отдельных **записей** для изменения значения в таблице до вызова **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="effb5-127">The example artificially creates a conflict by using a separate **Recordset** to change a value in the underlying table before **UpdateBatch** is called.</span></span>

```vb 
 
'BeginConflicts 
    On Error GoTo ErrHandler: 
     
    Dim objRs1 As New ADODB.Recordset 
    Dim objRs2 As New ADODB.Recordset 
    Dim strSQL As String 
    Dim strMsg As String 
     
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2" 
                  
    'Open Rs and change a value 
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
    objRs1("Phone") = "(111) 555-1111" 
     
    'Introduce a conflict at the db... 
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText 
    objRs2("Phone") = "(999) 555-9999" 
    objRs2.Update 
    objRs2.Close 
    Set objRs2 = Nothing 
     
    On Error Resume Next 
    objRs1.UpdateBatch 
     
    If objRs1.ActiveConnection.Errors.Count <> 0 Then 
        Dim intConflicts As Integer 
         
        intConflicts = 0 
         
        objRs1.Filter = adFilterConflictingRecords 
         
        intConflicts = objRs1.RecordCount 
         
        'Resync so we can see the UnderlyingValue and offer user a choice. 
        'This sample only displays all three values and resets to original. 
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues 
         
        If intConflicts > 0 Then 
            strMsg = "A conflict occurred with updates for " & intConflicts & _ 
                     " record(s)." & vbCrLf & "The values will be restored" & _ 
                     " to their original values." & vbCrLf & vbCrLf 
                      
            objRs1.MoveFirst 
            While Not objRs1.EOF 
                strMsg = strMsg & "SHIPPER = " & objRs1("CompanyName") & vbCrLf 
                strMsg = strMsg & "Value = " & objRs1("Phone").Value & vbCrLf 
                strMsg = strMsg & "UnderlyingValue = " & _ 
                                   objRs1("Phone").UnderlyingValue & vbCrLf 
                strMsg = strMsg & "OriginalValue = " & _ 
                                   objRs1("Phone").OriginalValue & vbCrLf 
                strMsg = strMsg & vbCrLf & "Original value has been restored." 
                   
                MsgBox strMsg, vbOKOnly, _ 
                      "Conflict " & objRs1.AbsolutePosition & _ 
                      " of " & intConflicts 
                   
                objRs1("Phone").Value = objRs1("Phone").OriginalValue 
                objRs1.MoveNext 
            Wend 
             
            objRs1.UpdateBatch adAffectGroup 
        Else 
            'Other error occurred. Minimal handling in this example. 
             strMsg = "Errors occurred during the update. " & _ 
                        objRs1.ActiveConnection.Errors(0).Number & " " & _ 
                        objRs1.ActiveConnection.Errors(0).Description 
        End If 
         
        On Error GoTo 0 
    End If 
     
    objRs1.MoveFirst 
     
    'Clean up 
    objRs1.Close 
    Set objRs1 = Nothing 
    Exit Sub 
     
ErrHandler: 
    
    If Not objRs1 Is Nothing Then 
        If objRs1.State = adStateOpen Then objRs1.Close 
        Set objRs1 = Nothing 
    End If 
     
    If Not objRs2 Is Nothing Then 
        If objRs2.State = adStateOpen Then objRs2.Close 
        Set objRs2 = Nothing 
    End If 
     
    If Err <> 0 Then 
        MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
     
'EndConflicts 
```

<span data-ttu-id="effb5-128">Чтобы определить, какой тип конфликта произошла можно использовать свойство **состояние** текущей **записи** или **поля** .</span><span class="sxs-lookup"><span data-stu-id="effb5-128">You can use the **Status** property of the current **Record** or of a specific **Field** to determine what kind of a conflict has occurred.</span></span>

<span data-ttu-id="effb5-129">Более подробные сведения об ошибках, см [Глава 6: обработки ошибок](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="effb5-129">For more detailed information on error handling, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

