---
title: Блок данных LookupRecord
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 920f0830a310452962eb5dd1c21be63215bf0f03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289793"
---
# <a name="lookuprecord-data-block"></a>Блок данных LookupRecord

**Область применения**: Access 2013, Office 2013

Блок данных **LookupRecord** выполняет набор действий с определенной записью.

> [!NOTE]
> Блок данных **LookupRecord** доступен только в макросах данных.

## <a name="setting"></a>Параметр

Макрокоманда **SetField** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Куда включается</p></td>
<td><p>Да</p></td>
<td><p>Строка, определяющая запись, с которой выполняется работа. Аргумент <em>in</em> может содержать имя таблицы, запрос на выборку или инструкцию SQL.</p><p><strong>Note</strong>: указанная запись не может содержать данные, хранящиеся в связанной таблице или источнике данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Условие отбора</p></td>
<td><p>Нет</p></td>
<td><p>Строковое выражение, используемое для ограничения диапазона данных, в котором выполняется блок данных <strong>LookupRecord</strong> . Например, критерии часто эквивалентны предложению WHERE в выражении SQL, без слова WHERE. Если критерии опущены, блок данных <strong>LookupRecord</strong> работает на всем домене, указанном аргументом <em>in</em> . Все поля, включенные в <em>критерии, также</em>должны быть полями в.</p></td>
</tr>
<tr class="odd">
<td><p>Псевдоним</p></td>
<td><p>Нет</p></td>
<td><p>Строка, предоставляющая альтернативное имя для записи, заданной аргументом <em>in</em> . Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки. Если параметр <em>Alias</em> не указан, имя таблицы или запроса будет использоваться в качестве псевдонима.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если условие, заданное в аргументах *условия* *in* и WHERE, указывает более одной записи, блок данных **LookupRecord** будет работать только с первой записью.

## <a name="example"></a>Пример

В приведенном ниже примере показано, как с помощью действия SetReturnVar вернуть значение из именованного макроса данных. ReturnVar с именем **куррентсервицерекуест** возвращается в макрос или подпрограмму Visual Basic для приложений (VBA), которая вызвала именованный макрос данных.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```

<br/>

В приведенном ниже примере показано, как использовать действие Раисиррор для отмены события перед изменением данных макроса. При обновлении поля AssignedTo используется блок данных LookupRecord, чтобы определить, назначен ли назначенному специалисту открытый запрос на обслуживание. Если этот параметр имеет значение true, событие "до изменения" отменяется и запись не обновляется.

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
