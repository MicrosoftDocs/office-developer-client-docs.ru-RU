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
ms.openlocfilehash: 943f16c5bb1f1525c8da36938fa6beb2e6f71444
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929799"
---
# <a name="after-delete-macro-event"></a>Событие макроса After Delete


**Применимо к**: Access 2013, Office 2013

**После удаления** событие происходит после удаления записи.


> [!NOTE]
> События **После удаления** доступна только в макросов данных.



## <a name="remarks"></a>Примечания

Событие **После удаления** используется для выполнения действий, которые должны происходить при удалении записи. Чаще всего используется **После удаления** включают применение бизнес-правил, рабочие процессы, обновление общую сумму и отправки уведомлений.

При возникновении события **После удаления** значения, содержащиеся в удаленной записи все еще доступны. Можно использовать удаленные значение для увеличения или уменьшения всего, аудита или сравнить существующее значение аргумента *WhereCondition* .

Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** . В следующем примере кода показано, как использовать выражение If staement, чтобы определить, определить, были ли изменены в поле PaidInFull.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Можно использовать доступа значение в удаленной записи, используя следующий синтаксис.

`[Old].[Field Name]`

Например для доступа к значению поля QuantityInStock в удаленной записи, используйте следующий синтаксис.

`[Old].[QuantityInStock]`

Значения, содержащиеся в удаленную запись удаляется без возможности восстановления при окончания события **После удаления** .

Приведенные ниже команды макрос можно использовать в событии **После удаления** .

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
<td><p><a href="comment-macro-statement.md">Оператор макроса Comment</a></p></td>
</tr>
<tr class="even">
<td><p>Выполнение программы</p></td>
<td><p><a href="group-macro-statement.md">Оператор макроса Group</a></p></td>
</tr>
<tr class="odd">
<td><p>Выполнение программы</p></td>
<td><p><a href="if-then-else-macro-block.md">Блок макросов If...Then...Else</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="createrecord-data-block.md">Действия макроса СоздатьЗапись</a></p></td>
</tr>
<tr class="odd">
<td><p>Блок данных</p></td>
<td><p><a href="editrecord-data-block.md">Действия макроса ИзменитьЗапись</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="foreachrecord-data-block.md">Действия макроса ДляКаждойЗаписи</a></p></td>
</tr>
<tr class="odd">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Блок данных макрокомандой НайтиЗапись, после</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">Макрокоманда CancelRecordChange</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Макрокоманда ClearMacroError</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="deleterecord-macro-action.md">Макрокоманда DeleteRecord</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">Макрокоманда ExitForEachRecord</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="logevent-macro-action.md">Макрокоманда LogEvent</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="onerror-macro-action.md">Макрокоманда OnError</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Макрокоманда RaiseError</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="rundatamacro-macro-action.md">Макрокоманда RunDataMacro</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="sendemail-macro-action.md">Макрокоманда SendEmail</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="setfield-macro-action.md">Макрокоманда SetField</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда SetLocalVar</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="stopallmacros-macro-action.md">Макрокоманда StopAllMacros</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Макрокоманда StopMacro</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос данных, который захватывает событие **После удаления** , выполните следующие действия.

1.  Откройте таблицу для записи события **После удаления** .

2.  На вкладке **таблицы** в группе **После событий** щелкните **После удаления**.

Пустой макрос данных отображается в конструктор макросов.

## <a name="example"></a>Пример

В следующем примере кода используется событие **После удаления** для обработки некоторых при удалении записи из таблицы пожертвования. При удалении записи объем пожертвования — форма subracted DonationsReceived поля в таблице DonationsReceived и TotalDonatedField в таблице дарители.

**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**

Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия.

1.  Откройте таблицу для записи события **После удаления** .

2.  На вкладке **таблицы** в группе **После событий** щелкните **После удаления**.

3.  Выберите код, приведенный ниже и нажмите клавиши CTRL + C для копирования его в буфер обмена.

4.  Активация окно конструктора макросов и нажмите клавиши CTRL + V.

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
