---
title: Свойство Recordset2. Transactions (DAO)
TOCTitle: Transactions Property
ms:assetid: f2169565-f782-4089-0e4b-bc5d58d37db5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836614(v=office.15)
ms:contentKeyID: 48548642
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 58610ee87e61a8b342955107c2ba2b690e610c8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309244"
---
# <a name="recordset2transactions-property-dao"></a><span data-ttu-id="5a24b-102">Свойство Recordset2. Transactions (DAO)</span><span class="sxs-lookup"><span data-stu-id="5a24b-102">Recordset2.Transactions property (DAO)</span></span>


<span data-ttu-id="5a24b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5a24b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5a24b-104">Возвращает значение, которое указывает на то, поддерживает ли объект транзакций.</span><span class="sxs-lookup"><span data-stu-id="5a24b-104">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="5a24b-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="5a24b-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a24b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a24b-106">Syntax</span></span>

<span data-ttu-id="5a24b-107">*Expression* . Транзакций</span><span class="sxs-lookup"><span data-stu-id="5a24b-107">*expression* .Transactions</span></span>

<span data-ttu-id="5a24b-108">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="5a24b-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a24b-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="5a24b-109">Remarks</span></span>

<span data-ttu-id="5a24b-110">В рабочей области Microsoft Access можно также использовать свойство **Transactions** с объектами **Recordset** типа динамического подмножества или таблицы.</span><span class="sxs-lookup"><span data-stu-id="5a24b-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="5a24b-111">Объекты **[Recordset](recordset-object-dao.md)** для типа моментального снимка и прямого прямого доступа — всегда возвращают **значение false**.</span><span class="sxs-lookup"><span data-stu-id="5a24b-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="5a24b-112">Если **набор записей** динамического типа или табличного типа основан на таблице ядра СУБД Microsoft Access, свойство **Transactions** имеет **значение true** , и вы можете использовать транзакции.</span><span class="sxs-lookup"><span data-stu-id="5a24b-112">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions.</span></span> <span data-ttu-id="5a24b-113">Другие ядра СУБД могут не поддерживать транзакции.</span><span class="sxs-lookup"><span data-stu-id="5a24b-113">Other database engines may not support transactions.</span></span> <span data-ttu-id="5a24b-114">Например, нельзя использовать транзакции в объекте **Recordset** типа динамического подмножества на основе таблицы Paradox.</span><span class="sxs-lookup"><span data-stu-id="5a24b-114">For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="5a24b-115">Проверьте свойство **Transactions** перед использованием метода **[BeginTrans](dbengine-begintrans-method-dao.md)** объекта **Recordset** объекта **[Workspace](workspace-object-dao.md)** , чтобы убедиться в том, что транзакции поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="5a24b-115">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported.</span></span> <span data-ttu-id="5a24b-116">Использование методов **BeginTrans**, **CommitTrans**и **ROLLBACK** для неподдерживаемого объекта не оказывает никакого действия.</span><span class="sxs-lookup"><span data-stu-id="5a24b-116">Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="5a24b-117">Пример</span><span class="sxs-lookup"><span data-stu-id="5a24b-117">Example</span></span>

<span data-ttu-id="5a24b-118">В этом примере показано свойство **Transactions** в рабочей области Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5a24b-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

