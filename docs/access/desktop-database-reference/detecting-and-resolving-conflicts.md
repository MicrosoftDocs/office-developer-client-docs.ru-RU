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
# <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="83107-102">Обнаружение и разрешение конфликтов</span><span class="sxs-lookup"><span data-stu-id="83107-102">Detecting and resolving conflicts</span></span>

<span data-ttu-id="83107-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83107-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="83107-104">Detecting and Resolving Conflicts</span><span class="sxs-lookup"><span data-stu-id="83107-104">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="83107-105">Если вы имеете дело с набором **записей** в немедленном режиме, вероятность возникновения проблем с совме характера значительно ниже.</span><span class="sxs-lookup"><span data-stu-id="83107-105">If you are dealing with your **Recordset** in immediate mode, there is much less chance for concurrency problems to arise.</span></span> <span data-ttu-id="83107-106">С другой стороны, если приложение использует пакетное обновление, существует вероятность того, что один пользователь изменит запись, прежде чем изменения, внесенные другим пользователем, редактирует эту же запись, будут сохранены.</span><span class="sxs-lookup"><span data-stu-id="83107-106">On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes made by another user editing the same record are saved.</span></span> <span data-ttu-id="83107-107">В таком случае необходимо, чтобы приложение корректно обрабатывал конфликт.</span><span class="sxs-lookup"><span data-stu-id="83107-107">In such a case, you will want your application to gracefully handle the conflict.</span></span> <span data-ttu-id="83107-108">Возможно, вы хотите, чтобы последнее лицо отправило обновление на сервер "wins".</span><span class="sxs-lookup"><span data-stu-id="83107-108">It may be your wish that the last person to send an update to the server "wins."</span></span> <span data-ttu-id="83107-109">Или вы можете позволить последнему пользователю решить, какое обновление должно иметь приоритет, предоставив ему возможность выбора между двумя конфликтующие значениями.</span><span class="sxs-lookup"><span data-stu-id="83107-109">Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</span></span>

<span data-ttu-id="83107-110">В любом случае ADO предоставляет свойства **UnderlyingValue** и **OriginalValue** объекта **Field** для обработки таких типов конфликтов.</span><span class="sxs-lookup"><span data-stu-id="83107-110">Whatever the case, ADO provides the **UnderlyingValue** and **OriginalValue** properties of the **Field** object in order to handle these types of conflicts.</span></span> <span data-ttu-id="83107-111">Используйте эти свойства в сочетании с методом **Resync** и **свойством Filter** объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="83107-111">Use these properties in combination with the **Resync** method and **Filter** property of the **Recordset**.</span></span>

## <a name="detecting-errors"></a><span data-ttu-id="83107-112">Detecting Errors</span><span class="sxs-lookup"><span data-stu-id="83107-112">Detecting Errors</span></span>

<span data-ttu-id="83107-113">Когда ADO сталкивается с конфликтом во время пакетного обновления, в коллекцию **ошибок** помещается предупреждение.</span><span class="sxs-lookup"><span data-stu-id="83107-113">When ADO encounters a conflict during a batch update, a warning will be placed in the **Errors** collection.</span></span> <span data-ttu-id="83107-114">Поэтому всегда следует проверять ошибки сразу после вызова **BatchUpdate,** и если они находятся, начните проверку предположения о том, что возник конфликт.</span><span class="sxs-lookup"><span data-stu-id="83107-114">Therefore, you should always check for errors immediately after calling **BatchUpdate**, and if you find them, begin testing the assumption that you have encountered a conflict.</span></span> <span data-ttu-id="83107-115">Первый шаг — установить для свойства **Filter** в наборе **записей** свойство **adFilterConflictingRecords** (свойство **Filter** обсуждается в предыдущей главе).</span><span class="sxs-lookup"><span data-stu-id="83107-115">The first step is to set the **Filter** property on the **Recordset** equal to **adFilterConflictingRecords** (the **Filter** property is discussed in the preceding chapter).</span></span> <span data-ttu-id="83107-116">Это ограничивает представление в наборе **recordset** только теми записями, которые находятся в конфликте.</span><span class="sxs-lookup"><span data-stu-id="83107-116">This limits the view on your **Recordset** to only those records that are in conflict.</span></span> <span data-ttu-id="83107-117">Если после этого шага свойство **RecordCount** равно нулю, вы знаете, что ошибка была иной, чем конфликт.</span><span class="sxs-lookup"><span data-stu-id="83107-117">If the **RecordCount** property is equal to zero after this step, you know the error was raised by something other than a conflict.</span></span>

