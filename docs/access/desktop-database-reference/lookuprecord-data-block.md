---
title: LookupRecord Data Block
TOCTitle: LookupRecord Data Block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dd0db6e818ab79fc124760509d07d60b954d49e5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481852"
---
# <a name="lookuprecord-data-block"></a>LookupRecord Data Block

**Применимо к**: Access 2013 | Office 2013

Блок данных **макрокомандой НайтиЗапись, после** выполняет набор действий в конкретной записи.

> [!NOTE]
> Блок данных **макрокомандой НайтиЗапись, после** доступна только в макросов данных.

## <a name="setting"></a>Параметр

Действие **SetField** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Куда включается</p></td>
<td><p>Да</p></td>
<td><p>Строка, идентифицирующая запись для работы. Аргумент <em>в</em> может содержать имя таблицы, запроса или инструкции SQL.</p>

> [!NOTE]
> Указанная запись не может включать данные, хранящиеся в связанной таблице или источник данных ODBC.


<p></p></td>
</tr>
<tr class="even">
<td><p>Условие отбора</p></td>
<td><p>Нет</p></td>
<td><p>Строковое выражение, используемое для ограничения диапазона данных, на котором блок данных <strong>макрокомандой НайтиЗапись, после</strong> выполнения. К примеру, критерии эквивалентны часто предложение WHERE в выражении SQL без слова ГДЕ. Если критерии опускаются, блок данных <strong>макрокомандой НайтиЗапись, после</strong> действует на весь домен, указанный в аргументе <em>в</em> . Поля, который включен в условия также должны входить в <em>в</em>поле.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Нет</p></td>
<td><p>Строка, которая предоставляет альтернативное имя для записи, указанный в аргументе <em>в</em> . Позволяет сократить имя таблицы для последующих ссылок избежать возможных неоднозначных ссылок. Если <em>псевдоним</em> не указан, будут использовать имя таблицы или запроса в качестве псевдоним.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Если условиям, указанным *в* и *Где условие* аргументы указывает более одной записи, блок данных **макрокомандой НайтиЗапись, после** будет работать только на первой записи.

## <a name="example"></a>Пример

Следующий пример демонстрирует действие SetReturnVar используется для возврата значения из именованный макрос данных. ReturnVar, с именем **CurrentServiceRequest** возвращается в макросе или Visual Basic для приложений (VBA) подпрограмму, которая называется именованный макрос данных.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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

Следующем примере показано, как использовать действие RaiseError для отмены события макрос данных до изменения. При обновлении поля Кому назначено блок данных макрокомандой НайтиЗапись, после используется для определения, назначенный технического специалиста в настоящее время назначен ли запроса на открытие службы. Если это так, отмене события до изменения и запись не обновляется.

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
