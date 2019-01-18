---
title: Метод DBEngine.Idle (DAO)
TOCTitle: Idle Method
ms:assetid: c90b565e-626e-139d-102a-0386601ce0c8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823202(v=office.15)
ms:contentKeyID: 48547666
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052978
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7a84e3cc4b35886a12b2e6b4cf92b7483fea293a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705115"
---
# <a name="dbengineidle-method-dao"></a><span data-ttu-id="0357a-102">Метод DBEngine.Idle (DAO)</span><span class="sxs-lookup"><span data-stu-id="0357a-102">DBEngine.Idle method (DAO)</span></span>

<span data-ttu-id="0357a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0357a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0357a-104">Выполняется приостановка обработки данных, позволяя ядро базы данных Microsoft Access завершить все ожидающие задач, таких как оптимизации памяти или время ожидания страницы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0357a-104">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0357a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0357a-105">Syntax</span></span>

<span data-ttu-id="0357a-106">*выражение* . Простоя (***Действие***)</span><span class="sxs-lookup"><span data-stu-id="0357a-106">*expression* .Idle(***Action***)</span></span>

<span data-ttu-id="0357a-107">*выражение* Переменная, которая представляет собой объект- **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="0357a-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="0357a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0357a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0357a-109">Имя</span><span class="sxs-lookup"><span data-stu-id="0357a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0357a-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="0357a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="0357a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0357a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="0357a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="0357a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0357a-113"><em>Action</em></span><span class="sxs-lookup"><span data-stu-id="0357a-113"><em>Action</em></span></span></p></td>
<td><p><span data-ttu-id="0357a-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="0357a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="0357a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="0357a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0357a-116">Указывает действие, которое выполняется.</span><span class="sxs-lookup"><span data-stu-id="0357a-116">Specifies the action to take.</span></span> <span data-ttu-id="0357a-117">Может быть <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> констант.</span><span class="sxs-lookup"><span data-stu-id="0357a-117">Can be one of the <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0357a-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="0357a-118">Remarks</span></span>

<span data-ttu-id="0357a-119">Метод **Idle** позволяет ядро базы данных Microsoft Access для выполнения фоновых задач, могут не соответствовать действительности из-за процесс обработки данных.</span><span class="sxs-lookup"><span data-stu-id="0357a-119">The **Idle** method allows the Microsoft Access database engine to perform background tasks that may not be up-to-date because of intense data processing.</span></span> <span data-ttu-id="0357a-120">Это особенно актуально в многопользовательской, многозадачных средах, которые не являются достаточно фоновую обработку времени хранения для всех записей в наборе **[записей](recordset-object-dao.md)** текущей.</span><span class="sxs-lookup"><span data-stu-id="0357a-120">This is often true in multiuser, multitasking environments that don't have enough background processing time to keep all records in a **[Recordset](recordset-object-dao.md)** current.</span></span>

<span data-ttu-id="0357a-121">Как правило доступ на чтение блокировки удаляются и данных в локальной добавляющий **набора записей** объекты обновляются только в том случае, если возникают никаких других действий (в том числе движения мыши).</span><span class="sxs-lookup"><span data-stu-id="0357a-121">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur.</span></span> <span data-ttu-id="0357a-122">При использовании метода **Idle** периодически ядро базы данных Microsoft Access можно захватить на фоновую обработку задачи освободить ненужные чтение блокировки.</span><span class="sxs-lookup"><span data-stu-id="0357a-122">If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span></span>

<span data-ttu-id="0357a-123">Указание аргумент необязательный **dbRefreshCache** обновляет памяти с последних данных из базы данных.</span><span class="sxs-lookup"><span data-stu-id="0357a-123">Specifying the optional **dbRefreshCache** argument refreshes memory with only the most current data from the database.</span></span>

<span data-ttu-id="0357a-124">Используйте этот метод в средах отдельного пользователя, если не запущено несколько экземпляров приложения не требуется.</span><span class="sxs-lookup"><span data-stu-id="0357a-124">You don't need to use this method in single-user environments unless multiple instances of an application are running.</span></span> <span data-ttu-id="0357a-125">Метод **Idle** может повысить производительность в многопользовательской среде, так как принудительно ядро базы данных для записи данных на диск, освобождения блокировок на память.</span><span class="sxs-lookup"><span data-stu-id="0357a-125">The **Idle** method may increase performance in a multiuser environment because it forces the database engine to write data to disk, releasing locks on memory.</span></span>


> [!NOTE]
> <span data-ttu-id="0357a-126">Можно также запустить блокировки чтения, сделав операции часть транзакции.</span><span class="sxs-lookup"><span data-stu-id="0357a-126">You can also release read locks by making operations part of a transaction.</span></span>

## <a name="example"></a><span data-ttu-id="0357a-127">Пример</span><span class="sxs-lookup"><span data-stu-id="0357a-127">Example</span></span>

<span data-ttu-id="0357a-128">В этом примере используется метод **Idle** , чтобы убедиться, что процедуру вывода обращается к последнему данных, которые доступны из базы данных.</span><span class="sxs-lookup"><span data-stu-id="0357a-128">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database.</span></span> <span data-ttu-id="0357a-129">Процедура IdleOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="0357a-129">The IdleOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub IdleX() 
 
 Dim dbsNorthwind As Database 
 Dim strCountry As String 
 Dim strSQL As String 
 Dim rstOrders As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Get name of country from user and build SQL statement 
 ' with it. 
 strCountry = Trim(InputBox("Enter country:")) 
 strSQL = "SELECT * FROM Orders WHERE ShipCountry = '" & _ 
 strCountry & "' ORDER BY OrderID" 
 
 ' Open Recordset object with SQL statement. 
 Set rstOrders = dbsNorthwind.OpenRecordset(strSQL) 
 
 ' Display contents of Recordset object. 
 IdleOutput rstOrders, strCountry 
 
 rstOrders.Close 
 dbsNorthwind.Close 
 
End Sub 
 
Sub IdleOutput(rstTemp As Recordset, strTemp As String) 
 
 ' Call the Idle method to release unneeded locks, force 
 ' pending writes, and refresh the memory with the current 
 ' data in the .mdb file. 
 DBEngine.Idle dbRefreshCache 
 
 ' Enumerate the Recordset object. 
 With rstTemp 
 Debug.Print "Orders from " & strTemp & ":" 
 Debug.Print , "OrderID", "CustomerID", "OrderDate" 
 Do While Not .EOF 
 Debug.Print , !OrderID, !CustomerID, !OrderDate 
 .MoveNext 
 Loop 
 End With 
 
End Sub 
 
```

