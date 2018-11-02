---
title: Событие макроса After Insert
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
ms.openlocfilehash: 4dc9d509dedfb74769c84f44a6237b9f6354dc16
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921686"
---
# <a name="after-insert-macro-event"></a><span data-ttu-id="3d4c1-102">Событие макроса After Insert</span><span class="sxs-lookup"><span data-stu-id="3d4c1-102">After Insert macro event</span></span>


<span data-ttu-id="3d4c1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d4c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d4c1-104">**После вставки** событие происходит после добавления записи.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-104">The **After Insert** event occurs after a record is added.</span></span>


> [!NOTE]
> <span data-ttu-id="3d4c1-105">События **После вставки** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-105">The **After Insert** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="3d4c1-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="3d4c1-106">Remarks</span></span>

<span data-ttu-id="3d4c1-107">Событие **После вставки** используется для выполнения действий, которые должны происходить при добавлении записи в таблицу.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-107">Use the **After Insert** event to perform any actions that you want to occur when a record is added to a table.</span></span> <span data-ttu-id="3d4c1-108">Чаще всего используется **После вставки** включают применение бизнес-правил, рабочие процессы, обновление общую сумму и отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-108">Common uses for the **After Insert** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="3d4c1-109">Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** .</span><span class="sxs-lookup"><span data-stu-id="3d4c1-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="3d4c1-110">В следующем примере кода показано, как использовать, **Если** оператор, чтобы определить, определить, были ли изменены в поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="3d4c1-111">В следующей таблице перечислены команды макросов, которые можно использовать в событии**После вставки** .</span><span class="sxs-lookup"><span data-stu-id="3d4c1-111">The following table lists macro commands that can be used in the**After Insert** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3d4c1-112">Тип команды</span><span class="sxs-lookup"><span data-stu-id="3d4c1-112">Command Type</span></span></p></th>
<th><p><span data-ttu-id="3d4c1-113">Команда</span><span class="sxs-lookup"><span data-stu-id="3d4c1-113">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-114">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="3d4c1-114">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-115"><a href="comment-macro-statement.md">Оператор макроса Comment</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-115"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-116">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="3d4c1-116">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-117"><a href="group-macro-statement.md">Оператор макроса Group</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-117"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-118">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="3d4c1-118">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-119"><a href="if-then-else-macro-block.md">Блок макросов If...Then...Else</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-119"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-120">Блок данных</span><span class="sxs-lookup"><span data-stu-id="3d4c1-120">Data Block</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-121"><a href="createrecord-data-block.md">Действия макроса СоздатьЗапись</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-121"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-122">Блок данных</span><span class="sxs-lookup"><span data-stu-id="3d4c1-122">Data Block</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-123"><a href="editrecord-data-block.md">Действия макроса ИзменитьЗапись</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-123"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-124">Блок данных</span><span class="sxs-lookup"><span data-stu-id="3d4c1-124">Data Block</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-125"><a href="foreachrecord-data-block.md">Действия макроса ДляКаждойЗаписи</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-125"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-126">Блок данных</span><span class="sxs-lookup"><span data-stu-id="3d4c1-126">Data Block</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-127"><a href="lookuprecord-data-block.md">Блок данных макрокомандой НайтиЗапись, после</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-127"><a href="lookuprecord-data-block.md">LookupRecord data block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-128">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-128">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-129"><a href="cancelrecordchange-macro-action.md">Макрокоманда CancelRecordChange</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-129"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-130">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-131"><a href="clearmacroerror-macro-action.md">Макрокоманда ClearMacroError</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-132">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-133"><a href="deleterecord-macro-action.md">Макрокоманда DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-133"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-134">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-135"><a href="exitforeachrecord-macro-action.md">Макрокоманда ExitForEachRecord</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-135"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-136">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-137"><a href="logevent-macro-action.md">Макрокоманда LogEvent</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-137"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-138">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-139"><a href="onerror-macro-action.md">Макрокоманда OnError</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-139"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-140">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-141"><a href="raiseerror-macro-action.md">Макрокоманда RaiseError</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-141"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-142">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-142">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-143"><a href="rundatamacro-macro-action.md">Макрокоманда RunDataMacro</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-143"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-144">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-144">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-145"><a href="sendemail-macro-action.md">Макрокоманда SendEmail</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-145"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-146">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-146">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-147"><a href="setfield-macro-action.md">Макрокоманда SetField</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-147"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-148">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-148">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-149"><a href="setlocalvar-macro-action.md">Макрокоманда SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-149"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3d4c1-150">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-150">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-151"><a href="stopallmacros-macro-action.md">Макрокоманда StopAllMacros</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-151"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3d4c1-152">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="3d4c1-152">Data Action</span></span></p></td>
<td><p><span data-ttu-id="3d4c1-153"><a href="stopmacro-macro-action.md">Макрокоманда StopMacro</a></span><span class="sxs-lookup"><span data-stu-id="3d4c1-153"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3d4c1-154">Чтобы создать макрос данных, который захватывает событие **После вставки** , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-154">To create a Data macro that captures the **After Insert** event, use the following steps.</span></span>

1.  <span data-ttu-id="3d4c1-155">Откройте таблицу для записи события **После вставки** .</span><span class="sxs-lookup"><span data-stu-id="3d4c1-155">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="3d4c1-156">На вкладке **таблицы** в группе **После событий** щелкните **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-156">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

<span data-ttu-id="3d4c1-157">Макрос пустой данных отображается в конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-157">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="3d4c1-158">Пример</span><span class="sxs-lookup"><span data-stu-id="3d4c1-158">Example</span></span>

<span data-ttu-id="3d4c1-159">В следующем примере кода используется события **После вставки** для обработки некоторых при добавлении записи в таблице пожертвования.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-159">The following code example uses the **After Insert** event to perform some processing when a record is added to the Donations table.</span></span> <span data-ttu-id="3d4c1-160">При добавлении записи объем пожертвования добавляется поле DonationsReceived в таблице кампании и TotalDonatedField в таблице дарители.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-160">When a record is added, the amount of the donation is added to the DonationsReceived field in the Campaigns table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="3d4c1-161">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="3d4c1-161">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="3d4c1-162">Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3d4c1-162">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="3d4c1-163">Откройте таблицу для записи события **После вставки** .</span><span class="sxs-lookup"><span data-stu-id="3d4c1-163">Open the table for which you want to capture the **After Insert** event.</span></span>

2.  <span data-ttu-id="3d4c1-164">На вкладке **таблицы** в группе **После событий** щелкните **После вставки**.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-164">On the **Table** tab, in the **After Events** group, click **After Insert**.</span></span>

3.  <span data-ttu-id="3d4c1-165">Выберите код в следующем примере кода и нажмите клавиши CTRL + C для копирования его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-165">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="3d4c1-166">Активация окно конструктора макросов и нажмите клавиши CTRL + V.</span><span class="sxs-lookup"><span data-stu-id="3d4c1-166">Activate the macro designer window and then press CTRL+V.</span></span>

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