<span data-ttu-id="83107-118">При **вызове BatchUpdate** ADO и поставщик SQL для выполнения обновлений в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="83107-118">When you call **BatchUpdate**, ADO and the provider are generating SQL statements to perform updates on the data source.</span></span> <span data-ttu-id="83107-119">Помните, что определенные источники данных имеют ограничения на типы столбцов, которые можно использовать в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="83107-119">Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</span></span>

<span data-ttu-id="83107-120">Затем вызовите метод **Resync** в **наборе recordset** с аргументом *AffectRecords,* равным **adAffectGroup,** а аргумент *ResyncValues* равен **adResyncUnderlyingValues.**</span><span class="sxs-lookup"><span data-stu-id="83107-120">Next, call the **Resync** method on the **Recordset** with the *AffectRecords* argument set equal to **adAffectGroup** and the *ResyncValues* argument set equal to **adResyncUnderlyingValues**.</span></span> <span data-ttu-id="83107-121">Метод **Resync** обновляет данные в текущем объекте **Recordset** из баз данных.</span><span class="sxs-lookup"><span data-stu-id="83107-121">The **Resync** method refreshes the data in the current **Recordset** object from the underlying database.</span></span> <span data-ttu-id="83107-122">Используя **adAffectGroup,** вы обеспечиваете синхронизацию с базой данных только записей, видимых с помощью текущего параметра фильтра, то есть только конфликтующих записей.</span><span class="sxs-lookup"><span data-stu-id="83107-122">By using **adAffectGroup**, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</span></span> <span data-ttu-id="83107-123">Это может существенно изменить производительность при работе с большим набором **записей.**</span><span class="sxs-lookup"><span data-stu-id="83107-123">This could make a significant performance difference if you are dealing with a large **Recordset**.</span></span> <span data-ttu-id="83107-124">Задав для аргумента *ResyncValues* значение **adResyncUnderlyingValues** при вызове **Resync,** вы гарантируете, что свойство **UnderlyingValue** будет содержать (конфликтующие) значения из базы данных, что свойство **Value** будет поддерживать введенное пользователем значение, а свойство **OriginalValue** будет содержать исходное значение поля (значение, которое оно было до последнего успешного вызова **UpdateBatch).**</span><span class="sxs-lookup"><span data-stu-id="83107-124">By setting the *ResyncValues* argument to **adResyncUnderlyingValues** when calling **Resync**, you ensure that the **UnderlyingValue** property will contain the (conflicting) value from the database, that the **Value** property will maintain the value entered by the user, and that the **OriginalValue** property will hold the original value for the field (the value it had before the last successful **UpdateBatch** call was made).</span></span> <span data-ttu-id="83107-125">Затем вы можете использовать эти значения для разрешения конфликта программным путем или потребовать от пользователя выбрать значение, которое будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="83107-125">You can then use these values to resolve the conflict programmatically or require the user to choose the value that will be used.</span></span>

<span data-ttu-id="83107-126">Этот метод показан в примере кода ниже.</span><span class="sxs-lookup"><span data-stu-id="83107-126">This technique is shown in the code example below.</span></span> <span data-ttu-id="83107-127">В этом примере искусственно создается  конфликт с помощью отдельного наборов записей для изменения значения в таблице перед тем, как будет вызван **UpdateBatch.**</span><span class="sxs-lookup"><span data-stu-id="83107-127">The example artificially creates a conflict by using a separate **Recordset** to change a value in the underlying table before **UpdateBatch** is called.</span></span>

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

<span data-ttu-id="83107-128">Можно использовать свойство **Status** текущей  записи или  определенного поля, чтобы определить, какой тип конфликта произошел.</span><span class="sxs-lookup"><span data-stu-id="83107-128">You can use the **Status** property of the current **Record** or of a specific **Field** to determine what kind of a conflict has occurred.</span></span>

<span data-ttu-id="83107-129">Дополнительные сведения об обработке ошибок см. в главе [6 "Обработка ошибок".](chapter-6-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="83107-129">For more detailed information on error handling, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

