---
title: Свойство Recordset.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: baa11b24-a330-eaa4-bd03-b8b9739d209e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822514(v=office.15)
ms:contentKeyID: 48547379
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052877
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 81c7b3e2474ee6cbcd8e45b61369e22f20440587
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996757"
---
# <a name="recordsetlockedits-property-dao"></a><span data-ttu-id="40002-102">Свойство Recordset.LockEdits (DAO)</span><span class="sxs-lookup"><span data-stu-id="40002-102">Recordset.LockEdits property (DAO)</span></span>

<span data-ttu-id="40002-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="40002-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40002-104">Задает или возвращает значение, указывающее тип блокировки, который фактически во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="40002-104">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="40002-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40002-105">Syntax</span></span>

<span data-ttu-id="40002-106">*выражение* . LockEdits</span><span class="sxs-lookup"><span data-stu-id="40002-106">*expression* .LockEdits</span></span>

<span data-ttu-id="40002-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="40002-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="40002-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="40002-108">Remarks</span></span>

<span data-ttu-id="40002-109">Параметр или возвращаемое значение указывает тип блокировки, как указано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="40002-109">The setting or return value indicates the type of locking, as specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40002-110">Значение</span><span class="sxs-lookup"><span data-stu-id="40002-110">Value</span></span></p></th>
<th><p><span data-ttu-id="40002-111">Описание</span><span class="sxs-lookup"><span data-stu-id="40002-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40002-112">True</span><span class="sxs-lookup"><span data-stu-id="40002-112">True</span></span></p></td>
<td><p><span data-ttu-id="40002-113">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="40002-113">Default.</span></span> <span data-ttu-id="40002-114">Жесткой блокировки действует.</span><span class="sxs-lookup"><span data-stu-id="40002-114">Pessimistic locking is in effect.</span></span> <span data-ttu-id="40002-115">На этой странице содержится запись, которую требуется изменить заблокированный сразу после вызова метода Правка.</span><span class="sxs-lookup"><span data-stu-id="40002-115">The page containing the record you're editing is locked as soon as you call the Edit method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40002-116">False</span><span class="sxs-lookup"><span data-stu-id="40002-116">False</span></span></p></td>
<td><p><span data-ttu-id="40002-117">Оптимистичный блокировки применяется для редактирования.</span><span class="sxs-lookup"><span data-stu-id="40002-117">Optimistic locking is in effect for editing.</span></span> <span data-ttu-id="40002-118">На этой странице содержится запись не блокируется до выполнения метода Update.</span><span class="sxs-lookup"><span data-stu-id="40002-118">The page containing the record is not locked until the Update method is executed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40002-119">Свойство **LockEdits** с обновляемым объекты **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="40002-119">You can use the **LockEdits** property with updatable **[Recordset](recordset-object-dao.md)** objects.</span></span>

<span data-ttu-id="40002-120">Если страницу заблокирован, другой пользователь не может редактировать записи на той же странице.</span><span class="sxs-lookup"><span data-stu-id="40002-120">If a page is locked, no other user can edit records on the same page.</span></span> <span data-ttu-id="40002-121">Если **LockEdits** задать **значение True** , а другой пользователь уже имеет странице блокируется, возникает ошибка при использовании метода **Edit** .</span><span class="sxs-lookup"><span data-stu-id="40002-121">If you set **LockEdits** to **True** and another user already has the page locked, an error occurs when you use the **Edit** method.</span></span> <span data-ttu-id="40002-122">Другие пользователи могут читать данные из страниц в заблокированной.</span><span class="sxs-lookup"><span data-stu-id="40002-122">Other users can read data from locked pages.</span></span>

<span data-ttu-id="40002-123">Если **LockEdits** свойству присвоено **значение False** и более поздних версий используйте метод **Update** в процессе странице заблокирован другим пользователем, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="40002-123">If you set the **LockEdits** property to **False** and later use the **Update** method while another user has the page locked, an error occurs.</span></span> <span data-ttu-id="40002-124">Чтобы просмотреть изменения, внесенные записи другим пользователем, используйте метод **[Move](recordset-move-method-dao.md)** с 0 в качестве аргумента; Тем не менее при этом будут потеряны изменения.</span><span class="sxs-lookup"><span data-stu-id="40002-124">To see the changes made to your record by another user, use the **[Move](recordset-move-method-dao.md)** method with 0 as the argument; however, if you do this, you will lose your changes.</span></span>

<span data-ttu-id="40002-125">При работе с источниками данных ODBC подключением модуля Microsoft Access базы данных, свойство **LockEdits** всегда имеет значение **False**или оптимистичный блокировки.</span><span class="sxs-lookup"><span data-stu-id="40002-125">When working with Microsoft Access database engine-connected ODBC data sources, the **LockEdits** property is always set to **False**, or optimistic locking.</span></span> <span data-ttu-id="40002-126">Ядро СУБД Microsoft Access не контролирует механизмы блокировки, используемые на серверах внешней базе данных.</span><span class="sxs-lookup"><span data-stu-id="40002-126">The Microsoft Access database engine has no control over the locking mechanisms used in external database servers.</span></span>

> [!NOTE]
> <span data-ttu-id="40002-127">Значение **LockEdits** могут быть предварительно при первом открытии **набора записей** , задав аргумент lockedits **[OpenRecordset](connection-openrecordset-method-dao.md)** метода.</span><span class="sxs-lookup"><span data-stu-id="40002-127">You can preset the value of **LockEdits** when you first open the **Recordset** by setting the lockedits argument of the **[OpenRecordset](connection-openrecordset-method-dao.md)** method.</span></span> <span data-ttu-id="40002-128">Установка для аргумента lockedits **dbPessimistic** будет **LockEdits** свойству присвоено **значение True,** и lockedits параметр к любым другим значением будет **LockEdits** свойству присвоено **значение False**.</span><span class="sxs-lookup"><span data-stu-id="40002-128">Setting the lockedits argument to **dbPessimistic** will set the **LockEdits** property to **True**, and setting lockedits to any other value will set the **LockEdits** property to **False**.</span></span>

## <a name="example"></a><span data-ttu-id="40002-129">Пример</span><span class="sxs-lookup"><span data-stu-id="40002-129">Example</span></span>

<span data-ttu-id="40002-130">В этом примере демонстрируется жесткой блокировки, задав свойство **LockEdits** значение **True**, а затем оптимистичный блокировки, задав свойство **LockEdits** значение False.</span><span class="sxs-lookup"><span data-stu-id="40002-130">This example demonstrates pessimistic locking by setting the **LockEdits** property to **True**, and then demonstrates optimistic locking by setting the **LockEdits** property to False.</span></span> <span data-ttu-id="40002-131">Также показано, какие виды обработки ошибок необходим в среде многопользовательской базы данных для изменения поля.</span><span class="sxs-lookup"><span data-stu-id="40002-131">It also demonstrates what kind of error handling is required in a multiuser database environment in order to modify a field.</span></span> <span data-ttu-id="40002-132">Функции PessimisticLock и OptimisticLock, необходимые для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="40002-132">The PessimisticLock and OptimisticLock functions are required for this procedure to run.</span></span>

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset 
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
     
    Function PessimisticLock(rstTemp As Recordset, _ 
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
