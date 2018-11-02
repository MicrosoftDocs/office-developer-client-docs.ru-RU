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
ms.openlocfilehash: f1f539659ef81ebb484c4a116176974491b0a480
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931066"
---
# <a name="recordsetlockedits-property-dao"></a>Свойство Recordset.LockEdits (DAO)


**Применимо к**: Access 2013, Office 2013

Задает или возвращает значение, указывающее тип блокировки, который фактически во время редактирования.

## <a name="syntax"></a>Синтаксис

*выражение* . LockEdits

*выражение* Переменная, которая представляет собой объект **набора записей** .

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
<td><p>Значение, используемое по умолчанию. Жесткой блокировки действует. На этой странице содержится запись, которую требуется изменить заблокированный сразу после вызова метода Правка.</p></td>
</tr>
<tr class="even">
<td><p>False</p></td>
<td><p>Оптимистичный блокировки применяется для редактирования. На этой странице содержится запись не блокируется до выполнения метода Update.</p></td>
</tr>
</tbody>
</table>


Свойство **LockEdits** с обновляемым объекты **[набора записей](recordset-object-dao.md)** .

Если страницу заблокирован, другой пользователь не может редактировать записи на той же странице. Если **LockEdits** задать **значение True** , а другой пользователь уже имеет странице блокируется, возникает ошибка при использовании метода **Edit** . Другие пользователи могут читать данные из страниц в заблокированной.

Если **LockEdits** свойству присвоено **значение False** и более поздних версий используйте метод **Update** в процессе странице заблокирован другим пользователем, возникает ошибка. Чтобы просмотреть изменения, внесенные записи другим пользователем, используйте метод **[Move](recordset-move-method-dao.md)** с 0 в качестве аргумента; Тем не менее при этом будут потеряны изменения.

При работе с источниками данных ODBC подключением модуля Microsoft Access базы данных, свойство **LockEdits** всегда имеет значение **False**или оптимистичный блокировки. Ядро СУБД Microsoft Access не контролирует механизмы блокировки, используемые на серверах внешней базе данных.


> [!NOTE]
> <P>Значение <STRONG>LockEdits</STRONG> могут быть предварительно при первом открытии <STRONG>набора записей</STRONG> , задав аргумент lockedits <STRONG><A href="connection-openrecordset-method-dao.md">OpenRecordset</A></STRONG> метода. Установка для аргумента lockedits <STRONG>dbPessimistic</STRONG> будет <STRONG>LockEdits</STRONG> свойству присвоено <STRONG>значение True,</STRONG>и lockedits параметр к любым другим значением будет <STRONG>LockEdits</STRONG> свойству присвоено <STRONG>значение False</STRONG>.</P>



## <a name="example"></a>Пример

В этом примере демонстрируется жесткой блокировки, задав свойство **LockEdits** значение **True**, а затем оптимистичный блокировки, задав свойство **LockEdits** значение False. Также показано, какие виды обработки ошибок необходим в среде многопользовательской базы данных для изменения поля. Функции PessimisticLock и OptimisticLock, необходимые для выполнения этой процедуры.

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
