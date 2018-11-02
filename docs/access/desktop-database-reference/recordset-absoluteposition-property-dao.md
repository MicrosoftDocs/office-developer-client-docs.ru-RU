---
title: Свойство Recordset.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bd214058b0b478c45b719798dc0b858bfd29b43
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928105"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Свойство Recordset.AbsolutePosition (DAO)

**Применимо к**: Access 2013, Office 2013

Задает или возвращает относительный номер записи текущего объекта **набора записей** .

## <a name="syntax"></a>Синтаксис

*выражение* . AbsolutePosition

*выражение* Переменная, которая представляет собой объект **набора записей** .

## <a name="remarks"></a>Примечания

Свойство **AbsolutePosition** наведите указатель текущей записи для конкретных записей по его порядковый номер в объект **набора записей** добавляющий или моментальный снимок. Также можно определить текущий номер записи, проверив значение свойства **AbsolutePosition** .

Так как значение свойства **AbsolutePosition** с отсчетом от нуля (то есть, значение 0 относится к первой записи в объекте **набора записей** ), вы не может задать значение больше или равно числу заполненной записей; Благодаря этому перехватываемые ошибки. Можно определить число заполненной записей в объекте **набора записей** , проверьте настройки свойства **RecordCount** . Максимальное допустимое свойство **AbsolutePosition** — значение свойства **RecordCount** минус 1.

Если нет текущей записи как при нет записей в объекте **набора записей** , **AbsolutePosition** возвращает значение – 1. При удалении текущей записи, значение свойства **AbsolutePosition** не определена и перехватываемые ошибка возникает, если ссылки на него. Новые записи добавляются в конец последовательности.

Это свойство не следует использовать как номер записи заменяющего. Закладки будут по-прежнему рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом для размещения текущей записи для всех типов объектов **наборов записей** . В частности при удалении одной или нескольких записей, перед изменение положения записи. Нет также никакой гарантий, что запись будет же абсолютного положения, если повторно объекта **набора записей** создается еще раз, так как порядок отдельных записей в объекте **набора записей** не гарантируется, если он создается с помощью инструкции SQL с помощью предложение ORDER BY.

> [!NOTE]
> - Для свойства **AbsolutePosition** значение значение больше нуля на вновь открыт, но пустые объекта **набора записей** происходит перехватываемые ошибки. Сначала заполнения объекта **набора записей** с помощью метода **MoveLast** .
> - Свойство **AbsolutePosition** недоступно прямого — только — тип объектов **наборов записей** , либо на объекты **набора записей** из Транзитные запросы к базам данных ODBC engine подключенной базы данных Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется свойство **AbsolutePosition** для отслеживания хода выполнения цикла, который перечисляет все записи из **набора записей**.

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
