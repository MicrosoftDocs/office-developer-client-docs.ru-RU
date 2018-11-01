---
title: Recordset.Sort Property (DAO)
TOCTitle: Sort Property
ms:assetid: 9be9bf62-f713-537e-4df0-3a54d485a523
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198077(v=office.15)
ms:contentKeyID: 48546582
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053063
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cdf82bac92b06d0dc4fb251278e3d6226405439b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873210"
---
# <a name="recordsetsort-property-dao"></a>Recordset.Sort Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает порядок сортировки для записей в объекте **[набора записей](recordset-object-dao.md)** (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . Сортировка

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Замечания

Можно использовать свойство **сортировки** с динамический набор – и моментальный снимок — тип объектов **наборов записей** .

Если значение этого свойства для объекта, сортировка происходит при последующих объекта **набора записей** из этого объекта. Свойство **сортировки** переопределяет любой порядок сортировки, указанный для объекта **[QueryDef](querydef-object-dao.md)** .

Порядок сортировки по возрастанию (A-Z или 0 до 100).

Свойство **сортировки** не применяется к таблице – прямого – только для – тип или объектов **наборов записей** . Чтобы отсортировать объекта **набора записей** в таблице — тип, используйте свойство **[индекса](recordset-index-property-dao.md)** .


> [!NOTE]
> <P>Во многих случаях это быстрее, чтобы открыть новый объект <STRONG>набора записей</STRONG> с помощью инструкции SQL, которая включает в себя критерия сортировки.</P>



## <a name="example"></a>Пример

В этом примере демонстрируется свойство **сортировки** , изменив его значение и создание нового **набора записей**. Функция SortOutput является обязательным для выполнения этой процедуры.

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstSortEmployees As Recordset 
     
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

Если вы знаете данных, которые нужно выбрать, обычно более эффективно создание **набора записей** с помощью инструкции SQL. В этом примере показано, как можно создать только один **набор записей** и получить те же результаты, как показано в предыдущем примере.

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
