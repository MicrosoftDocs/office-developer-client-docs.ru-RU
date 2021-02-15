---
title: Свойство Recordset2.AbsolutePosition (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: 91ca203f-0c80-67f4-e180-415b6af05030
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197637(v=office.15)
ms:contentKeyID: 48546358
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053074
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4de869866e2aeb28032553be78bee7af16f60402
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307513"
---
# <a name="recordset2absoluteposition-property-dao"></a>Свойство Recordset2.AbsolutePosition (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает относительный номер записи текущей записи объекта **Recordset2.**

## <a name="syntax"></a>Синтаксис

*expression* .AbsolutePosition

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Заметки

Свойство **AbsolutePosition** можно использовать для расположения указателя текущей записи на определенную запись на основе его порядкового положения в объекте **Recordset2** типа dynaset или моментальный снимок. Вы также можете определить текущий номер записи с помощью настройки свойства **AbsolutePosition**.

Так как значение свойства **AbsolutePosition** равно нулю (т. е. значение 0 относится к первой записи в объекте **Recordset2),** вы не можете установить для него значение больше или равное числу заполненных записей; Это приводит к перехитовывуемой ошибке. Вы можете определить количество заполненных записей в **объекте Recordset2,** проверив параметр свойства **RecordCount.** Максимально допустимое значение для свойства **AbsolutePosition** –значение свойства **RecordCount** минус 1.

Если текущей записи нет, как если в объекте **Recordset2** нет записей, **AbsolutePosition** возвращает –1. При удалении текущей записи, значение свойства **AbsolutePosition** не определяется, а перехватываемая ошибка возникает, если сослаться на него. Новые записи будут добавлены в конец последовательности.

Не следует использовать это свойство в качестве замены номеру записи. Закладки по-прежнему являются рекомендуемой возможностью сохранения и возврата в заданную позицию и являются единственным способом позиции текущей записи во всех типах объектов **Recordset2.** В частности положение запись изменяется при удалении одной или нескольких записей, расположенных перед ней. Кроме того, нет уверенности в том, что запись будет иметь одинаковое абсолютное положение, если объект **Recordset2** будет повторно создан, так как порядок отдельных записей в объекте **Recordset** не гарантируется, если она создана с помощью SQL с помощью предложения ORDER BY.

> [!NOTE]
> - Установка **свойству AbsolutePosition** значения больше нуля для только что открытого, но ненастроенного объекта **Recordset2** приводит к перехименовывуемой ошибке. Сначала **заполнять объект Recordset2** с помощью **метода MoveLast.**
> - Свойство **AbsolutePosition** не доступно для объектов **Recordset2** только однонастроенного типа или объектов **Recordset2,** открытых из сквозных запросов к базам данных ODBC, подключенным к ядру базы данных Microsoft Access.

## <a name="example"></a>Пример

В этом примере **свойство AbsolutePosition** используется для отслеживания хода выполнения цикла, который регистрирует все записи **объекта Recordset2.**

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset2 
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
