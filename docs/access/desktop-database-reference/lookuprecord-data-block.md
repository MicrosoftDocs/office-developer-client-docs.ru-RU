---
title: Блок данных LookupRecord
TOCTitle: LookupRecord data block
ms:assetid: 750dc8ca-3bab-c3d1-c91d-2196f9c0604d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195882(v=office.15)
ms:contentKeyID: 48545671
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7a5cccb77300f36f3e33cd1eccb6c6d278db3120
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734212"
---
# <a name="lookuprecord-data-block"></a>Блок данных LookupRecord

**Область применения**: Access 2013, Office 2013

Блок **данных LookupRecord** выполняет набор действий с определенной записью.

> [!NOTE]
> Блок **данных LookupRecord** доступен только в макросах данных.

## <a name="setting"></a>Setting

Действие **SetField** имеет следующие аргументы.

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
<td><p>Строка, идентифицирует запись, с которую необходимо работать. Аргумент <em>In</em> может содержать имя таблицы, запрос выбора или SQL.</p><p><strong>ПРИМЕЧАНИЕ.</strong>Указанная запись не может включать данные, хранимые в связанной таблице или источнике данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Where Condition</p></td>
<td><p>Нет</p></td>
<td><p>Строка выражения, используемая для ограничения диапазона данных, для которого выполняется блок данных <strong>LookupRecord.</strong> Например, критерии часто эквивалентны предложению WHERE в SQL выражения без слова WHERE. Если критерии не указаны, блок данных <strong>LookupRecord</strong> работает на всем домене, указанном аргументом <em>In.</em> Любое поле, включенное в условия, также должно быть полем в <em>in</em>.</p></td>
</tr>
<tr class="odd">
<td><p>Alias</p></td>
<td><p>Нет</p></td>
<td><p>Строка, которая предоставляет альтернативное имя для записи, указанной в <em>аргументе In.</em> Часто используется для сокращения имени таблицы для последующих ссылок, чтобы предотвратить возможные неоднозначные ссылки. Если <em>псевдоним не</em> указан, в качестве псевдонима будет использоваться таблица или имя запроса.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Если критерии, указанные  аргументами условия "В" и "Где", возвращают несколько записей, блок данных **LookupRecord** будет работать только с первой записью.   Если записи не соответствуют заданным условиям, Access пропустит набор действий, содержащихся в блоке **LookupRecord,** как если бы это было выражение блока макроса **[If,](if-then-else-macro-block.md)** которое было оценено как false.

## <a name="example"></a>Пример

В следующем примере показано, как использовать действие SetReturnVar для возврата значения из именоваемом макроса данных. ReturnVar с **именем CurrentServiceRequest** возвращается в подгруппу макроса или Visual Basic для приложений (VBA), которая вызвала именуемого макроса данных.

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

В следующем примере показано, как использовать действие RaiseError для отмены события макроса данных "Перед изменением". При обновлении поля AssignedTo блок данных LookupRecord используется для определения того, назначен ли техники в настоящее время открытый запрос на обслуживание. Если это так, событие before Change отменяется, а запись не обновляется.

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
