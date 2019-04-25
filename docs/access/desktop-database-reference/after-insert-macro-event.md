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
# <a name="after-insert-macro-event"></a><span data-ttu-id="02d9a-102">Событие макроса "После вставки"</span><span class="sxs-lookup"><span data-stu-id="02d9a-102">After Insert macro event</span></span>

<span data-ttu-id="02d9a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02d9a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02d9a-104">Событие макроса **После вставки** возникает после добавления записи.</span><span class="sxs-lookup"><span data-stu-id="02d9a-104">The **After Insert** event occurs after a record is added.</span></span>

> [!NOTE]
> <span data-ttu-id="02d9a-105">Событие **После вставки** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="02d9a-105">The **After Insert** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="02d9a-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="02d9a-106">Remarks</span></span>

<span data-ttu-id="02d9a-107">Используйте событие **После вставки**, чтобы выполнять любые действия, которые должны происходить при добавлении записи в таблицу.</span><span class="sxs-lookup"><span data-stu-id="02d9a-107">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table.</span></span> <span data-ttu-id="02d9a-108">Распространенные варианты использования события **После вставки** включают применение бизнес-правил, рабочих процессов, обновление суммарного итогового значения и отправку уведомлений.</span><span class="sxs-lookup"><span data-stu-id="02d9a-108">Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="02d9a-109">Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле.</span><span class="sxs-lookup"><span data-stu-id="02d9a-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="02d9a-110">В следующем примере кода показано, как использовать инструкцию **If**, чтобы определить, изменилось ли поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="02d9a-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="02d9a-111">В следующей таблице перечислены макрокоманды, которые можно использовать в событии **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="02d9a-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02d9a-112">Тип команды</span><span class="sxs-lookup"><span data-stu-id="02d9a-112">Command type</span></span></p></th>
<th><p><span data-ttu-id="02d9a-113">Команда</span><span class="sxs-lookup"><span data-stu-id="02d9a-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-114">Управление</span><span class="sxs-lookup"><span data-stu-id="02d9a-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="02d9a-115"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-116">Управление</span><span class="sxs-lookup"><span data-stu-id="02d9a-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="02d9a-117"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-118">Управление</span><span class="sxs-lookup"><span data-stu-id="02d9a-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="02d9a-119"><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-120">Блок данных</span><span class="sxs-lookup"><span data-stu-id="02d9a-120">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="02d9a-121"><a href="createrecord-data-block.md">Макрокоманда "СоздатьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-121"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-122">Блок данных</span><span class="sxs-lookup"><span data-stu-id="02d9a-122">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="02d9a-123"><a href="editrecord-data-block.md">Макрокоманда "ИзменитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-123"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-124">Блок данных</span><span class="sxs-lookup"><span data-stu-id="02d9a-124">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="02d9a-125"><a href="foreachrecord-data-block.md">Макрокоманда "ДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-125"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-126">Блок данных</span><span class="sxs-lookup"><span data-stu-id="02d9a-126">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="02d9a-127"><a href="lookuprecord-data-block.md">Блок данных "НайтиЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-127"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-128">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-129"><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-130">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-131"><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-132">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-133"><a href="deleterecord-macro-action.md">Макрокоманда "УдалитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-134">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-135"><a href="exitforeachrecord-macro-action.md">Макрокоманда "ВыходДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-136">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-137"><a href="logevent-macro-action.md">Макрокоманда "РегистрацияСобытия"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-138">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-139"><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-140">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-141"><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-142">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-143"><a href="rundatamacro-macro-action.md">Макрокоманда "ЗапускМакросаДанных"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-144">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-145"><a href="sendemail-macro-action.md">Макрокоманда "ОтправитьПочту"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-146">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-147"><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-148">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-149"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02d9a-150">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-151"><a href="stopallmacros-macro-action.md">Макрокоманда "ОстановитьВсеМакросы"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02d9a-152">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="02d9a-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="02d9a-153"><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></span><span class="sxs-lookup"><span data-stu-id="02d9a-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02d9a-154">Чтобы создать макрос данных, который записывает событие **После вставки**, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="02d9a-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="02d9a-155">Откройте таблицу, для которой нужно записать событие **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="02d9a-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="02d9a-156">На вкладке **Таблица** в группе **После событий** щелкните **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="02d9a-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="02d9a-157">В окне конструктора макросов отобразится пустой макрос данных.</span><span class="sxs-lookup"><span data-stu-id="02d9a-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="02d9a-158">Пример</span><span class="sxs-lookup"><span data-stu-id="02d9a-158">Example</span></span>

<span data-ttu-id="02d9a-159">В следующем примере кода используется событие **После вставки** для выполнения некоторой обработки при добавлении записи в таблицу Donations (Пожертвования).</span><span class="sxs-lookup"><span data-stu-id="02d9a-159">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table.</span></span> <span data-ttu-id="02d9a-160">При добавлении записи сумма пожертвований добавляется в поле DonationsReceived таблицы Campaigns (Кампании) и TotalDonatedField таблицы Donors (Спонсоры).</span><span class="sxs-lookup"><span data-stu-id="02d9a-160">When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="02d9a-161">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="02d9a-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="02d9a-162">Чтобы просмотреть этот пример в конструкторе макросов, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="02d9a-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="02d9a-163">Откройте таблицу, для которой нужно записать событие **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="02d9a-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="02d9a-164">На вкладке **Таблица** в группе **После событий** щелкните **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="02d9a-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="02d9a-165">Выделите код в следующем примере и нажмите клавиши CTRL+C, чтобы скопировать его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="02d9a-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="02d9a-166">Активируйте окно конструктора макросов и нажмите клавиши CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="02d9a-166">Activate the macro designer window and then press CTRL+V.</span></span>

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
