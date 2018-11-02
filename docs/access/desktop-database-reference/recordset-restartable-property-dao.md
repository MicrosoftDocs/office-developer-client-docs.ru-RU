---
title: Свойство Recordset.Restartable (DAO)
TOCTitle: Restartable Property
ms:assetid: 00def49d-ea7e-6cd5-2f4a-914a1ddcdd51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844737(v=office.15)
ms:contentKeyID: 48542919
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052926
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 26d9d215c35e9a768a663d41ecc40f49bee4dfdb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920860"
---
# <a name="recordsetrestartable-property-dao"></a><span data-ttu-id="ec642-102">Свойство Recordset.Restartable (DAO)</span><span class="sxs-lookup"><span data-stu-id="ec642-102">Recordset.Restartable property (DAO)</span></span>


<span data-ttu-id="ec642-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec642-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec642-104">Возвращает значение, указывающее, поддерживает ли объект **[набора записей](recordset-object-dao.md)** метод **[повторный запрос](recordset-requery-method-dao.md)** , который повторно выполняет запрос, на котором основано объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec642-104">Returns a value that indicates whether a **[Recordset](recordset-object-dao.md)** object supports the **[Requery](recordset-requery-method-dao.md)** method, which re-executes the query on which the **Recordset** object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec642-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec642-105">Syntax</span></span>

<span data-ttu-id="ec642-106">*выражение* . Перезапускаемое</span><span class="sxs-lookup"><span data-stu-id="ec642-106">*expression* .Restartable</span></span>

<span data-ttu-id="ec642-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec642-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec642-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="ec642-108">Remarks</span></span>

<span data-ttu-id="ec642-109">Объекты **набора записей** в таблице типа всегда возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="ec642-109">Table-type **Recordset** objects always return **False**.</span></span>

<span data-ttu-id="ec642-110">Проверьте свойство **Restartable** перед использованием метода **повторный запрос** на объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec642-110">Check the **Restartable** property before using the **Requery** method on a **Recordset** object.</span></span> <span data-ttu-id="ec642-111">Если свойство **Restartable** имеет значение **False**, используйте метод **[OpenRecordset](connection-openrecordset-method-dao.md)** для базового объекта **[QueryDef](querydef-object-dao.md)** повторное выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="ec642-111">If the object's **Restartable** property is set to **False**, use the **[OpenRecordset](connection-openrecordset-method-dao.md)** method on the underlying **[QueryDef](querydef-object-dao.md)** object to re-execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="ec642-112">Пример</span><span class="sxs-lookup"><span data-stu-id="ec642-112">Example</span></span>

<span data-ttu-id="ec642-113">В этом примере демонстрируется свойство **Restartable** с разных объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="ec642-113">This example demonstrates the **Restartable** property with different **Recordset** objects.</span></span>

```vb
    Sub RestartableX() 
     
     Dim dbsNorthwind As Database 
     Dim rstTemp As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open a table-type Recordset and print its 
     ' Restartable property. 
     Set rstTemp = .OpenRecordset("Employees", dbOpenTable) 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from an SQL statement and print its 
     ' Restartable property. 
     Set rstTemp = _ 
     .OpenRecordset("SELECT * FROM Employees") 
     Debug.Print "Recordset based on SQL statement" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     ' Open a Recordset from a saved QueryDef object and 
     ' print its Restartable property. 
     Set rstTemp = .OpenRecordset("Current Product List") 
     Debug.Print _ 
     "Recordset based on permanent QueryDef (" & _ 
     rstTemp.Name & ")" 
     Debug.Print " Restartable = " & rstTemp.Restartable 
     rstTemp.Close 
     
     .Close 
     End With 
     
    End Sub
```
