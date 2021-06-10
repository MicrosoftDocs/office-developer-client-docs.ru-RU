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

Задает или возвращает относительное рекордное число текущей записи объекта **Recordset2.**

## <a name="syntax"></a>Синтаксис

*expression* .AbsolutePosition

*выражение* Переменная, представляюная объект **Recordset2.**

## <a name="remarks"></a>Примечания

Свойство **AbsolutePosition** можно использовать для расположения текущего указателя записи к определенной записи в зависимости от его расположения в объекте Recordset или типа снимков **Recordset2.** Вы также можете определить текущий номер записи с помощью настройки свойства **AbsolutePosition**.

Так как значение **свойства AbsolutePosition** равно нулю (т. е. параметр 0 относится к первой записи объекта **Recordset2),** нельзя установить его значение, большее или равное количеству населенных записей; это приводит к ошибке, которая может быть заблокирована. Количество населенных записей в объекте **Recordset2** можно определить, проверив параметр **свойства RecordCount.** Максимально допустимое значение для свойства **AbsolutePosition** –значение свойства **RecordCount** минус 1.

Если нет текущей записи, как если в объекте **Recordset2** нет записей, **AbsolutePosition** возвращается —1. При удалении текущей записи, значение свойства **AbsolutePosition** не определяется, а перехватываемая ошибка возникает, если сослаться на него. Новые записи будут добавлены в конец последовательности.

Не следует использовать это свойство в качестве замены номеру записи. Закладки по-прежнему являются рекомендуемой возможностью сохранения и возвращения в заданную позицию и единственным способом расположить текущую запись во всех типах объектов **Recordset2.** В частности положение запись изменяется при удалении одной или нескольких записей, расположенных перед ней. Нет также уверенности в том, что запись будет иметь ту же абсолютную позицию, если объект **Recordset2** будет повторно создан, так как порядок отдельных записей в объекте **Recordset** не гарантируется, если он не создан с помощью SQL с помощью пункта ORDER BY.

> [!NOTE]
> - Настройка свойства **AbsolutePosition** к значению больше нуля для недавно открытого, но незаселенного объекта **Recordset2** приводит к ошибке. Сначала заполнять **объект Recordset2** методом **MoveLast.**
> - Свойство **AbsolutePosition** не доступно для объектов **Recordset2** только для форвардного типа или для объектов **Recordset2,** открытых из сквозных запросов в базах данных базы данных Microsoft Access, подключенных к базе данных ODBC.

## <a name="example"></a>Пример

В этом примере свойство **AbsolutePosition** используется для отслеживания хода цикла, который регистрирует все записи **Recordset2.**

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
