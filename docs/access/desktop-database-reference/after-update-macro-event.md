---
title: Событие макроса "После обновления"
TOCTitle: After Update macro event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: a96b46fcc78c4f93887e487f52091a77da6c0d2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297188"
---
# <a name="after-update-macro-event"></a>Событие макроса "После обновления"

**Область применения**: Access 2013, Office 2013

Событие макроса **После обновления** возникает после изменения записи.

> [!NOTE]
> Событие **После обновления** доступно только в макросах данных.

## <a name="remarks"></a>Примечания

Используйте событие **После обновления**, чтобы выполнять любые действия, которые должны происходить при изменении записи. Распространенные варианты использования события **После вставки** включают применение бизнес-правил, обновление суммарного итогового значения и отправку уведомлений.

Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле. В следующем примере кода показано, как использовать инструкцию **If**, чтобы определить, изменилось ли поле PaidInFull.

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

Можно использовать доступ к предыдущему значению в поле с помощью следующего синтаксиса.

`[Old].[Field Name]`

Например, для доступа к предыдущему значению поля QuantityInStock используйте следующий синтаксис.

`[Old].[QuantityInStock]`

Предыдущие значения удаляются без возможности восстановления при завершении события **После обновления**.

В следующей таблице перечислены макрокоманды, которые можно использовать в событии **После обновления**.

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


Чтобы создать макрос данных, который записывает событие **После обновления**, выполните следующие действия:

1.  Откройте таблицу, для которой нужно записать событие **После обновления**.

2.  На вкладке **Таблица** в группе **После событий** щелкните **После обновления**.

В окне конструктора макросов отобразится пустой макрос данных.

## <a name="example"></a>Пример

В следующем примере кода используется событие **После обновления** для запуска именованного макроса данных, добавляющего запись в таблицу Comment (Примечание) при каждом обновлении состояния проблемы.

**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**

Чтобы просмотреть этот пример в конструкторе макросов, выполните следующие действия:

1.  Откройте таблицу, для которой нужно записать событие **После обновления**.

2.  На вкладке **Таблица** в группе **После событий** щелкните **После обновления**.

3.  Выделите код в следующем примере и нажмите клавиши CTRL+C, чтобы скопировать его в буфер обмена.

4.  Активируйте окно конструктора макросов и нажмите клавиши CTRL+V.

<!-- end list -->

```xml
    <DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
      <DataMacro Event="AfterUpdate"> 
        <Statements> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Status")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Status changed to &quot; &amp; [Status]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
          <ConditionalBlock> 
            <If> 
              <Condition>Updated("Resolution")</Condition> 
              <Statements> 
                <Action Name="RunDataMacro"> 
                  <Argument Name="MacroName">Comments.AddComment</Argument> 
                  <Parameters> 
                    <Parameter Name="prmRelatedID" Value="[ID]" /> 
                    <Parameter Name="prmUserID" Value="[UserID]" /> 
                    <Parameter Name="prmComment" Value="&quot;-- Issue resolved as &quot; &amp; [Resolution]" /> 
                  </Parameters> 
                </Action> 
              </Statements> 
            </If> 
          </ConditionalBlock> 
        </Statements> 
      </DataMacro> 
    </DataMacros>
``` 

<br/>

```vb
If  Updated("Status")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
         prmComment   ="--Status Changes to "&[Status] 
          prmUserID   =[ChangedByUserID] 
End If 
 
If   Updated("Resolution")   Then 
     RunDataMacro 
        Macro Name   Comments.AddComment 
     Parameters 
       prmRelatedID   = [ID] 
          prmUserID   =[ChangedByUserID] 
         prmComment   ="--Issue Resolved as "&[Status] 
End If 
```

