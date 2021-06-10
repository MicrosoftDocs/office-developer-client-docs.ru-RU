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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294332"
---
# <a name="dbengineidle-method-dao"></a><span data-ttu-id="4f9eb-102">Метод DBEngine.Idle (DAO)</span><span class="sxs-lookup"><span data-stu-id="4f9eb-102">DBEngine.Idle method (DAO)</span></span>

<span data-ttu-id="4f9eb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f9eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4f9eb-104">Приостанавливать обработку данных, позволяя движку базы данных Microsoft Access выполнять любые ожидающие задачи, такие как оптимизация памяти или время ожидания страниц (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4f9eb-104">Suspends data processing, enabling the Microsoft Access database engine to complete any pending tasks, such as memory optimization or page timeouts (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f9eb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f9eb-105">Syntax</span></span>

<span data-ttu-id="4f9eb-106">*выражения* . Idle ***(Action)***</span><span class="sxs-lookup"><span data-stu-id="4f9eb-106">*expression* .Idle(***Action***)</span></span>

<span data-ttu-id="4f9eb-107">*expression*: переменная, представляющая объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f9eb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f9eb-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4f9eb-109">Имя</span><span class="sxs-lookup"><span data-stu-id="4f9eb-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4f9eb-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="4f9eb-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4f9eb-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4f9eb-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4f9eb-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4f9eb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4f9eb-113"><em>Action</em></span><span class="sxs-lookup"><span data-stu-id="4f9eb-113"><em>Action</em></span></span></p></td>
<td><p><span data-ttu-id="4f9eb-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4f9eb-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="4f9eb-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4f9eb-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4f9eb-116">Указывает действие, необходимое для принятия.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-116">Specifies the action to take.</span></span> <span data-ttu-id="4f9eb-117">Может быть одной из <strong><a href="idleenum-enumeration-dao.md">констант IdleEnum.</a></strong></span><span class="sxs-lookup"><span data-stu-id="4f9eb-117">Can be one of the <strong><a href="idleenum-enumeration-dao.md">IdleEnum</a></strong> constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4f9eb-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="4f9eb-118">Remarks</span></span>

<span data-ttu-id="4f9eb-119">Метод **Idle** позволяет механизму базы данных Microsoft Access выполнять фоновые задачи, которые могут быть не в курсе из-за интенсивной обработки данных.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-119">The **Idle** method allows the Microsoft Access database engine to perform background tasks that may not be up-to-date because of intense data processing.</span></span> <span data-ttu-id="4f9eb-120">Это часто верно в многоядерных многозадачных средах, где не хватает времени фоновой обработки, чтобы сохранить все записи в течение **[Recordset.](recordset-object-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="4f9eb-120">This is often true in multiuser, multitasking environments that don't have enough background processing time to keep all records in a **[Recordset](recordset-object-dao.md)** current.</span></span>

<span data-ttu-id="4f9eb-121">Обычно блоки чтения удаляются, а данные в локальных объектах **recordset** типа dynaset обновляются только в том случае, если не происходит никаких других действий (в том числе движений мыши).</span><span class="sxs-lookup"><span data-stu-id="4f9eb-121">Usually, read locks are removed and data in local dynaset-type **Recordset** objects are updated only when no other actions (including mouse movements) occur.</span></span> <span data-ttu-id="4f9eb-122">Если вы периодически используете метод **Idle,** то двигатель базы данных Microsoft Access может догнать задачи обработки фона, выпустив нежелательные блокировки чтения.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-122">If you periodically use the **Idle** method, the Microsoft Access database engine can catch up on background processing tasks by releasing unneeded read locks.</span></span>

<span data-ttu-id="4f9eb-123">Указание необязательного **аргумента dbRefreshCache** обновляет память только с самыми актуальными данными из базы данных.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-123">Specifying the optional **dbRefreshCache** argument refreshes memory with only the most current data from the database.</span></span>

<span data-ttu-id="4f9eb-124">Этот метод не требуется использовать в средах с одним пользователем, если не запущено несколько экземпляров приложения.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-124">You don't need to use this method in single-user environments unless multiple instances of an application are running.</span></span> <span data-ttu-id="4f9eb-125">Метод **Idle** может повысить производительность в многоуровневой среде, так как заставляет двигатель базы данных записывать данные на диск, выпуская блокировки в памяти.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-125">The **Idle** method may increase performance in a multiuser environment because it forces the database engine to write data to disk, releasing locks on memory.</span></span>


> [!NOTE]
> <span data-ttu-id="4f9eb-126">Кроме того, можно освободить блокировки чтения, сделав операции частью транзакции.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-126">You can also release read locks by making operations part of a transaction.</span></span>

## <a name="example"></a><span data-ttu-id="4f9eb-127">Пример</span><span class="sxs-lookup"><span data-stu-id="4f9eb-127">Example</span></span>

<span data-ttu-id="4f9eb-128">В этом примере метод **Idle** используется для обеспечения доступа к самым актуальным данным из базы данных.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-128">This example uses the **Idle** method to ensure that an output procedure is accessing the most current data available from the database.</span></span> <span data-ttu-id="4f9eb-129">Процедура IdleOutput необходима для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="4f9eb-129">The IdleOutput procedure is required for this procedure to run.</span></span>

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

