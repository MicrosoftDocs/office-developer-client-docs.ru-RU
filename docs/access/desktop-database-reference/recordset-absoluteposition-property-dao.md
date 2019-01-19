---
title: Свойство Recordset.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 22284abf537f57d98d5f0416b58a9a2ac3c6ebe5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702506"
---
# <a name="recordsetabsoluteposition-property-dao"></a>Свойство Recordset.AbsolutePosition (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает относительный номер записи объекта **Recordset** текущей записи.

## <a name="syntax"></a>Синтаксис

*expression* .AbsolutePosition

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Комментарии

Вы можете использовать свойство **AbsolutePosition**, чтобы расположить указатель текущей записи на определенной записи с учетом его порядкового положения в объекте **Recordset** типа dynaset или моментальный снимок. Вы также можете определить текущий номер записи с помощью настройки свойства **AbsolutePosition**.

Так как значение свойства **AbsolutePosition** опирается на ноль (то есть установка значения 0 указывает на первую запись объекта **Recordset**), вы не можете установить значение, которые больше или равно количеству заполненных записей, так как это вызывает перехватываемую ошибку. Вы можете определить количество заполненных записей в объекте **Recordset** путем проверки настройки свойства **RecordCount**. Максимально допустимое значение для свойства **AbsolutePosition** –значение свойства **RecordCount** минус 1.

При отсутствии текущей записи, например, когда в объекте **Recordset** нет записей, **AbsolutePosition** возвращает -1. При удалении текущей записи, значение свойства **AbsolutePosition** не определяется, а перехватываемая ошибка возникает, если сослаться на него. Новые записи будут добавлены в конец последовательности.

Не следует использовать это свойство в качестве замены номеру записи. Закладки по-прежнему являются рекомендуемым методом сохранения и возврата к заданному положению и — единственным способом расположения текущей записи для всех типов объектов **Recordset**. В частности положение запись изменяется при удалении одной или нескольких записей, расположенных перед ней. Кроме того, нет гарантий, что запись будет иметь такое же абсолютное положение, если объект **Recordset** будет создан повторно, так как порядок отдельных записей в пределах объекта **Recordset** не гарантируется, если он не создан с помощью оператора SQL, который включает в себя предложение ORDER BY.

> [!NOTE]
> - Настройка свойства **AbsolutePosition** со значением больше нуля для только что открытого, но не заполненного объекта **Recordset** вызывает перехватываемую ошибку. Сначала заполните объект **Recordset** с помощью метода **MoveLast**.
> - Свойство **AbsolutePosition** не поддерживается для объекта **Recordset** однонаправленного типа или для объектов **Recordset**, открытых через запрос к серверу для базы данных ODBC, подключенной к ядру СУБД Microsoft Access.

## <a name="example"></a>Пример

В этом примере используется свойство **AbsolutePosition** для отслеживания хода выполнения цикла, который перечисляет все записи в **Recordset**.

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
