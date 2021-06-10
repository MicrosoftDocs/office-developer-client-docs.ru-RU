---
title: Макрокоманда RaiseError
TOCTitle: RaiseError macro action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b706ffed14fdb440f3c3192c7c36015343f2e134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300926"
---
# <a name="raiseerror-macro-action"></a>Макрокоманда RaiseError

**Область применения**: Access 2013, Office 2013 

Действие **RaiseError** бросает исключение, которое может быть обработано макро-действием **[OnError.](onerror-macro-action.md)**

> [!NOTE]
> Действие **RaiseError** доступно только в Макросах данных.

## <a name="setting"></a>Параметр

Действие **RaiseError имеет** следующие аргументы.

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
<td><p>Номер ошибки</p></td>
<td><p>Да</p></td>
<td><p>Число или выражение, разрешаемая типу Длинные данные.</p></td>
</tr>
<tr class="even">
<td><p>Описание ошибки</p></td>
<td><p>Нет</p></td>
<td><p>Строка, описываемая ошибкой.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Если действие **RaiseError** вызывается **[](before-change-macro-event.md)** в **[](before-delete-macro-event.md)** событии перед изменением или перед удалением макросов, событие отменяется.

Если не существует активного заявления **OnError,** которое занимается ошибками, ошибка, брошенная действием **RaiseError,** добавляется в таблицу **системы USysApplicationLog.** Когда действие **RaiseError** для записи в таблицу **USysApplicationLog** автоматически задает столбец **Category** **к исполнению**.

Чтобы увидеть **таблицу USysApplicationLog,** используйте следующие действия:

1.  Щелкните **меню File** и нажмите кнопку **Параметры**.

2.  В **диалоговом окне Параметры** доступа щелкните вкладку **Current Database.**

3.  В разделе **Навигация** нажмите **кнопку Параметры навигации**.

4.  В **диалоговом окне Параметры** навигации щелкните **Показать объекты системы** и нажмите **кнопку ОК**.

5.  Нажмите **кнопку ОК,** чтобы **отклонять диалоговое** окно Access Options.

## <a name="example"></a>Пример

В следующем примере показано, как использовать действие RaiseError для отмены макрос события перед изменением данных. При обновлении поля AssignedTo блок данных LookupRecord используется для определения того, назначен ли назначенный специалист в настоящее время запросу открытой службы. Если это так, событие Before Change отменяется и запись не обновляется.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
