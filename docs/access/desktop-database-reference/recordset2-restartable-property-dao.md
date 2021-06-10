---
title: Свойство Recordset2.Restartable (DAO)
TOCTitle: Restartable Property
ms:assetid: 9b1c40f8-5a33-2527-a7b6-bef4cb991d7e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198019(v=office.15)
ms:contentKeyID: 48546560
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 873911ff8475a0b37f3f67d9cb2c01afc577487d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309092"
---
# <a name="recordset2restartable-property-dao"></a><span data-ttu-id="c4722-102">Свойство Recordset2.Restartable (DAO)</span><span class="sxs-lookup"><span data-stu-id="c4722-102">Recordset2.Restartable property (DAO)</span></span>


<span data-ttu-id="c4722-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4722-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4722-104">Возвращает значение, которое указывает на то, поддерживает ли объект **[Recordset](recordset-object-dao.md)** метод **[Requery](recordset2-requery-method-dao.md)**, который повторно выполняет запрос, на котором основан объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c4722-104">Returns a value that indicates whether a **[Recordset](recordset-object-dao.md)** object supports the **[Requery](recordset2-requery-method-dao.md)** method, which re-executes the query on which the **Recordset** object is based.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4722-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c4722-105">Syntax</span></span>

<span data-ttu-id="c4722-106">*выражения* . Перезапуск</span><span class="sxs-lookup"><span data-stu-id="c4722-106">*expression* .Restartable</span></span>

<span data-ttu-id="c4722-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="c4722-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4722-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="c4722-108">Remarks</span></span>

<span data-ttu-id="c4722-109">Объекты **Recordset типа таблицы** всегда возвращают **False.**</span><span class="sxs-lookup"><span data-stu-id="c4722-109">Table-type **Recordset** objects always return **False**.</span></span>

<span data-ttu-id="c4722-110">Проверьте свойство **Restartable** перед использованием метода **Requery** на **объекте Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c4722-110">Check the **Restartable** property before using the **Requery** method on a **Recordset** object.</span></span> <span data-ttu-id="c4722-111">Если свойство перезапуска объекта настроено на **False,** используйте метод **[OpenRecordset](connection-openrecordset-method-dao.md)** на основном объекте **[QueryDef](querydef-object-dao.md)** для повторного выполнения запроса. </span><span class="sxs-lookup"><span data-stu-id="c4722-111">If the object's **Restartable** property is set to **False**, use the **[OpenRecordset](connection-openrecordset-method-dao.md)** method on the underlying **[QueryDef](querydef-object-dao.md)** object to re-execute the query.</span></span>

## <a name="example"></a><span data-ttu-id="c4722-112">Пример</span><span class="sxs-lookup"><span data-stu-id="c4722-112">Example</span></span>

<span data-ttu-id="c4722-113">В этом примере демонстрируется свойство **Restartable** с различными **объектами Recordset.**</span><span class="sxs-lookup"><span data-stu-id="c4722-113">This example demonstrates the **Restartable** property with different **Recordset** objects.</span></span>

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
