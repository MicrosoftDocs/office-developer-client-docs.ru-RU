---
title: Метод Database.MakeReplica (DAO)
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
ms.openlocfilehash: 45aa005b7c8337a4c5541ea7217cbdb520bb1725
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997737"
---
# <a name="databasemakereplica-method-dao"></a>Метод Database.MakeReplica (DAO)

**Применимо к**: Access 2013, Office 2013

Делает новой реплики из другой реплики базы данных (только для рабочих областей Microsoft Access).

## <a name="syntax"></a>Синтаксис

*выражение* . MakeReplica (***PathName***, ***Описание***, ***Параметры***)

*выражение* Переменная, которая представляет собой объект **базы данных** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Имя пути</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Путь и имя новой реплики. Если реплики существующее имя файла, возникает ошибка.</p></td>
</tr>
<tr class="even">
<td><p><em>Описание</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p><strong>Строка</strong> , описывающая реплики, которую вы создаете</p></td>
</tr>
<tr class="odd">
<td><p><em>Варианты</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Константа <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> , указывающее, характеристики реплики при создании.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Только что созданный реплику будут иметь все **[этого](tabledef-replicafilter-property-dao.md)** свойства, значение **False**, что означает, что данные не будут в таблицах.

## <a name="example"></a>Пример

Эта функция использует метод **MakeReplica** для создания дополнительной реплики из имеющегося образца проекта. Аргумент intOptions может быть сочетание констант **dbRepMakeReadOnly** и **dbRepMakePartial**, или она может иметь значение 0. Например, создание частичная реплика только для чтения, необходимо передать значение **dbRepMakeReadOnly** + **dbRepMakePartial** как значение intOptions.

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

