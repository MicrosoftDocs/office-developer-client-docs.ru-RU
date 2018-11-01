---
title: Recordset2.AbsolutePosition Property (DAO)
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
ms.openlocfilehash: c5eb8c80743b5fac17f7a3c8d11080863e511eb8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888603"
---
# <a name="recordset2absoluteposition-property-dao"></a>Recordset2.AbsolutePosition Property (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает относительный номер записи текущего объекта **Recordset2** .

## <a name="syntax"></a>Синтаксис

*выражение* . AbsolutePosition

*выражение* Переменная, которая представляет собой объект- **Recordset2** .

## <a name="remarks"></a>Замечания

Свойство **AbsolutePosition** наведите указатель текущей записи на основании его порядковый номер в объект **Recordset2** добавляющий или моментальный снимок определенную запись. Также можно определить текущий номер записи, проверив значение свойства **AbsolutePosition** .

Так как значение свойства **AbsolutePosition** с отсчетом от нуля (то есть, значение 0 относится к первой записи в объекте **Recordset2** ), вы не может задать значение больше или равно числу заполненной записей; Благодаря этому перехватываемые ошибки. Можно определить число заполненной записей в объекте **Recordset2** , проверьте настройки свойства **RecordCount** . Максимальное допустимое свойство **AbsolutePosition** — значение свойства **RecordCount** минус 1.

Если нет текущей записи как при нет записей в объекте **Recordset2** , **AbsolutePosition** возвращает значение – 1. При удалении текущей записи, значение свойства **AbsolutePosition** не определена и перехватываемые ошибка возникает, если ссылки на него. Новые записи добавляются в конец последовательности.

Это свойство не следует использовать как номер записи заменяющего. Закладки будут по-прежнему рекомендуемый способ сохранения и возврата в заданной позиции и являются единственным способом для размещения текущей записи для всех типов объектов **Recordset2** . В частности при удалении одной или нескольких записей, перед изменение положения записи. Нет также никакой гарантий, что запись будет же абсолютного положения, если повторно объект **Recordset2** создается еще раз, так как порядок отдельных записей в объекте **набора записей** не гарантируется, если он создается с помощью SQL оператор с помощью предложение ORDER BY.


> [!NOTE]
> <UL>
> <LI>
> <P>Для свойства <STRONG>AbsolutePosition</STRONG> значение значение больше нуля в объекте <STRONG>Recordset2</STRONG> недавно открытых, но пустые возникает перехватываемые ошибки. Объект <STRONG>Recordset2</STRONG> сначала заполняется с помощью метода <STRONG>MoveLast</STRONG> .</P>
> <LI>
> <P>Свойство <STRONG>AbsolutePosition</STRONG> недоступно <STRONG>Recordset2</STRONG> прямого — только — тип объектов или объектов <STRONG>Recordset2</STRONG> открывается из Транзитные запросы к базам данных ODBC engine подключенной базы данных Microsoft Access.</P></LI></UL>



## <a name="example"></a>Пример

В этом примере используется свойство **AbsolutePosition** для отслеживания хода выполнения цикла, который перечисляет все записи **Recordset2**.

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
