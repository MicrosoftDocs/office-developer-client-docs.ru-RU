---
title: After Insert Macro Event
TOCTitle: After Insert Macro Event
ms:assetid: 78013896-ee07-6979-96f7-fa0f3490419e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196099(v=office.15)
ms:contentKeyID: 48545742
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3180
f1_categories:
- Office.Version=v15
ms.openlocfilehash: a343c9bb0ea498c3388eb5ce67c3e0692808824c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481013"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="2210c-102">After Insert Macro Event</span><span class="sxs-lookup"><span data-stu-id="2210c-102">After Insert Macro Event</span></span>


<span data-ttu-id="2210c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2210c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2210c-104">**После вставки** событие происходит после добавления записи.</span><span class="sxs-lookup"><span data-stu-id="2210c-104">The **After Insert** event occurs after a record is added.</span></span>


> [!NOTE]
> <span data-ttu-id="2210c-105">События **После вставки** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="2210c-105">The **After Insert** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="2210c-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="2210c-106">Remarks</span></span>

<span data-ttu-id="2210c-107">Событие **После вставки** используется для выполнения действий, которые должны происходить при добавлении записи в таблицу.</span><span class="sxs-lookup"><span data-stu-id="2210c-107">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table.</span></span> <span data-ttu-id="2210c-108">Чаще всего используется **После вставки** включают применение бизнес-правил, рабочие процессы, обновление общую сумму и отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="2210c-108">Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="2210c-109">Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** .</span><span class="sxs-lookup"><span data-stu-id="2210c-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="2210c-110">В следующем примере кода показано, как использовать, **Если** оператор, чтобы определить, определить, были ли изменены в поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="2210c-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="2210c-111">В следующей таблице перечислены команды макросов, которые можно использовать в событии**После вставки** .</span><span class="sxs-lookup"><span data-stu-id="2210c-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2210c-112">Тип команды</span><span class="sxs-lookup"><span data-stu-id="2210c-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="2210c-113">Команда</span><span class="sxs-lookup"><span data-stu-id="2210c-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2210c-114">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="2210c-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2210c-115"><a href="comment-macro-statement.md">Comment Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="2210c-115"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-116">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="2210c-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2210c-117"><a href="group-macro-statement.md">Group Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="2210c-117"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-118">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="2210c-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="2210c-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span><span class="sxs-lookup"><span data-stu-id="2210c-119"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-120">Блок данных</span><span class="sxs-lookup"><span data-stu-id="2210c-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2210c-121"><a href="createrecord-data-block.md">Действия СоздатьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="2210c-121"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-122">Блок данных</span><span class="sxs-lookup"><span data-stu-id="2210c-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2210c-123"><a href="editrecord-data-block.md">Действия ИзменитьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="2210c-123"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-124">Блок данных</span><span class="sxs-lookup"><span data-stu-id="2210c-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2210c-125"><a href="foreachrecord-data-block.md">Действия ДляКаждойЗаписи макроса</a></span><span class="sxs-lookup"><span data-stu-id="2210c-125"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-126">Блок данных</span><span class="sxs-lookup"><span data-stu-id="2210c-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="2210c-127"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span><span class="sxs-lookup"><span data-stu-id="2210c-127"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-128">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-130">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-131"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-131"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-132">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-133"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-133"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-134">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-136">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-137"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-137"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-138">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-139"><a href="onerror-macro-action.md">OnError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-139"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-140">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-141"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-141"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-142">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-143"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-143"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-144">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-145"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-145"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-146">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-147"><a href="setfield-macro-action.md">SetField Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-147"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-148">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-149"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-149"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2210c-150">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-151"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-151"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2210c-152">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="2210c-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="2210c-153"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="2210c-153"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2210c-154">Чтобы создать макрос данных, который захватывает событие **После вставки** , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2210c-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="2210c-155">Откройте таблицу для записи события **После вставки** .</span><span class="sxs-lookup"><span data-stu-id="2210c-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="2210c-156">На вкладке **таблицы** в группе **После событий** щелкните **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="2210c-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="2210c-157">Макрос пустой данных отображается в конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="2210c-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="2210c-158">Пример</span><span class="sxs-lookup"><span data-stu-id="2210c-158">Example</span></span>

<span data-ttu-id="2210c-159">В следующем примере кода используется события **После вставки** для обработки некоторых при добавлении записи в таблице пожертвования.</span><span class="sxs-lookup"><span data-stu-id="2210c-159">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table.</span></span> <span data-ttu-id="2210c-160">При добавлении записи объем пожертвования добавляется поле DonationsReceived в таблице кампании и TotalDonatedField в таблице дарители.</span><span class="sxs-lookup"><span data-stu-id="2210c-160">When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="2210c-161">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="2210c-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="2210c-162">Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2210c-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="2210c-163">Откройте таблицу для записи события **После вставки** .</span><span class="sxs-lookup"><span data-stu-id="2210c-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="2210c-164">На вкладке **таблицы** в группе **После событий** щелкните **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="2210c-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="2210c-165">Выберите код в следующем примере кода и нажмите клавиши CTRL + C для копирования его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="2210c-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="2210c-166">Активация окно конструктора макросов и нажмите клавиши CTRL + V.</span><span class="sxs-lookup"><span data-stu-id="2210c-166">Activate the macro designer window and then press CTRL+V.</span></span>

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
