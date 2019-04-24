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

Действие **раисиррор** создает исключение, которое может быть обработано макрокомандОй **[OnError](onerror-macro-action.md)** .

> [!NOTE]
> Действие **раисиррор** доступно только в макросах данных.

## <a name="setting"></a>Параметр

Макрокоманда **раисиррор** имеет следующие аргументы.

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

Если действие **раисиррор** вызывается в событии **[перед изменением](before-change-macro-event.md)** или **[перед удалением](before-delete-macro-event.md)** макроса, событие отменяется.

Если отсутствует активный оператор OnError **** , который обрабатывает ошибки, то ошибка, вызываемая действием **раисиррор** , добавляется в системную таблицу **усисаппликатионлог** . При выполнении действия **раисиррор** для записи в таблицу **Усисаппликатионлог** для столбца **Category** автоматически устанавливается значение **выполнение**.

Чтобы просмотреть таблицу **усисаппликатионлог** , выполните указанные ниже действия.

1.  Откройте меню **файл** и выберите пункт **Параметры**.

2.  В диалоговом окне **Параметры Access** перейдите на вкладку **Текущая база данных** .

3.  В разделе **Навигация** щелкните **Параметры навигации**.

4.  В диалоговом окне **Параметры навигации** нажмите кнопку **Показать системные объекты**, а затем нажмите кнопку **ОК**.

5.  Нажмите кнопку **ОК** , чтобы закрыть диалоговое окно **Параметры Access** .

## <a name="example"></a>Пример

В приведенном ниже примере показано, как использовать действие Раисиррор для отмены события перед изменением данных макроса. При обновлении поля AssignedTo используется блок данных LookupRecord, чтобы определить, назначен ли назначенному специалисту открытый запрос на обслуживание. Если этот параметр имеет значение true, то событие "до изменения" отменяется и запись не обновляется.

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
