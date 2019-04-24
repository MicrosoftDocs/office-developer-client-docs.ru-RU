---
title: Свойство Recordset. LockEdits (DAO)
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
# <a name="recordsetlockedits-property-dao"></a>Свойство Recordset. LockEdits (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, определяющее тип блокировки, которая действует во время редактирования.

## <a name="syntax"></a>Синтаксис

*Expression* . LockEdits

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Параметр или возвращаемое значение указывает тип блокировки, как указано в следующей таблице.

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
<td><p>True</p></td>
<td><p>Значение, используемое по умолчанию. Применяется Пессимистическая блокировка. Страница, содержащая редактируемую запись, блокируется сразу после вызова метода Edit.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>Для редактирования применяется Оптимистическая блокировка. Страница, содержащая запись, не блокируется до тех пор, пока не будет выполнен метод Update.</p></td>
</tr>
</tbody>
</table>


Можно использовать свойство **LockEdits** с обновляемыми объектами **[Recordset](recordset-object-dao.md)** .

Если страница заблокирована, другие пользователи не могут изменять записи на той же странице. Если для **LockEdits** задано **значение true** , а у другого пользователя уже есть страница заблокирована, то при использовании метода **Edit** возникает ошибка. Другие пользователи могут считывать данные из заблокированных страниц.

Если для свойства **LockEdits** задано **значение false** , а в дальнейшем используется метод **Update** , а страница заблокирована другим пользователем, возникает ошибка. Чтобы просмотреть изменения, внесенные в запись другим пользователем, используйте метод **[Move](recordset-move-method-dao.md)** с 0 в качестве аргумента; Тем не менее, если вы сделаете это, изменения будут потеряны.

При работе с источниками данных ODBC, подключенными к ядру СУБД Microsoft Access, свойство **LockEdits** всегда имеет значение **false**или Оптимистическая блокировка. Ядро СУБД Microsoft Access не контролирует механизмы блокировки, используемые на внешних серверах баз данных.

> [!NOTE]
> Вы можете предварительно установить значение **LockEdits** при первом открытии объекта **Recordset** , задав аргумент LockEdits метода **[OpenRecordset](connection-openrecordset-method-dao.md)** . Если задать для аргумента LockEdits значение **дбпессимистик** , свойству **LockEdits** будет присвоено **значение true**, а для свойства **LockEdits** будет задано значение **false**.

## <a name="example"></a>Пример

В этом примере показана Пессимистическая блокировка путем установки свойства **LockEdits** в **значение true**, а затем демонстрируется Оптимистическая блокировка путем установки свойства **LockEdits** в значение false. Здесь также показано, какой тип обработки ошибок необходим в многопользовательской среде базы данных для изменения поля. Для выполнения этой процедуры необходимы функции Пессимистиклокк и Оптимистиклокк.

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
