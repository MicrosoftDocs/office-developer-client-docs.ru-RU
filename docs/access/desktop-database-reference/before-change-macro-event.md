---
title: Событие макроса Before Change
TOCTitle: Before Change macro event
ms:assetid: da456d55-a773-abeb-1fac-ef58e3331cb5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835322(v=office.15)
ms:contentKeyID: 48548077
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm19867
dev_langs:
- xml
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a180068e805ae11883822ebf26f924e10d34bac5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538118"
---
# <a name="before-change-macro-event"></a>Событие макроса Before Change

**Область применения**: Access 2013, Office 2013

Событие **Before Change** происходит при изменении записи, но до совершения изменения.

> [!NOTE]
> Событие **Before Change** доступно только в макросах данных.

## <a name="remarks"></a>Примечания

Используйте событие **Before Change** для выполнения любых действий, которые необходимо выполнить перед изменением записи. Перед **изменением** обычно используется для проверки и повышения пользовательских сообщений об ошибках.

Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле. В следующем примере кода показано, как использовать заявление **If** для определения изменения поля PaidInFull.

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

Используйте свойство **IsInsert,** чтобы определить, было ли событие **Before Change** вызвано создаемой новой записью или изменением существующей записи. Свойство **IsInsert** содержит **True,** если событие было вызвано новой записью **False,** если событие было вызвано изменением для en existing record.

В следующем примере кода показан синтаксис для использования **свойства IsInsert.**

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

Можно использовать доступ к предыдущему значению в поле с помощью следующего синтаксиса.

```vb
    [Old].[Field Name]
```

Например, для доступа к предыдущему значению поля QuantityInStock используйте следующий синтаксис.

```vb
    [Old].[QuantityInStock]
```

Предыдущие значения удаляются навсегда после окончания события **"Перед** изменением".

Событие Before **Change** можно отменить с помощью **действия RaiseError.** При поднятии ошибки отбрасываются изменения, содержащиеся в событии **Before Change.**

В следующей таблице перечислены макро-команды, которые можно использовать в событии **Before Change.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип команды</p></th>
<th><p>Команда</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Управление</p></td>
<td><p><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></p></td>
</tr>
<tr class="even">
<td><p>Управление</p></td>
<td><p><a href="group-macro-statement.md">Оператор макроса "Группа"</a></p></td>
</tr>
<tr class="odd">
<td><p>Управление</p></td>
<td><p><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Макро-действие LookupRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос данных, который захватывает событие **Before Change,** используйте следующие действия:

1.  Откройте таблицу, для которой необходимо зафиксировать событие **Before Change.**

2.  На **вкладке Таблица** в группе **Перед событиями** нажмите кнопку **Перед изменением**.

В окне конструктора макросов отобразится пустой макрос данных.

## <a name="example"></a>Пример

В следующем примере кода для проверки полей Status используется событие Before **Change.** Ошибка вызывается, если в поле Разрешение содержится недопустимое значение.

```vb 
 
/* Check to ensure that if the bug is resloved that the user has selected a resolution      */ 
If   [Status]="3 - Resolved" And IsNull([Resolution])   Then 
 
     RaiseError 
             Error Number   1 
        Error Description   You must select a resolution. 
End If 
 
/* Check to ensure that if a bug is closed that the user has selected a resolution first     */ 
If   [Status]="4 - Closed" And IsNull([Resolution])   Then 
 
      RaiseError 
             Error Number   2 
        Error Description   An issue must be resolved before it can be closed. 
End If 
 
If   [Status]<>"3 - Resolved" And [Status]<>"4 - Closed"   Then 
 
      SetField 
             Name   Resolution 
            Value   =Null 
End If 
 
```

Чтобы просмотреть этот пример в конструкторе макроса, используйте следующие действия.

1.  Откройте таблицу, для которой необходимо зафиксировать событие **Before Change.**

2.  На **вкладке Таблица** в группе **Перед событиями** нажмите кнопку **Перед изменением**.

3.  Выберите код в следующем примере кода и нажмите **кнопку CTRL+C,** чтобы скопировать его в буфер обмена.

4.  Активируйте окно конструктора макроса и нажмите **кнопку CTRL+V**.



```xml
<DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
  <DataMacro Event="BeforeChange"> 
    <Statements> 
      <Comment>Check to ensure that if the bug is resloved that the user has selected a resolution </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="3 - Resolved" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">1</Argument> 
              <Argument Name="Description">You must select a resolution.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <Comment>Check to ensure that if a bug is closed that the user has selected a resolution first </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="4 - Closed" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">2</Argument> 
              <Argument Name="Description">An issue must be resolved before it can be closed.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]&lt;&gt;"3 - Resolved" And [Status]&lt;&gt;"4 - Closed"</Condition> 
          <Statements> 
            <Action Name="SetField"> 
              <Argument Name="Field">Resolution</Argument> 
              <Argument Name="Value">Null</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
    </Statements> 
  </DataMacro> 
</DataMacros>
```

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
