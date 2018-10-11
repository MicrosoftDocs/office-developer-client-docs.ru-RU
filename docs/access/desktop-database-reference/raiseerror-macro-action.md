---
title: RaiseError Macro Action
TOCTitle: RaiseError Macro Action
ms:assetid: c8c57685-b373-67d6-cea6-8f2c334547d3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823192(v=office.15)
ms:contentKeyID: 48547661
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 134222e825826615feb495adaae6296229edb868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480276"
---
# <a name="raiseerror-macro-action"></a>RaiseError Macro Action

**Применимо к**: Access 2013 | Office 2013 

Действие **RaiseError** создает исключение, могут быть обработаны **[ПриОшибке](onerror-macro-action.md)** .

> [!NOTE]
> Действие **RaiseError** доступна только в макросов данных.

## <a name="setting"></a>Параметр

Действие **RaiseError** состоит из следующих аргументов.

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
<td><p>Номер ошибки</p></td>
<td><p>Да</p></td>
<td><p>Число или выражение, которое разрешается в тип данных Long.</p></td>
</tr>
<tr class="even">
<td><p>Описание ошибки</p></td>
<td><p>Нет</p></td>
<td><p>Строковое выражение, описывающее ошибку.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Если действие **RaiseError** вызывается в событии макрос **[До изменения](before-change-macro-event.md)** или **[До удаления](before-delete-macro-event.md)** , отмене события.

Если не является активной инструкции **OnError** , который обрабатывает ошибки, ошибку, сгенерированную действие **RaiseError** добавляется к **системе см** . Когда действие **RaiseError** записывает **сведения см** , в столбце **категории** автоматически устанавливается значение **выполнения**.

Чтобы просмотреть **сведения см** , выполните следующие действия:

1.  Выберите в меню **файл** и выберите пункт **Параметры**.

2.  В диалоговом окне **Параметры доступа к** перейдите на вкладку **Текущей базы данных** .

3.  В разделе **Переходы** щелкните **Параметры навигации**.

4.  В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**и нажмите кнопку **ОК**.

5.  Нажмите **кнопку ОК** , чтобы закрыть диалоговое окно **Параметры доступа** .

## <a name="example"></a>Пример

Следующем примере показано, как использовать действие RaiseError для отмены события макрос данных до изменения. При обновлении поля Кому назначено блок данных макрокомандой НайтиЗапись, после используется для определения, назначенный технического специалиста в настоящее время назначен ли запроса на открытие службы. Если это так, затем отмене события до изменения и запись не обновляется.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
