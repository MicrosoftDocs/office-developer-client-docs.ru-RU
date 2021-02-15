---
title: Свойство Recordset.LockEdits (DAO)
TOCTitle: LockEdits Property
ms:assetid: baa11b24-a330-eaa4-bd03-b8b9739d209e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822514(v=office.15)
ms:contentKeyID: 48547379
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052877
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 54f91dea98f4f47057eb673a0fae08c8ac2b6f1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300464"
---
# <a name="recordsetlockedits-property-dao"></a>Свойство Recordset.LockEdits (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, определяющее тип блокировки, которая действует во время редактирования.

## <a name="syntax"></a>Синтаксис

*выражение .* LockEdits

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Параметр или возвращаемого значения указывает тип блокировки, как указано в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Верно</p></td>
<td><p>Значение, используемое по умолчанию. Действует пессимистическая блокировка. Страница, содержащая редактируемую запись, блокируется сразу же после вызова метода Edit.</p></td>
</tr>
<tr class="even">
<td><p>Неверно</p></td>
<td><p>Оптимистичная блокировка действует для редактирования. Страница, содержащая запись, не блокируется, пока не будет выполнен метод Update.</p></td>
</tr>
</tbody>
</table>


Вы можете использовать свойство **LockEdits** с объектами updatable **[Recordset.](recordset-object-dao.md)**

Если страница заблокирована, другие пользователи не смогут редактировать записи на той же странице. Если для **LockEdits** установлено true, а страница другого пользователя уже заблокирована, при использовании метода **Edit** возникает ошибка.  Другие пользователи могут читать данные со заблокированных страниц.

Если для свойства **LockEdits** установлено имя **False,** а затем вы используете метод **Update,** когда страница другого пользователя заблокирована, возникает ошибка. Чтобы увидеть изменения, внесенные в вашу запись другим пользователем, используйте метод **[Move](recordset-move-method-dao.md)** с 0 в качестве аргумента; однако если вы сделаете это, вы потеряете изменения.

При работе с источниками данных ODBC, подключенными к яду баз данных Microsoft Access, свойство **LockEdits** всегда имеет свойство **False** или оптимистичную блокировку. Механизм баз данных Microsoft Access не управляет механизмами блокировки, используемыми на внешних серверах баз данных.

> [!NOTE]
> Вы можете предварительно установить значение **LockEdits** при первом открыть набор **записей,** задав аргумент lockedits метода **[OpenRecordset.](connection-openrecordset-method-dao.md)** Если для аргумента lockedits установлено значение **dbPessimistic,** для свойства **LockEdits** будет установлено значение **True,** а для параметра lockedits любое другое значение **будет** установлено значение **False.**

## <a name="example"></a>Пример

В этом примере демонстрируется пессимистическая блокировка путем установки для свойства **LockEdits** свойства **True,** а затем демонстрируется оптимистическая блокировка путем установки для свойства **LockEdits** свойства False. В нем также показано, какой тип обработки ошибок требуется в многомерной среде базы данных для изменения поля. Для запуска этой процедуры необходимы функции "Пессимистическийlock" и "Оптимистичныйlock".

```vb
    Sub LockEditsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstCustomers As Recordset 
     Dim strOldName As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstCustomers = _ 
     dbsNorthwind.OpenRecordset("Customers", _ 
     dbOpenDynaset) 
     
     With rstCustomers 
     ' Store original data. 
     strOldName = !CompanyName 
     
     If MsgBox("Pessimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with pessimistic locking 
     ' in effect. 
     If PessimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     If MsgBox("Optimistic locking demonstration...", _ 
     vbOKCancel) = vbOK Then 
     
     ' Attempt to modify data with optimistic locking 
     ' in effect. 
     If OptimisticLock(rstCustomers, !CompanyName, _ 
     "Acme Foods") Then 
     MsgBox "Record successfully edited." 
     
     ' Restore original data... 
     .Edit 
     !CompanyName = strOldName 
     .Update 
     End If 
     
     End If 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function PessimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     PessimisticLock = True 
     
     With rstTemp 
     .LockEdits = True 
     
     ' When you set LockEdits to True, you trap for errors 
     ' when you call the Edit method. 
     On Error GoTo Err_Lock 
     .Edit 
     On Error GoTo 0 
     
     ' If the Edit is still in progress, then no errors 
     ' were triggered; you may modify the data. 
     If .EditMode = dbEditInProgress Then 
     fldTemp = strNew 
     .Update 
     .Bookmark = .LastModified 
     Else 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     PessimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function 
     
    Function OptimisticLock(rstTemp As Recordset, _ 
     fldTemp As Field, strNew As String) As Boolean 
     
     dim ErrLoop as Error 
     
     OptimisticLock = True 
     
     With rstTemp 
     .LockEdits = False 
     .Edit 
     fldTemp = strNew 
     
     ' When you set LockEdits to False, you trap for errors 
     ' when you call the Update method. 
     On Error GoTo Err_Lock 
     .Update 
     On Error GoTo 0 
     
     ' If there is no Edit in progress, then no errors were 
     ' triggered; you may modify the data. 
     If .EditMode = dbEditNone Then 
     ' Move current record pointer to the most recently 
     ' modified record. 
     .Bookmark = .LastModified 
     Else 
     .CancelUpdate 
     ' Retrieve current record to see changes made by 
     ' other user. 
     .Move 0 
     End If 
     
     End With 
     
     Exit Function 
     
    Err_Lock: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     OptimisticLock = False 
     End If 
     
     Resume Next 
     
    End Function
```
