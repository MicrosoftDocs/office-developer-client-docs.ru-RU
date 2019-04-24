---
title: Обнаружение и разрешение конфликтов
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd7566be2581fe449872eb576bf7f11e5a806fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293926"
---
# <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="18d17-102">Обнаружение и разрешение конфликтов</span><span class="sxs-lookup"><span data-stu-id="18d17-102">Detecting and resolving conflicts</span></span>

<span data-ttu-id="18d17-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18d17-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="18d17-104">Detecting and Resolving Conflicts</span><span class="sxs-lookup"><span data-stu-id="18d17-104">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="18d17-105">При работе с **наборОм записей** в режиме интерпретации возникает вероятность возникновения проблем с параллелизмом.</span><span class="sxs-lookup"><span data-stu-id="18d17-105">If you are dealing with your **Recordset** in immediate mode, there is much less chance for concurrency problems to arise.</span></span> <span data-ttu-id="18d17-106">С другой стороны, если ваше приложение использует обновление в пакетном режиме, может возникнуть подозрение, что один пользователь изменит запись, прежде чем изменения, внесенные другим пользователем при редактировании той же записи, будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="18d17-106">On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes made by another user editing the same record are saved.</span></span> <span data-ttu-id="18d17-107">В этом случае вам потребуется, чтобы ваше приложение корректно обрабатывал конфликт.</span><span class="sxs-lookup"><span data-stu-id="18d17-107">In such a case, you will want your application to gracefully handle the conflict.</span></span> <span data-ttu-id="18d17-108">Возможно, вы хотите, чтобы последний пользователь отправлял обновление на сервер "WINS".</span><span class="sxs-lookup"><span data-stu-id="18d17-108">It may be your wish that the last person to send an update to the server "wins."</span></span> <span data-ttu-id="18d17-109">Или вы можете предоставить самому последнему пользователю выбрать, какое обновление будет иметь приоритет, предоставив ему выбор между двумя конфликтующими значениями.</span><span class="sxs-lookup"><span data-stu-id="18d17-109">Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</span></span>

<span data-ttu-id="18d17-110">Как и в случае, ADO предоставляет свойства **UnderlyingValue** и **originalValue** объекта **field** для обработки этих типов конфликтов.</span><span class="sxs-lookup"><span data-stu-id="18d17-110">Whatever the case, ADO provides the **UnderlyingValue** and **OriginalValue** properties of the **Field** object in order to handle these types of conflicts.</span></span> <span data-ttu-id="18d17-111">Используйте эти свойства в сочетании с методом **Resync** и свойством **Filter** объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="18d17-111">Use these properties in combination with the **Resync** method and **Filter** property of the **Recordset**.</span></span>

## <a name="detecting-errors"></a><span data-ttu-id="18d17-112">Detecting Errors</span><span class="sxs-lookup"><span data-stu-id="18d17-112">Detecting Errors</span></span>

<span data-ttu-id="18d17-113">Если при пакетном обновлении ADO обнаруживает конфликт, в коллекцию **Errors** будет включено предупреждение.</span><span class="sxs-lookup"><span data-stu-id="18d17-113">When ADO encounters a conflict during a batch update, a warning will be placed in the **Errors** collection.</span></span> <span data-ttu-id="18d17-114">Таким образом, следует всегда проверять наличие ошибок сразу же после вызова **батчупдате**, и если вы их обнаружите, начните проверку предположения, что вы столкнулись с конфликтом.</span><span class="sxs-lookup"><span data-stu-id="18d17-114">Therefore, you should always check for errors immediately after calling **BatchUpdate**, and if you find them, begin testing the assumption that you have encountered a conflict.</span></span> <span data-ttu-id="18d17-115">Первый шаг — установка свойства **Filter** в **наборе записей** , равного **адфилтерконфликтингрекордс** (свойство **Filter** рассматривается в предыдущей главе).</span><span class="sxs-lookup"><span data-stu-id="18d17-115">The first step is to set the **Filter** property on the **Recordset** equal to **adFilterConflictingRecords** (the **Filter** property is discussed in the preceding chapter).</span></span> <span data-ttu-id="18d17-116">Это ограничит представление объекта **Recordset** только теми записями, в которых возник конфликт.</span><span class="sxs-lookup"><span data-stu-id="18d17-116">This limits the view on your **Recordset** to only those records that are in conflict.</span></span> <span data-ttu-id="18d17-117">Если после этого шага свойство **RecordCount** равно нулю, вы знаете, что ошибка вызвана не с помощью конфликта.</span><span class="sxs-lookup"><span data-stu-id="18d17-117">If the **RecordCount** property is equal to zero after this step, you know the error was raised by something other than a conflict.</span></span>

