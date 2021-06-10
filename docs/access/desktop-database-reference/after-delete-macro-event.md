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
# <a name="after-delete-macro-event"></a><span data-ttu-id="bdacf-102">Событие макроса After Delete</span><span class="sxs-lookup"><span data-stu-id="bdacf-102">After Delete macro event</span></span>

<span data-ttu-id="bdacf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bdacf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bdacf-104">Событие **После удаления** происходит после удаления записи.</span><span class="sxs-lookup"><span data-stu-id="bdacf-104">The **After Delete** event occurs after a record is deleted.</span></span>

> [!NOTE]
> <span data-ttu-id="bdacf-105">Событие **После удаления** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="bdacf-105">The **After Delete** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdacf-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="bdacf-106">Remarks</span></span>

<span data-ttu-id="bdacf-107">Используйте событие **После удаления** для выполнения действий, которые необходимо выполнить при удалении записи.</span><span class="sxs-lookup"><span data-stu-id="bdacf-107">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted.</span></span> <span data-ttu-id="bdacf-108">Распространенные виды использования **для "После** удаления" включают применение бизнес-правил, рабочий процесс, обновление общего общего числа и отправку уведомлений.</span><span class="sxs-lookup"><span data-stu-id="bdacf-108">Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="bdacf-109">Когда происходит **событие После** удаления, значения, содержащиеся в удаленной записи, по-прежнему доступны.</span><span class="sxs-lookup"><span data-stu-id="bdacf-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="bdacf-110">Может потребоваться использовать удаленную величину для приумножания или приумножания общего числа, создания следа аудита или сравнения с существующим значением в аргументе *WhereCondition.*</span><span class="sxs-lookup"><span data-stu-id="bdacf-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="bdacf-111">Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле.</span><span class="sxs-lookup"><span data-stu-id="bdacf-111">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="bdacf-112">В следующем примере кода показано, как использовать застой If, чтобы определить, было ли изменено поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="bdacf-112">The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="bdacf-113">Вы можете использовать доступ к значению в удаленной записи, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="bdacf-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="bdacf-114">Например, чтобы получить доступ к значению поля QuantityInStock в удаленной записи, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="bdacf-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="bdacf-115">Значения, содержащиеся в удаленной записи, удаляются навсегда после окончания события **После** удаления.</span><span class="sxs-lookup"><span data-stu-id="bdacf-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="bdacf-116">Следующие команды макроса можно использовать в событии **После удаления.**</span><span class="sxs-lookup"><span data-stu-id="bdacf-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdacf-117">Тип команды</span><span class="sxs-lookup"><span data-stu-id="bdacf-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="bdacf-118">Команда</span><span class="sxs-lookup"><span data-stu-id="bdacf-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-119">Управление</span><span class="sxs-lookup"><span data-stu-id="bdacf-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="bdacf-120"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-120"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-121">Управление</span><span class="sxs-lookup"><span data-stu-id="bdacf-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="bdacf-122"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-122"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-123">Управление</span><span class="sxs-lookup"><span data-stu-id="bdacf-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="bdacf-124"><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-124"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-125">Блок данных</span><span class="sxs-lookup"><span data-stu-id="bdacf-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="bdacf-126"><a href="createrecord-data-block.md">Макрокоманда "СоздатьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-126"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-127">Блок данных</span><span class="sxs-lookup"><span data-stu-id="bdacf-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="bdacf-128"><a href="editrecord-data-block.md">Макрокоманда "ИзменитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-128"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-129">Блок данных</span><span class="sxs-lookup"><span data-stu-id="bdacf-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="bdacf-130"><a href="foreachrecord-data-block.md">Макрокоманда "ДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-130"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-131">Блок данных</span><span class="sxs-lookup"><span data-stu-id="bdacf-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="bdacf-132"><a href="lookuprecord-data-block.md">Блок данных "НайтиЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-132"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-134"><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-135">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-136"><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-136"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-137">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-138"><a href="deleterecord-macro-action.md">Макрокоманда "УдалитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-138"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-139">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-140"><a href="exitforeachrecord-macro-action.md">Макрокоманда "ВыходДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-141">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-142"><a href="logevent-macro-action.md">Макрокоманда "РегистрацияСобытия"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-142"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-143">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-144"><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-144"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-145">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-146"><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-146"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-147">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-148"><a href="rundatamacro-macro-action.md">Макрокоманда "ЗапускМакросаДанных"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-148"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-149">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-150"><a href="sendemail-macro-action.md">Макрокоманда "ОтправитьПочту"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-150"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-151">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-152"><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-152"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-153">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-154"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-154"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdacf-155">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-156"><a href="stopallmacros-macro-action.md">Макрокоманда "ОстановитьВсеМакросы"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-156"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdacf-157">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="bdacf-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="bdacf-158"><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></span><span class="sxs-lookup"><span data-stu-id="bdacf-158"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bdacf-159">Чтобы создать макрос данных, который фиксирует событие **После удаления,** используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bdacf-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="bdacf-160">Откройте таблицу, для которой необходимо зафиксировать событие **После удаления.**</span><span class="sxs-lookup"><span data-stu-id="bdacf-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="bdacf-161">На **вкладке Таблица** в группе **После событий** нажмите **кнопку После удаления**.</span><span class="sxs-lookup"><span data-stu-id="bdacf-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="bdacf-162">Пустой макрос данных отображается в конструкторе макроса.</span><span class="sxs-lookup"><span data-stu-id="bdacf-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="bdacf-163">Пример</span><span class="sxs-lookup"><span data-stu-id="bdacf-163">Example</span></span>

<span data-ttu-id="bdacf-164">В следующем примере кода для выполнения некоторой обработки при удалении записи из таблицы "Пожертвования" используется событие After **Delete.**</span><span class="sxs-lookup"><span data-stu-id="bdacf-164">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table.</span></span> <span data-ttu-id="bdacf-165">При удалении записи сумма пожертвования передается в субрацированную форму поля DonationsReceived в таблице DonationsReceived и TotalDonatedField в таблице Доноры.</span><span class="sxs-lookup"><span data-stu-id="bdacf-165">When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="bdacf-166">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="bdacf-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="bdacf-167">Чтобы просмотреть этот пример в конструкторе макроса, используйте следующие действия.</span><span class="sxs-lookup"><span data-stu-id="bdacf-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="bdacf-168">Откройте таблицу, для которой необходимо зафиксировать событие **После удаления.**</span><span class="sxs-lookup"><span data-stu-id="bdacf-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="bdacf-169">На **вкладке Таблица** в группе **После событий** нажмите **кнопку После удаления**.</span><span class="sxs-lookup"><span data-stu-id="bdacf-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="bdacf-170">Выберите указанный ниже код и нажмите кнопку CTRL+C, чтобы скопировать его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="bdacf-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="bdacf-171">Активируйте окно конструктора макросов и нажмите клавиши CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="bdacf-171">Activate the macro designer window and then press CTRL+V.</span></span>

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
