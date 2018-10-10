---
title: Recordset2.Restartable Property (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3be986fce66342ec736ebfebcfbc3e615ae57a40
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481608"
---
# <a name="recordset2restartable-property-dao"></a><span data-ttu-id="3a04c-102">Recordset2.Restartable Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a04c-102">Recordset2.Restartable Property (DAO)</span></span>


<span data-ttu-id="3a04c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a04c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3a04c-104">Возвращает значение, указывающее, поддерживает ли объект **[набора записей](recordset-object-dao.md)** метод **[повторный запрос](recordset2-requery-method-dao.md)** , который повторно выполняет запрос, на котором основано объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3a04c-104">Returns a value that indicates whether a **[Recordset](recordset-object-dao.md)** object supports the **[Requery](recordset2-requery-method-dao.md)** method, which re-executes the query on which the **Recordset** object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a04c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a04c-105">Syntax</span></span>

<span data-ttu-id="3a04c-106">*выражение* . Перезапускаемое</span><span class="sxs-lookup"><span data-stu-id="3a04c-106">*expression* .Restartable</span></span>

<span data-ttu-id="3a04c-107">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="3a04c-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a04c-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="3a04c-108">Remarks</span></span>

<span data-ttu-id="3a04c-109">Объекты **набора записей** в таблице типа всегда возвращает **значение False**.</span><span class="sxs-lookup"><span data-stu-id="3a04c-109">Table-type **Recordset** objects always return **False**.</span></span>

<span data-ttu-id="3a04c-110">Проверьте свойство **Restartable** перед использованием метода **повторный запрос** на объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3a04c-110">Check the **Restartable** property before using the **Requery** method on a **Recordset** object.</span></span> <span data-ttu-id="3a04c-111">Если свойство **Restartable** имеет значение **False**, используйте метод **[OpenRecordset](connection-openrecordset-method-dao.md)** для базового объекта **[QueryDef](querydef-object-dao.md)** повторное выполнение запроса.</span><span class="sxs-lookup"><span data-stu-id="3a04c-111">If the object's **Restartable** property is set to **False**, use the **[OpenRecordset](connection-openrecordset-method-dao.md)** method on the underlying **[QueryDef](querydef-object-dao.md)** object to re-execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="3a04c-112">Пример</span><span class="sxs-lookup"><span data-stu-id="3a04c-112">Example</span></span>

<span data-ttu-id="3a04c-113">В этом примере демонстрируется свойство **Restartable** с разных объектов **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="3a04c-113">This example demonstrates the **Restartable** property with different **Recordset** objects.</span></span>

```vb
    Sub RestartableX()
    
       Dim dbsNorthwind As Database
       Dim rstTemp As Recordset2
    
       Set dbsNorthwind = OpenDatabase("Northwind.mdb")
    
       With dbsNorthwind
          ' Open a table-type Recordset and print its 
          ' Restartable property.
          Set rstTemp = .OpenRecordset("Employees", dbOpenTable)
          Debug.Print _
             "Table-type recordset from Employees table"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from an SQL statement and print its 
          ' Restartable property.
          Set rstTemp = _
             .OpenRecordset("SELECT * FROM Employees")
          Debug.Print "Recordset based on SQL statement"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          ' Open a Recordset from a saved QueryDef object and 
          ' print its Restartable property.
          Set rstTemp = .OpenRecordset("Current Product List")
          Debug.Print _
             "Recordset based on permanent QueryDef (" & _
             rstTemp.Name & ")"
          Debug.Print "  Restartable = " & rstTemp.Restartable
          rstTemp.Close
    
          .Close
       End With
    
    End Sub
```