<span data-ttu-id="18d17-118">При вызове **батчупдате**ADO и поставщик создают инструкции SQL для выполнения обновлений источника данных.</span><span class="sxs-lookup"><span data-stu-id="18d17-118">When you call **BatchUpdate**, ADO and the provider are generating SQL statements to perform updates on the data source.</span></span> <span data-ttu-id="18d17-119">Помните, что определенные источники данных имеют ограничения на типы столбцов, которые можно использовать в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="18d17-119">Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</span></span>

<span data-ttu-id="18d17-120">Затем вызовите метод **Resync** для объекта **Recordset** с набором аргументов *аффектрекордс* , равным **адаффектграуп** , а аргумент *ресинквалуес* , равным **адресинкундерлингвалуес**.</span><span class="sxs-lookup"><span data-stu-id="18d17-120">Next, call the **Resync** method on the **Recordset** with the *AffectRecords* argument set equal to **adAffectGroup** and the *ResyncValues* argument set equal to **adResyncUnderlyingValues**.</span></span> <span data-ttu-id="18d17-121">Метод **Resync** обновляет данные в текущем объекте **Recordset** из базовой базы данных.</span><span class="sxs-lookup"><span data-stu-id="18d17-121">The **Resync** method refreshes the data in the current **Recordset** object from the underlying database.</span></span> <span data-ttu-id="18d17-122">С помощью **адаффектграуп**вы гарантируете, что только записи, отображаемые с текущим параметром фильтра, то есть только конфликтующие записи, повторно синхронизируются с базой данных.</span><span class="sxs-lookup"><span data-stu-id="18d17-122">By using **adAffectGroup**, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</span></span> <span data-ttu-id="18d17-123">Это может значительно увеличить производительность, если вы работаете с большим **наборОм записей**.</span><span class="sxs-lookup"><span data-stu-id="18d17-123">This could make a significant performance difference if you are dealing with a large **Recordset**.</span></span> <span data-ttu-id="18d17-124">Если присвоить аргументу *ресинквалуес* значение **адресинкундерлингвалуес** при вызове Resync, убедитесь, что в свойстве **UnderlyingValue** будет содержаться значение (конфликтующее) из базы данных, то есть **значение** \*\*\*\* Свойство сохранит значение, введенное пользователем, и что свойство **originalValue** будет содержать исходное значение поля (значение, которое оно имело до последнего успешного вызова **UpdateBatch** ).</span><span class="sxs-lookup"><span data-stu-id="18d17-124">By setting the *ResyncValues* argument to **adResyncUnderlyingValues** when calling **Resync**, you ensure that the **UnderlyingValue** property will contain the (conflicting) value from the database, that the **Value** property will maintain the value entered by the user, and that the **OriginalValue** property will hold the original value for the field (the value it had before the last successful **UpdateBatch** call was made).</span></span> <span data-ttu-id="18d17-125">Затем эти значения можно использовать для программного разрешения конфликта или для того, чтобы пользователь мог выбрать значение, которое будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="18d17-125">You can then use these values to resolve the conflict programmatically or require the user to choose the value that will be used.</span></span>

<span data-ttu-id="18d17-126">Этот метод показан в приведенном ниже примере кода.</span><span class="sxs-lookup"><span data-stu-id="18d17-126">This technique is shown in the code example below.</span></span> <span data-ttu-id="18d17-127">В этом примере искусственно создается конфликт с помощью отдельного **набора записей** для изменения значения в базовой таблице перед вызовом **UpdateBatch** .</span><span class="sxs-lookup"><span data-stu-id="18d17-127">The example artificially creates a conflict by using a separate **Recordset** to change a value in the underlying table before **UpdateBatch** is called.</span></span>

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

<span data-ttu-id="18d17-128">Можно использовать свойство **Status** текущей **записи** или определенного **поля** , чтобы определить, какой тип конфликта был вызван.</span><span class="sxs-lookup"><span data-stu-id="18d17-128">You can use the **Status** property of the current **Record** or of a specific **Field** to determine what kind of a conflict has occurred.</span></span>

<span data-ttu-id="18d17-129">Более подробную информацию об обработке ошибок можно найти в [главе 6: обработка ошибок](chapter-6-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="18d17-129">For more detailed information on error handling, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

