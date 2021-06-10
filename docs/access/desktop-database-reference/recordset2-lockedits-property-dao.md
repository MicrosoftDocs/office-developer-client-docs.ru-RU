---
title: Свойство Recordset2.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff2db22dcb0119792eb57a971d3cf36e763d3049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309648"
---
# <a name="recordset2lockedits-property-dao"></a><span data-ttu-id="8ed2e-102">Свойство Recordset2.LockEdits (DAO)</span><span class="sxs-lookup"><span data-stu-id="8ed2e-102">Recordset2.LockEdits property (DAO)</span></span>

<span data-ttu-id="8ed2e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ed2e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ed2e-104">Задает или возвращает значение, определяющее тип блокировки, которая действует во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed2e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ed2e-105">Syntax</span></span>

<span data-ttu-id="8ed2e-106">*выражения* . LockEdits</span><span class="sxs-lookup"><span data-stu-id="8ed2e-106">*expression* .LockEdits</span></span>

<span data-ttu-id="8ed2e-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="8ed2e-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed2e-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="8ed2e-108">Remarks</span></span>

<span data-ttu-id="8ed2e-109">Значение параметра или возврата указывает тип блокировки, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ed2e-110">Значение</span><span class="sxs-lookup"><span data-stu-id="8ed2e-110">Value</span></span></p></th>
<th><p><span data-ttu-id="8ed2e-111">Описание</span><span class="sxs-lookup"><span data-stu-id="8ed2e-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ed2e-112">True (Истина)</span><span class="sxs-lookup"><span data-stu-id="8ed2e-112">True</span></span></p></td>
<td><p><span data-ttu-id="8ed2e-113">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-113">Default.</span></span> <span data-ttu-id="8ed2e-114">Пессимистическая блокировка действует.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-114">Pessimistic locking is in effect.</span></span> <span data-ttu-id="8ed2e-115">Страница, содержащая записи, которые вы редактируете, блокируется сразу же после вызова метода Редактирования.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-115">The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ed2e-116">False (Ложь)</span><span class="sxs-lookup"><span data-stu-id="8ed2e-116">False</span></span></p></td>
<td><p><span data-ttu-id="8ed2e-117">Для редактирования действует оптимистичная блокировка.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="8ed2e-118">Страница, содержащая запись, не блокируется до выполнения метода Update.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ed2e-119">Свойство **LockEdits можно** использовать с помощью updatable **[объектов Recordset.](recordset-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="8ed2e-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="8ed2e-120">Если страница заблокирована, никто другой пользователь не может редактировать записи на той же странице.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-120">If a page is locked, no other user can edit records on the same page.</span></span> <span data-ttu-id="8ed2e-121">Если вы установите **LockEdits** для **True** и у другого пользователя уже заблокирована страница, при использовании метода **Редактирования** возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-121">If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method.</span></span> <span data-ttu-id="8ed2e-122">Другие пользователи могут читать данные с заблокированных страниц.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-122">Other users can read data from locked pages.</span></span>

<span data-ttu-id="8ed2e-123">Если вы установите свойство **LockEdits** false, а затем используйте метод **Update,** а другой пользователь заблокировали страницу, возникает ошибка. </span><span class="sxs-lookup"><span data-stu-id="8ed2e-123">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs.</span></span> <span data-ttu-id="8ed2e-124">Чтобы увидеть изменения, внесенные в запись другим пользователем, используйте метод **[Move](recordset2-move-method-dao.md)** с 0 в качестве аргумента; однако, если вы сделаете это, вы потеряете свои изменения.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-124">To see the changes made to your record by another user, use the **[Move](recordset2-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="8ed2e-125">При работе с источниками данных базы данных Microsoft Access, подключенными к базе данных ODBC, свойство **LockEdits** всегда задает ложную или оптимистичную блокировку.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-125">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking.</span></span> <span data-ttu-id="8ed2e-126">Двигатель базы данных Microsoft Access не контролирует механизмы блокировки, используемые на внешних серверах баз данных.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-126">The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>

> [!NOTE]
> <span data-ttu-id="8ed2e-127">Вы можете предустановить значение **LockEdits** при первом открываемом наборе записей, задав аргумент lockedits метода **[OpenRecordset.](connection-openrecordset-method-dao.md)** </span><span class="sxs-lookup"><span data-stu-id="8ed2e-127">You can preset the value of **LockEdits** when you first open the **Recordset** by setting the lockedits argument of the **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span> <span data-ttu-id="8ed2e-128">Настройка аргумента lockedits для **dbPessimistic** заведет свойство **LockEdits** значение **True,** а параметр lockedits к любому другому значению заведет свойство **LockEdits** значение **False**.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-128">Setting the lockedits argument to **dbPessimistic** will set the **LockEdits** property to **True**, and setting lockedits to any other value will set the **LockEdits** property to **False**.</span></span>

## <a name="example"></a><span data-ttu-id="8ed2e-129">Пример</span><span class="sxs-lookup"><span data-stu-id="8ed2e-129">Example</span></span>

<span data-ttu-id="8ed2e-130">В этом примере демонстрируется пессимистическая блокировка, установив свойство **LockEdits** **true,** а затем демонстрирует оптимистичную блокировку, установив свойство **LockEdits** false.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-130">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False.</span></span> <span data-ttu-id="8ed2e-131">В нем также показано, какая обработка ошибок требуется в многоуровневой среде базы данных для изменения поля.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-131">It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field.</span></span> <span data-ttu-id="8ed2e-132">Для запуска этой процедуры необходимы функции PessimisticLock и OptimisticLock.</span><span class="sxs-lookup"><span data-stu-id="8ed2e-132">The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset2 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset2, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
