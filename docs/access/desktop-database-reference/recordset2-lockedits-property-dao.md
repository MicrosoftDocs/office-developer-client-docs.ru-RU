---
title: Recordset2.LockEdits Property (DAO)
TOCTitle: LockEdits Property
ms:assetid: 77055f44-f8e9-ac64-ecc3-144ddb4a4558
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196045(v=office.15)
ms:contentKeyID: 48545716
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c963e4dfe2c1d507845333b7c20efe23aaf050f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872531"
---
# <a name="recordset2lockedits-property-dao"></a><span data-ttu-id="7a260-102">Recordset2.LockEdits Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="7a260-102">Recordset2.LockEdits Property (DAO)</span></span>


<span data-ttu-id="7a260-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a260-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7a260-104">Задает или возвращает значение, указывающее тип блокировки, который фактически во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="7a260-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a260-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a260-105">Syntax</span></span>

<span data-ttu-id="7a260-106">*выражение* . LockEdits</span><span class="sxs-lookup"><span data-stu-id="7a260-106">*expression* .LockEdits</span></span>

<span data-ttu-id="7a260-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="7a260-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a260-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="7a260-108">Remarks</span></span>

<span data-ttu-id="7a260-109">Параметр или возвращаемое значение указывает тип блокировки, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="7a260-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a260-110">Значение</span><span class="sxs-lookup"><span data-stu-id="7a260-110">Value</span></span></p></th>
<th><p><span data-ttu-id="7a260-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7a260-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a260-112">True</span><span class="sxs-lookup"><span data-stu-id="7a260-112">True</span></span></p></td>
<td><p><span data-ttu-id="7a260-113">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a260-113">Default.</span></span> <span data-ttu-id="7a260-114">Жесткой блокировки действует.</span><span class="sxs-lookup"><span data-stu-id="7a260-114">Pessimistic locking is in effect.</span></span> <span data-ttu-id="7a260-115">На этой странице содержится запись, которую требуется изменить заблокированный сразу после вызова метода Правка.</span><span class="sxs-lookup"><span data-stu-id="7a260-115">The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a260-116">False</span><span class="sxs-lookup"><span data-stu-id="7a260-116">False</span></span></p></td>
<td><p><span data-ttu-id="7a260-117">Оптимистичный блокировки применяется для редактирования.</span><span class="sxs-lookup"><span data-stu-id="7a260-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="7a260-118">На этой странице содержится запись не блокируется до выполнения метода Update.</span><span class="sxs-lookup"><span data-stu-id="7a260-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7a260-119">Свойство **LockEdits** с обновляемым объекты **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="7a260-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="7a260-120">Если страницу заблокирован, другой пользователь не может редактировать записи на той же странице.</span><span class="sxs-lookup"><span data-stu-id="7a260-120">If a page is locked, no other user can edit records on the same page.</span></span> <span data-ttu-id="7a260-121">Если **LockEdits** задать **значение True** , а другой пользователь уже имеет странице блокируется, возникает ошибка при использовании метода **Edit** .</span><span class="sxs-lookup"><span data-stu-id="7a260-121">If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method.</span></span> <span data-ttu-id="7a260-122">Другие пользователи могут читать данные из страниц в заблокированной.</span><span class="sxs-lookup"><span data-stu-id="7a260-122">Other users can read data from locked pages.</span></span>

<span data-ttu-id="7a260-123">Если **LockEdits** свойству присвоено **значение False** и более поздних версий используйте метод **Update** в процессе странице заблокирован другим пользователем, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="7a260-123">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs.</span></span> <span data-ttu-id="7a260-124">Чтобы просмотреть изменения, внесенные записи другим пользователем, используйте метод **[Move](recordset2-move-method-dao.md)** с 0 в качестве аргумента; Тем не менее при этом будут потеряны изменения.</span><span class="sxs-lookup"><span data-stu-id="7a260-124">To see the changes made to your record by another user, use the **[Move](recordset2-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="7a260-125">При работе с источниками данных ODBC подключением модуля Microsoft Access базы данных, свойство **LockEdits** всегда имеет значение **False**или оптимистичный блокировки.</span><span class="sxs-lookup"><span data-stu-id="7a260-125">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking.</span></span> <span data-ttu-id="7a260-126">Ядро СУБД Microsoft Access не контролирует механизмы блокировки, используемые на серверах внешней базе данных.</span><span class="sxs-lookup"><span data-stu-id="7a260-126">The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7a260-127">Значение <STRONG>LockEdits</STRONG> могут быть предварительно при первом открытии <STRONG>набора записей</STRONG> , задав аргумент lockedits <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> метода.</span><span class="sxs-lookup"><span data-stu-id="7a260-127">You can preset the value of <STRONG>LockEdits</STRONG> when you first open the <STRONG>Recordset</STRONG> by setting the lockedits argument of the <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> method.</span></span> <span data-ttu-id="7a260-128">Установка для аргумента lockedits <STRONG>dbPessimistic</STRONG> будет <STRONG>LockEdits</STRONG> свойству присвоено <STRONG>значение True,</STRONG>и lockedits параметр к любым другим значением будет <STRONG>LockEdits</STRONG> свойству присвоено <STRONG>значение False</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="7a260-128">Setting the lockedits argument to <STRONG>dbPessimistic</STRONG> will set the <STRONG>LockEdits</STRONG> property to <STRONG>True</STRONG>, and setting lockedits to any other value will set the <STRONG>LockEdits</STRONG> property to <STRONG>False</STRONG>.</span></span></P>



## <a name="example"></a><span data-ttu-id="7a260-129">Пример</span><span class="sxs-lookup"><span data-stu-id="7a260-129">Example</span></span>

<span data-ttu-id="7a260-130">В этом примере демонстрируется жесткой блокировки, задав свойство **LockEdits** значение **True**, а затем оптимистичный блокировки, задав свойство **LockEdits** значение False.</span><span class="sxs-lookup"><span data-stu-id="7a260-130">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False.</span></span> <span data-ttu-id="7a260-131">Также показано, какие виды обработки ошибок необходим в среде многопользовательской базы данных для изменения поля.</span><span class="sxs-lookup"><span data-stu-id="7a260-131">It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field.</span></span> <span data-ttu-id="7a260-132">Функции PessimisticLock и OptimisticLock, необходимые для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="7a260-132">The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

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
