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

Событие **Before Change** возникает при изменении записи, но до фиксации изменения.

> [!NOTE]
> Событие " **до изменения** " доступно только в макросах данных.

## <a name="remarks"></a>Примечания

Используйте событие **Before Change** для выполнения действий, которые должны выполняться перед изменением записи. Для выполнения проверки и порождения настраиваемых сообщений об ошибках обычно используется значение **Before Change** .

Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле. В приведенном ниже примере кода показано, как использовать оператор **If** , чтобы определить, было ли изменено поле паидинфулл.

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

Свойство **INSERT** используется для определения того, было ли событие **Before Change** вызвано новой создаваемой записью или изменением существующей записи. Свойство **INSERT** содержит **значение true** , если событие вызвано новой записью, и **false** , если событие вызвано изменением существующей записи.

В приведенном ниже примере кода показан синтаксис для использования свойства **INSERT** .

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

Предыдущие значения удаляются навсегда при завершении события **перед изменением** .

Вы можете отменить событие " **до изменения** " с помощью действия **раисиррор** . При возникновении ошибки изменения, которые хранятся в событии **Before Change** , отбрасываются.

В следующей таблице перечислены команды макросов, которые можно использовать в событии**Before Change** .

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
<td><p><a href="lookuprecord-data-block.md">Макрокоманда LookupRecord</a></p></td>
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


Чтобы создать макрос данных, который захватывает событие **Before Change** , выполните следующие действия:

1.  Откройте таблицу, для которой необходимо записать событие **до изменения** .

2.  На вкладке **Таблица** в группе **события до** выберите **перед изменением**.

В окне конструктора макросов отобразится пустой макрос данных.

## <a name="example"></a>Пример

В следующем примере кода для проверки полей состояния используется событие **Before Change** . Если в поле разрешение указано неуместное значение, возникает ошибка.

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

Чтобы просмотреть этот пример в конструкторе макросов, выполните указанные ниже действия.

1.  Откройте таблицу, для которой необходимо записать событие **до изменения** .

2.  На вкладке **Таблица** в группе **события до** выберите **перед изменением**.

3.  Выберите код в приведенном ниже примере кода, а затем нажмите клавиши **CTRL + C** , чтобы скопировать его в буфер обмена.

4.  Активируйте окно конструктора макросов и нажмите клавиши **CTRL + V**.



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
