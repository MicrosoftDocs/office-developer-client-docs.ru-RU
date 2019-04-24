---
title: Метод Database. Макереплика (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294920"
---
# <a name="databasemakereplica-method-dao"></a>Метод Database. Макереплика (DAO)

**Область применения**: Access 2013, Office 2013

Создает новую реплику из другой реплики базы данных (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*Expression* . Макереплика (***путь***, ***Описание***, ***Параметры***)

*выражение*: переменная, представляющая объект **Database**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>PathName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Путь и имя файла новой реплики. Если реплика является именем существующего файла, возникает ошибка.</p></td>
</tr>
<tr class="even">
<td><p><em>Description</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p><strong>Строка</strong> , описывающая создаваемую реплику</p></td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="replicatypeenum-enumeration-dao.md">репликатипинум</a></strong> , определяющая характеристики создаваемой реплики.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Только что созданная частичная реплика будет иметь все свойства **[репликафилтер](tabledef-replicafilter-property-dao.md)** со значением **false**, что означает, что в таблицах не будет данных.

## <a name="example"></a>Пример

Эта функция использует метод **макереплика** для создания дополнительной реплики существующей основной реплики. Аргумент Интоптионс может быть сочетанием констант **дбрепмакереадонли** и **дбрепмакепартиал**, а также может быть равно 0. Например, чтобы создать частичную реплику только для чтения, необходимо передать значение **дбрепмакереадонли** + **дбрепмакепартиал** в качестве значения интоптионс.

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

