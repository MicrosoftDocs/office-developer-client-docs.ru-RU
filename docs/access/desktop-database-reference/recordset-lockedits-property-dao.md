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

*выражения* . LockEdits

*expression*: переменная, представляющая объект **Recordset**.

## <a name="remarks"></a>Примечания

Значение параметра или возврата указывает тип блокировки, как указано в следующей таблице.

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
<td><p>True (Истина)</p></td>
<td><p>Значение, используемое по умолчанию. Пессимистическая блокировка действует. Страница, содержащая записи, которые вы редактируете, блокируется сразу же после вызова метода Редактирования.</p></td>
</tr>
<tr class="even">
<td><p>False (Ложь)</p></td>
<td><p>Для редактирования действует оптимистичная блокировка. Страница, содержащая запись, не блокируется до выполнения метода Update.</p></td>
</tr>
</tbody>
</table>


Свойство **LockEdits можно** использовать с помощью updatable **[объектов Recordset.](recordset-object-dao.md)**

Если страница заблокирована, никто другой пользователь не может редактировать записи на той же странице. Если вы установите **LockEdits** для **True** и у другого пользователя уже заблокирована страница, при использовании метода **Редактирования** возникает ошибка. Другие пользователи могут читать данные с заблокированных страниц.

Если вы установите свойство **LockEdits** false, а затем используйте метод **Update,** а другой пользователь заблокировали страницу, возникает ошибка.  Чтобы увидеть изменения, внесенные в запись другим пользователем, используйте метод **[Move](recordset-move-method-dao.md)** с 0 в качестве аргумента; однако, если вы сделаете это, вы потеряете свои изменения.

При работе с источниками данных базы данных Microsoft Access, подключенными к базе данных ODBC, свойство **LockEdits** всегда задает ложную или оптимистичную блокировку. Двигатель базы данных Microsoft Access не контролирует механизмы блокировки, используемые на внешних серверах баз данных.

> [!NOTE]
> Вы можете предустановить значение **LockEdits** при первом открываемом наборе записей, задав аргумент lockedits метода **[OpenRecordset.](connection-openrecordset-method-dao.md)**  Настройка аргумента lockedits для **dbPessimistic** заведет свойство **LockEdits** значение **True,** а параметр lockedits к любому другому значению заведет свойство **LockEdits** значение **False**.

## <a name="example"></a>Пример

В этом примере демонстрируется пессимистическая блокировка, установив свойство **LockEdits** **true,** а затем демонстрирует оптимистичную блокировку, установив свойство **LockEdits** false. В нем также показано, какая обработка ошибок требуется в многоуровневой среде базы данных для изменения поля. Для запуска этой процедуры необходимы функции PessimisticLock и OptimisticLock.

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
