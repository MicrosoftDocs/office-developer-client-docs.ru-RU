---
title: Событие макроса After Delete
TOCTitle: After Delete macro event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f524a544736f68bcfa6bd15e3bcc720ffa2bc4d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297216"
---
# <a name="after-delete-macro-event"></a>Событие макроса After Delete

**Область применения**: Access 2013, Office 2013

Событие **After Delete** возникает после удаления записи.

> [!NOTE]
> Событие " **после удаления** " доступно только для макросов данных.

## <a name="remarks"></a>Замечания

Используйте событие " **после удаления** " для выполнения действий, которые должны выполняться при удалении записи. Типичные случаи использования " **после удаления** " включают применение бизнес-правил, рабочих процессов, обновление итоговых сумм и отправку уведомлений.

При возникновении события " **после удаления** " значения, хранящиеся в удаленной записи, по-прежнему доступны. Можно использовать удаленное значение для увеличения или уменьшения суммы, создания журнала аудита или сравнения с существующим значением в аргументе *WhereCondition* .

Можно использовать функцию **Updated ("*имя поля*")** , чтобы определить, изменилось ли поле. В приведенном ниже примере кода показано, как использовать метод if стаемент, чтобы определить, было ли изменено поле Паидинфулл.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Вы можете использовать доступ к значению в удаленной записи, используя следующий синтаксис.

`[Old].[Field Name]`

Например, чтобы получить доступ к значению поля Куантитинстокк в удаленной записи, используйте следующий синтаксис.

`[Old].[QuantityInStock]`

Значения, хранящиеся в удаленной записи, удаляются навсегда при завершении события " **после удаления** ".

В событии **After Delete** можно использовать следующие команды макросов.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип команды</p></th>
<th><p>Command</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Program Flow</p></td>
<td><p><a href="comment-macro-statement.md">Оператор макроса Comment</a></p></td>
</tr>
<tr class="even">
<td><p>Program Flow</p></td>
<td><p><a href="group-macro-statement.md">Оператор макроса Group</a></p></td>
</tr>
<tr class="odd">
<td><p>Program Flow</p></td>
<td><p><a href="if-then-else-macro-block.md">Блок макросов If...Then...Else</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="createrecord-data-block.md">Макрокоманда СоздатьЗапись</a></p></td>
</tr>
<tr class="odd">
<td><p>Блок данных</p></td>
<td><p><a href="editrecord-data-block.md">Макрокоманда ИзменитьЗапись</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="foreachrecord-data-block.md">Макрокоманда ДляКаждойЗаписи</a></p></td>
</tr>
<tr class="odd">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Блок данных LookupRecord</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">Макрокоманда CancelRecordChange</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Макрокоманда ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="deleterecord-macro-action.md">Макрокоманда DeleteRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">Макрокоманда ExitForEachRecord</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="logevent-macro-action.md">Макрокоманда LogEvent</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="onerror-macro-action.md">Макрокоманда OnError</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Макрокоманда RaiseError</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="rundatamacro-macro-action.md">Макрокоманда RunDataMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="sendemail-macro-action.md">Макрокоманда SendEmail</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="setfield-macro-action.md">Макрокоманда SetField</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда SetLocalVar</a></p></td>
</tr>
<tr class="odd">
<td><p>Действие с данными</p></td>
<td><p><a href="stopallmacros-macro-action.md">Макрокоманда StopAllMacros</a></p></td>
</tr>
<tr class="even">
<td><p>Действие с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Макрокоманда StopMacro</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос данных, который захватывает событие **After Delete** , выполните указанные ниже действия.

1.  Откройте таблицу, для которой необходимо записать событие " **после удаления** ".

2.  На вкладке **Таблица** в группе **после событий** нажмите кнопку **после удаления**.

Пустой макрос данных отображается в конструкторе макросов.

## <a name="example"></a>Пример

В следующем примере кода показано использование события **After Delete** для выполнения некоторой обработки при удалении записи из таблицы пожертвования. Когда запись удаляется, сумма пожертвований субрактед Forms в поле Донатионсрецеивед таблицы Донатионсрецеивед и Тоталдонатедфиелд в таблице благотворителей.

**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**

Чтобы просмотреть этот пример в конструкторе макросов, выполните указанные ниже действия.

1.  Откройте таблицу, для которой необходимо записать событие " **после удаления** ".

2.  На вкладке **Таблица** в группе **после событий** нажмите кнопку **после удаления**.

3.  Выберите приведенный ниже код и нажмите клавиши CTRL + C, чтобы скопировать его в буфер обмена.

4.  Активируйте окно конструктора макросов и нажмите клавиши CTRL + V.

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterDelete"> 
        <Statements> 
          <Comment>Initialize a variable and assign the old</Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Old].[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Old].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Collapsed="true" Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([Old].[DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Old].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]-[varAmount]</Argument> 
                        </Action> 
                      </Statements> 
                    </EditRecord> 
                  </Statements> 
                </ForEachRecord> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
```

<br/>

```vb
    SetLocalVar 
                    Name    varAmount 
              Expression   =[Old].[Amount] 
     
    If   Not(IsNull([Old].[CampaignID]]))   Then 
     
         For Each Record In     Campaigns 
            Where Condition     =[ID]=[Old].[CampaignID] 
                      Alias 
            EditRecord 
                      Alias 
                  SetField   ([DonationsReceived], [DonationsReceived] - [varAmount]) 
            End EditRecord 
     
    End If 
     
    If   Not(IsNull([Old].[DonorID]]))   Then 
     
         For Each Record In    Donors 
            Where Condition     =[ID]=[Old].[DonorID] 
                      Alias 
            EditRecord 
                      Alias 
     
              SetField 
                             Name   [TotalDonated] 
                            Value   =[TotalDonated]-[varAmount] 
            End EditRecord 
    End If
```
