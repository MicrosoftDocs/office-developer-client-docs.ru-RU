---
title: Прежде чем событие изменения макросов
TOCTitle: Before Change Macro Event
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
ms.openlocfilehash: 09188378ff75944f6dc8acccc64b621ea2bca1f6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887861"
---
# <a name="before-change-macro-event"></a>Прежде чем событие изменения макросов

**Применимо к**: Access 2013, Office 2013

Событие **Перед изменение** происходит при изменении записи, но перед сохранением изменений.

> [!NOTE]
> Событие **Change перед** доступна только в макросов данных.

## <a name="remarks"></a>Замечания

Изменить с помощью события **До изменения** для выполнения действий, которые следует выполнить перед записью. **До изменения** обычно используется для выполнения проверки и повысить пользовательские сообщения об ошибках.

Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** . В следующем примере кода показано, как использовать оператор **If** для определения, были ли изменены в поле PaidInFull.

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

Свойство **IsInsert** определяет ли событие **Перед изменение** было включено путем создания новой записи или изменение существующей записи. Они **IsInsert** свойство содержит **значение True** , если событие было вызвано **новую запись** , если событие было вызвано изменение существующей записи en.

В следующем примере кода показан синтаксис для с помощью свойства **IsInsert** .

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

Можно использовать доступ в предыдущем значение в поле, используя следующий синтаксис.

```vb
    [Old].[Field Name]
```

Например чтобы получить доступ к предыдущей значение поля QuantityInStock, используйте следующий синтаксис.

```vb
    [Old].[QuantityInStock]
```

Предыдущие значения удаляется без возможности восстановления при окончания события **До изменения** .

С помощью действия **RaiseError** можно отменить событие **До изменения** . При возникновении ошибки изменения, содержащиеся в событии **До изменения** будут удалены.

В следующей таблице перечислены команды макросов, которые можно использовать в событии**До изменения** .

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
<td><p>Выполнение программы</p></td>
<td><p><a href="comment-macro-statement.md">Оператор комментария макросов</a></p></td>
</tr>
<tr class="even">
<td><p>Выполнение программы</p></td>
<td><p><a href="group-macro-statement.md">Оператор группы макросов</a></p></td>
</tr>
<tr class="odd">
<td><p>Выполнение программы</p></td>
<td><p><a href="if-then-else-macro-block.md">If... Затем... Блок else макросов</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Действия макрокомандой НайтиЗапись, после макроса</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Действия макроса ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="onerror-macro-action.md">Действия макроса OnError</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Действия макроса RaiseError</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="setfield-macro-action.md">Действия SetField макроса</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Действия макроса SetLocalVar</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Действия ОстановитьМакрос макроса</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос данных, который захватывает события **До изменения** , выполните следующие действия:

1.  Откройте таблицу для записи события **До изменения** .

2.  На вкладке **таблицы** в группе **Перед событий** щелкните **До изменения**.

Макрос пустой данных отображается в конструктор макросов.

## <a name="example"></a>Пример

В следующем примере кода используется события **До изменения** для проверки состояния полей. Если содержится неверное значение в поле разрешения, возникает ошибка.

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

Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия.

1.  Откройте таблицу для записи события **До изменения** .

2.  На вкладке **таблицы** в группе **Перед событий** щелкните **До изменения**.

3.  Выберите код в следующем примере кода и нажмите **Клавиши CTRL + C** для копирования его в буфер обмена.

4.  Активация окно конструктора макросов и нажмите клавиши **CTRL + V**.



```xml
<DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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
