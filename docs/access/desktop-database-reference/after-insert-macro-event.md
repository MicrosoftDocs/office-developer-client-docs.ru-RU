---
title: Событие макроса "После вставки"
TOCTitle: After Insert macro event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: c84a737d08b791bfe560bfe6af6bcc59a14d2678
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297223"
---
# <a name="after-insert-macro-event"></a>Событие макроса "После вставки"

**Область применения**: Access 2013, Office 2013

Событие макроса **После вставки** возникает после добавления записи.

> [!NOTE]
> Событие **После вставки** доступно только в макросах данных.

## <a name="remarks"></a>Примечания

Используйте событие **После вставки**, чтобы выполнять любые действия, которые должны происходить при добавлении записи в таблицу. Распространенные варианты использования события **После вставки** включают применение бизнес-правил, рабочих процессов, обновление суммарного итогового значения и отправку уведомлений.

Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле. В следующем примере кода показано, как использовать инструкцию **If**, чтобы определить, изменилось ли поле PaidInFull.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

В следующей таблице перечислены макрокоманды, которые можно использовать в событии **После вставки**.

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
<td><p><a href="createrecord-data-block.md">Макрокоманда "СоздатьЗапись"</a></p></td>
</tr>
<tr class="odd">
<td><p>Блок данных</p></td>
<td><p><a href="editrecord-data-block.md">Макрокоманда "ИзменитьЗапись"</a></p></td>
</tr>
<tr class="even">
<td><p>Блок данных</p></td>
<td><p><a href="foreachrecord-data-block.md">Макрокоманда "ДляКаждойЗаписи"</a></p></td>
</tr>
<tr class="odd">
<td><p>Блок данных</p></td>
<td><p><a href="lookuprecord-data-block.md">Блок данных "НайтиЗапись"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="deleterecord-macro-action.md">Макрокоманда "УдалитьЗапись"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="exitforeachrecord-macro-action.md">Макрокоманда "ВыходДляКаждойЗаписи"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="logevent-macro-action.md">Макрокоманда "РегистрацияСобытия"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="rundatamacro-macro-action.md">Макрокоманда "ЗапускМакросаДанных"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="sendemail-macro-action.md">Макрокоманда "ОтправитьПочту"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></p></td>
</tr>
<tr class="odd">
<td><p>Действия с данными</p></td>
<td><p><a href="stopallmacros-macro-action.md">Макрокоманда "ОстановитьВсеМакросы"</a></p></td>
</tr>
<tr class="even">
<td><p>Действия с данными</p></td>
<td><p><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></p></td>
</tr>
</tbody>
</table>


Чтобы создать макрос данных, который записывает событие **После вставки**, выполните следующие действия:

1.  Откройте таблицу, для которой нужно записать событие **После вставки**.

2.  На вкладке **Таблица** в группе **После событий** щелкните **После вставки**.

В окне конструктора макросов отобразится пустой макрос данных.

## <a name="example"></a>Пример

В следующем примере кода используется событие **После вставки** для выполнения некоторой обработки при добавлении записи в таблицу Donations (Пожертвования). При добавлении записи сумма пожертвований добавляется в поле DonationsReceived таблицы Campaigns (Кампании) и TotalDonatedField таблицы Donors (Спонсоры).

**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**

Чтобы просмотреть этот пример в конструкторе макросов, выполните следующие действия:

1.  Откройте таблицу, для которой нужно записать событие **После вставки**.

2.  На вкладке **Таблица** в группе **После событий** щелкните **После вставки**.

3.  Выделите код в следующем примере и нажмите клавиши CTRL+C, чтобы скопировать его в буфер обмена.

4.  Активируйте окно конструктора макросов и нажмите клавиши CTRL+V.

<!-- end list -->

```xml
    <DataMacros> 
      <DataMacro Event="AfterInsert"> 
        <Statements> 
          <Comment>This data macro increments the DonationsReceived field in Campaigns and theAmountCollected field in Pledges </Comment> 
          <Action Name="SetLocalVar"> 
            <Argument Name="Name">varAmount</Argument> 
            <Argument Name="Value">[Amount]</Argument> 
          </Action> 
          <ConditionalBlock> 
            <If> 
              <Condition>Not (IsNull([CampaignID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Campaigns</Reference> 
                    <WhereCondition>[ID]=[Donations].[CampaignID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[DonationsReceived]</Argument> 
                          <Argument Name="Value">[DonationsReceived]+[varAmount]</Argument> 
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
              <Condition>Not (IsNull([DonorID]))</Condition> 
              <Statements> 
                <ForEachRecord> 
                  <Data> 
                    <Reference>Donors</Reference> 
                    <WhereCondition>[ID]=[Donations].[DonorID]</WhereCondition> 
                  </Data> 
                  <Statements> 
                    <EditRecord> 
                      <Data /> 
                      <Statements> 
                        <Action Name="SetField"> 
                          <Argument Name="Field">[TotalDonated]</Argument> 
                          <Argument Name="Value">[TotalDonated]+[varAmount]</Argument> 
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
                  Name   varAmount 
            Expression   =[Amount] 
     
    If   Not (IsNull([CampaignID]))   Then 
     
         For Each Record In   Campaigns 
            Where Condition   =[ID]=[Donations].[CampaignID] 
                      Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [DonationsReceived] 
                                Value   =[DonationsReceived]+[varAmount] 
                End EditRecord 
    End If 
     
    If   Not (IsNull([DonorID]))   Then 
     
         For Each Record In  Donors 
            WhereCondition   =[ID]=[Donations].[DonorID] 
                     Alias 
     
                 EditRecord 
                              Alias 
                     SetField 
                                 Name   [TotalDonated] 
                                Value   =[TotalDonated]+[varAmount] 
                 End EditRecord 
    End If
```
