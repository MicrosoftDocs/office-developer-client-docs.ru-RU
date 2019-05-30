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
ms.openlocfilehash: 5b3b2da44d817885eb6190a8cbbfc73bf99e9e0a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538237"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="5059b-102">Событие макроса After Delete</span><span class="sxs-lookup"><span data-stu-id="5059b-102">After Delete macro event</span></span>

<span data-ttu-id="5059b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5059b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5059b-104">Событие **After Delete** возникает после удаления записи.</span><span class="sxs-lookup"><span data-stu-id="5059b-104">The **After Delete** event occurs after a record is deleted.</span></span>

> [!NOTE]
> <span data-ttu-id="5059b-105">Событие " **после удаления** " доступно только для макросов данных.</span><span class="sxs-lookup"><span data-stu-id="5059b-105">The **After Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="5059b-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="5059b-106">Remarks</span></span>

<span data-ttu-id="5059b-107">Используйте событие " **после удаления** " для выполнения действий, которые должны выполняться при удалении записи.</span><span class="sxs-lookup"><span data-stu-id="5059b-107">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted.</span></span> <span data-ttu-id="5059b-108">Типичные случаи использования " **после удаления** " включают применение бизнес-правил, рабочих процессов, обновление итоговых сумм и отправку уведомлений.</span><span class="sxs-lookup"><span data-stu-id="5059b-108">Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="5059b-109">При возникновении события " **после удаления** " значения, хранящиеся в удаленной записи, по-прежнему доступны.</span><span class="sxs-lookup"><span data-stu-id="5059b-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="5059b-110">Можно использовать удаленное значение для увеличения или уменьшения суммы, создания журнала аудита или сравнения с существующим значением в аргументе *WhereCondition* .</span><span class="sxs-lookup"><span data-stu-id="5059b-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="5059b-111">Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле.</span><span class="sxs-lookup"><span data-stu-id="5059b-111">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="5059b-112">В приведенном ниже примере кода показано, как использовать метод if стаемент, чтобы определить, было ли изменено поле Паидинфулл.</span><span class="sxs-lookup"><span data-stu-id="5059b-112">The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="5059b-113">Вы можете использовать доступ к значению в удаленной записи, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="5059b-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="5059b-114">Например, чтобы получить доступ к значению поля Куантитинстокк в удаленной записи, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="5059b-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="5059b-115">Значения, хранящиеся в удаленной записи, удаляются навсегда при завершении события " **после удаления** ".</span><span class="sxs-lookup"><span data-stu-id="5059b-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="5059b-116">В событии **After Delete** можно использовать следующие команды макросов.</span><span class="sxs-lookup"><span data-stu-id="5059b-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5059b-117">Тип команды</span><span class="sxs-lookup"><span data-stu-id="5059b-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="5059b-118">Команда</span><span class="sxs-lookup"><span data-stu-id="5059b-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5059b-119">Управление</span><span class="sxs-lookup"><span data-stu-id="5059b-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="5059b-120"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-120"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-121">Управление</span><span class="sxs-lookup"><span data-stu-id="5059b-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="5059b-122"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-122"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-123">Управление</span><span class="sxs-lookup"><span data-stu-id="5059b-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="5059b-124"><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></span><span class="sxs-lookup"><span data-stu-id="5059b-124"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-125">Блок данных</span><span class="sxs-lookup"><span data-stu-id="5059b-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5059b-126"><a href="createrecord-data-block.md">Макрокоманда "СоздатьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-126"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-127">Блок данных</span><span class="sxs-lookup"><span data-stu-id="5059b-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5059b-128"><a href="editrecord-data-block.md">Макрокоманда "ИзменитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-128"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-129">Блок данных</span><span class="sxs-lookup"><span data-stu-id="5059b-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5059b-130"><a href="foreachrecord-data-block.md">Макрокоманда "ДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-130"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-131">Блок данных</span><span class="sxs-lookup"><span data-stu-id="5059b-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="5059b-132"><a href="lookuprecord-data-block.md">Блок данных "НайтиЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-132"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-134"><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-135">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-136"><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-136"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-137">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-138"><a href="deleterecord-macro-action.md">Макрокоманда "УдалитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-138"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-139">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-140"><a href="exitforeachrecord-macro-action.md">Макрокоманда "ВыходДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-141">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-142"><a href="logevent-macro-action.md">Макрокоманда "РегистрацияСобытия"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-142"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-143">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-144"><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-144"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-145">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-146"><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-146"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-147">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-148"><a href="rundatamacro-macro-action.md">Макрокоманда "ЗапускМакросаДанных"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-148"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-149">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-150"><a href="sendemail-macro-action.md">Макрокоманда "ОтправитьПочту"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-150"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-151">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-152"><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-152"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-153">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-154"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-154"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5059b-155">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-156"><a href="stopallmacros-macro-action.md">Макрокоманда "ОстановитьВсеМакросы"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-156"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5059b-157">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="5059b-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="5059b-158"><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></span><span class="sxs-lookup"><span data-stu-id="5059b-158"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5059b-159">Чтобы создать макрос данных, который захватывает событие **After Delete** , выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5059b-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="5059b-160">Откройте таблицу, для которой необходимо записать событие " **после удаления** ".</span><span class="sxs-lookup"><span data-stu-id="5059b-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="5059b-161">На вкладке **Таблица** в группе **после событий** нажмите кнопку **после удаления**.</span><span class="sxs-lookup"><span data-stu-id="5059b-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="5059b-162">Пустой макрос данных отображается в конструкторе макросов.</span><span class="sxs-lookup"><span data-stu-id="5059b-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="5059b-163">Пример</span><span class="sxs-lookup"><span data-stu-id="5059b-163">Example</span></span>

<span data-ttu-id="5059b-164">В следующем примере кода показано использование события **After Delete** для выполнения некоторой обработки при удалении записи из таблицы пожертвования.</span><span class="sxs-lookup"><span data-stu-id="5059b-164">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table.</span></span> <span data-ttu-id="5059b-165">Когда запись удаляется, сумма пожертвований субрактед Forms в поле Донатионсрецеивед таблицы Донатионсрецеивед и Тоталдонатедфиелд в таблице благотворителей.</span><span class="sxs-lookup"><span data-stu-id="5059b-165">When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="5059b-166">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="5059b-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="5059b-167">Чтобы просмотреть этот пример в конструкторе макросов, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5059b-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="5059b-168">Откройте таблицу, для которой необходимо записать событие " **после удаления** ".</span><span class="sxs-lookup"><span data-stu-id="5059b-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="5059b-169">На вкладке **Таблица** в группе **после событий** нажмите кнопку **после удаления**.</span><span class="sxs-lookup"><span data-stu-id="5059b-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="5059b-170">Выберите приведенный ниже код и нажмите клавиши CTRL + C, чтобы скопировать его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="5059b-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="5059b-171">Активируйте окно конструктора макросов и нажмите клавиши CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="5059b-171">Activate the macro designer window and then press CTRL+V.</span></span>

<!-- end list -->

```xml
    <?xml version="1.0" encoding="UTF-16" standalone="no"?> 
    <DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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
