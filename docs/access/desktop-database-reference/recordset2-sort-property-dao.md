---
title: Свойство Recordset2.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309271"
---
# <a name="recordset2sort-property-dao"></a>Свойство Recordset2.Sort (DAO)

**Область применения**: Access 2013, Office 2013 

Задает или возвращает порядок сортировки для записей в объекте **[Recordset](recordset-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*expression* .Sort

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Комментарии

Вы можете использовать свойство **Sort** с объектами **Recordset** типа dynaset и моментальный снимок.

Если вы задаете это свойство для объекта, сортировка будет выполнена при создании последующего объекта **Recordset** из данного объекта. Настройка свойства **Sort** будет переопределять любой порядок сортировки, указанный для объекта **[QueryDef](querydef-object-dao.md)**.

Стандартный порядок сортировки по возрастанию (от А до Я или от 0 до 100).

Свойство **Sort** не оказывает влияние на объекты **Recordset** табличного или однонаправленного типа. Чтобы отсортировать табличный тип объекта **Recordset** используйте свойство **[Index](recordset2-index-property-dao.md)**.

> [!NOTE]
> Во многих случаях быстрее будет открыть новый объект **Recordset** с помощью оператора SQL, который включает условия сортировки.

## <a name="example"></a>Пример

В этом примере показано свойство **Sort**, изменение его значения, а также создание нового объекта **Recordset**. Функция SortOutput обязательна для запуска этой процедуры.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

Если вы знаете данные, которые вы хотите выбрать, как правило, более рационально будет создать **Recordset** с оператором SQL. В этом примере показано, как можно создать только один объект **Recordset** и получить те же результаты, что и в предыдущем примере.

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
