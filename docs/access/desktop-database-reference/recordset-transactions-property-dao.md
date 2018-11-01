---
title: Recordset.Transactions Property (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c3b34f8f027b2e70ada94c6d15584cf25a4aec1c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873294"
---
# <a name="recordsettransactions-property-dao"></a><span data-ttu-id="51889-102">Recordset.Transactions Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="51889-102">Recordset.Transactions Property (DAO)</span></span>


<span data-ttu-id="51889-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51889-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51889-104">Возвращает значение, указывающее, поддерживает ли объект транзакции.</span><span class="sxs-lookup"><span data-stu-id="51889-104">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="51889-105">Только для чтения, **Boolean**.</span><span class="sxs-lookup"><span data-stu-id="51889-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="51889-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51889-106">Syntax</span></span>

<span data-ttu-id="51889-107">*выражение* . Транзакции</span><span class="sxs-lookup"><span data-stu-id="51889-107">*expression* .Transactions</span></span>

<span data-ttu-id="51889-108">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="51889-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="51889-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="51889-109">Remarks</span></span>

<span data-ttu-id="51889-110">В рабочей области Microsoft Access можно также свойство **транзакции** с или таблице добавляющий объекты **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="51889-110">In a Microsoft Access workspace, you can also use the **Transactions** property with dynaset- or table-type **Recordset** objects.</span></span> <span data-ttu-id="51889-111">Моментальный снимок и прямого — только – **[набора записей](recordset-object-dao.md)** объекты типа всегда возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="51889-111">Snapshot- and forward–only–type **[Recordset](recordset-object-dao.md)** objects always return **False**.</span></span>

<span data-ttu-id="51889-112">Если динамический набор - или -таблицей **набора записей** на основании таблица ядра базы данных Microsoft Access, свойство **транзакции** имеет **значение True** , и могут использоваться транзакции.</span><span class="sxs-lookup"><span data-stu-id="51889-112">If a dynaset- or table-type **Recordset** is based on a Microsoft Access database engine table, the **Transactions** property is **True** and you can use transactions.</span></span> <span data-ttu-id="51889-113">Другие модули базы данных могут не поддерживать транзакции.</span><span class="sxs-lookup"><span data-stu-id="51889-113">Other database engines may not support transactions.</span></span> <span data-ttu-id="51889-114">К примеру нельзя использовать транзакции в объект типа динамического **набора записей** , на основе таблицы Paradox.</span><span class="sxs-lookup"><span data-stu-id="51889-114">For example, you can't use transactions in a dynaset-type **Recordset** object based on a Paradox table.</span></span>

<span data-ttu-id="51889-115">Проверьте свойство **транзакций** перед убедитесь в том, что транзакции поддерживаются с помощью метода **[BeginTrans](dbengine-begintrans-method-dao.md)** объекта **[рабочей области для](workspace-object-dao.md)** объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="51889-115">Check the **Transactions** property before using the **[BeginTrans](dbengine-begintrans-method-dao.md)** method on the **Recordset** object's **[Workspace](workspace-object-dao.md)** object to make sure that transactions are supported.</span></span> <span data-ttu-id="51889-116">С помощью методов **BeginTrans**, **CommitTrans**или **отката** неподдерживаемый объект не оказывает влияния.</span><span class="sxs-lookup"><span data-stu-id="51889-116">Using the **BeginTrans**, **CommitTrans**, or **Rollback** methods on an unsupported object has no effect.</span></span>

## <a name="example"></a><span data-ttu-id="51889-117">Пример</span><span class="sxs-lookup"><span data-stu-id="51889-117">Example</span></span>

<span data-ttu-id="51889-118">В этом примере демонстрируется свойство **транзакции** в рабочих областях Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="51889-118">This example demonstrates the **Transactions** property in Microsoft Access workspaces.</span></span>

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

