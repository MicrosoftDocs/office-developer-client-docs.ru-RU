---
title: После удаления макроса события
TOCTitle: After Delete Macro Event
ms:assetid: ecf9e6d4-345f-9b78-eb36-bd526e5df09b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836323(v=office.15)
ms:contentKeyID: 48548527
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm15155
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b180acb99ab2ac406a7b60fdecf8aff5d63eb71f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869115"
---
# <a name="after-delete-macro-event"></a><span data-ttu-id="6e056-102">После удаления макроса события</span><span class="sxs-lookup"><span data-stu-id="6e056-102">After Delete Macro Event</span></span>


<span data-ttu-id="6e056-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e056-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e056-104">**После удаления** событие происходит после удаления записи.</span><span class="sxs-lookup"><span data-stu-id="6e056-104">The **After Delete** event occurs after a record is deleted.</span></span>


> [!NOTE]
> <span data-ttu-id="6e056-105">События **После удаления** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="6e056-105">The **After Delete** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="6e056-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="6e056-106">Remarks</span></span>

<span data-ttu-id="6e056-107">Событие **После удаления** используется для выполнения действий, которые должны происходить при удалении записи.</span><span class="sxs-lookup"><span data-stu-id="6e056-107">Use the **After Delete** event to perform any actions that you want to occur when a record is deleted.</span></span> <span data-ttu-id="6e056-108">Чаще всего используется **После удаления** включают применение бизнес-правил, рабочие процессы, обновление общую сумму и отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6e056-108">Common uses for the **After Delete** include enforcing business rules, workflows, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="6e056-109">При возникновении события **После удаления** значения, содержащиеся в удаленной записи все еще доступны.</span><span class="sxs-lookup"><span data-stu-id="6e056-109">When the **After Delete** event occurs, the values contained in the deleted record are still available.</span></span> <span data-ttu-id="6e056-110">Можно использовать удаленные значение для увеличения или уменьшения всего, аудита или сравнить существующее значение аргумента *WhereCondition* .</span><span class="sxs-lookup"><span data-stu-id="6e056-110">You may want to use a deleted value to increment or decrement a total, create an audit trail, or compare to an existing value in a *WhereCondition* argument.</span></span>

<span data-ttu-id="6e056-111">Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** .</span><span class="sxs-lookup"><span data-stu-id="6e056-111">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="6e056-112">В следующем примере кода показано, как использовать выражение If staement, чтобы определить, определить, были ли изменены в поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="6e056-112">The following code example shows how to use an If staement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="6e056-113">Можно использовать доступа значение в удаленной записи, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6e056-113">You can use access a value in the deleted record by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="6e056-114">Например для доступа к значению поля QuantityInStock в удаленной записи, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="6e056-114">For example, to access the value of the QuantityInStock field in the deleted record, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="6e056-115">Значения, содержащиеся в удаленную запись удаляется без возможности восстановления при окончания события **После удаления** .</span><span class="sxs-lookup"><span data-stu-id="6e056-115">The values contained in the deleted record are deleted permanently when the **After Delete** event ends.</span></span>

<span data-ttu-id="6e056-116">Приведенные ниже команды макрос можно использовать в событии **После удаления** .</span><span class="sxs-lookup"><span data-stu-id="6e056-116">The following macro commands can be used in the **After Delete** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e056-117">Тип команды</span><span class="sxs-lookup"><span data-stu-id="6e056-117">Command Type</span></span></p></th>
<th><p><span data-ttu-id="6e056-118">Команда</span><span class="sxs-lookup"><span data-stu-id="6e056-118">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e056-119">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="6e056-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="6e056-120"><a href="comment-macro-statement.md">Оператор комментария макросов</a></span><span class="sxs-lookup"><span data-stu-id="6e056-120"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-121">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="6e056-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="6e056-122"><a href="group-macro-statement.md">Оператор группы макросов</a></span><span class="sxs-lookup"><span data-stu-id="6e056-122"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-123">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="6e056-123">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="6e056-124"><a href="if-then-else-macro-block.md">If... Затем... Блок else макросов</a></span><span class="sxs-lookup"><span data-stu-id="6e056-124"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-125">Блок данных</span><span class="sxs-lookup"><span data-stu-id="6e056-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="6e056-126"><a href="createrecord-data-block.md">Действия СоздатьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-126"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-127">Блок данных</span><span class="sxs-lookup"><span data-stu-id="6e056-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="6e056-128"><a href="editrecord-data-block.md">Действия ИзменитьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-128"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-129">Блок данных</span><span class="sxs-lookup"><span data-stu-id="6e056-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="6e056-130"><a href="foreachrecord-data-block.md">Действия ДляКаждойЗаписи макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-130"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-131">Блок данных</span><span class="sxs-lookup"><span data-stu-id="6e056-131">Data Block</span></span></p></td>
<td><p><span data-ttu-id="6e056-132"><a href="lookuprecord-data-block.md">Блок данных LookupRecord</a></span><span class="sxs-lookup"><span data-stu-id="6e056-132"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-134"><a href="cancelrecordchange-macro-action.md">Действия макроса CancelRecordChange</a></span><span class="sxs-lookup"><span data-stu-id="6e056-134"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-135">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-136"><a href="clearmacroerror-macro-action.md">Действия макроса ClearMacroError</a></span><span class="sxs-lookup"><span data-stu-id="6e056-136"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-137">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-138"><a href="deleterecord-macro-action.md">Действия макрокоманду УдалитьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-138"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-139">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-140"><a href="exitforeachrecord-macro-action.md">Действия макроса ExitForEachRecord</a></span><span class="sxs-lookup"><span data-stu-id="6e056-140"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-141">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-142"><a href="logevent-macro-action.md">Действия LogEvent макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-142"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-143">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-144"><a href="onerror-macro-action.md">Действия макроса OnError</a></span><span class="sxs-lookup"><span data-stu-id="6e056-144"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-145">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-146"><a href="raiseerror-macro-action.md">Действия макроса RaiseError</a></span><span class="sxs-lookup"><span data-stu-id="6e056-146"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-147">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-148"><a href="rundatamacro-macro-action.md">Действия ЗапускМакросаДанных макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-148"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-149">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-150"><a href="sendemail-macro-action.md">Действия макроса sendemail действие</a></span><span class="sxs-lookup"><span data-stu-id="6e056-150"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-151">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-152"><a href="setfield-macro-action.md">Действия SetField макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-152"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-153">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-154"><a href="setlocalvar-macro-action.md">Действия макроса SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="6e056-154"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e056-155">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-156"><a href="stopallmacros-macro-action.md">Действия ОстановитьВсеМакросы макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-156"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e056-157">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="6e056-157">Data Action</span></span></p></td>
<td><p><span data-ttu-id="6e056-158"><a href="stopmacro-macro-action.md">Действия ОстановитьМакрос макроса</a></span><span class="sxs-lookup"><span data-stu-id="6e056-158"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e056-159">Чтобы создать макрос данных, который захватывает событие **После удаления** , выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6e056-159">To create a Data Macro that captures the **After Delete** event, use the following steps.</span></span>

1.  <span data-ttu-id="6e056-160">Откройте таблицу для записи события **После удаления** .</span><span class="sxs-lookup"><span data-stu-id="6e056-160">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="6e056-161">На вкладке **таблицы** в группе **После событий** щелкните **После удаления**.</span><span class="sxs-lookup"><span data-stu-id="6e056-161">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

<span data-ttu-id="6e056-162">Пустой макрос данных отображается в конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="6e056-162">An empty Data Macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="6e056-163">Пример</span><span class="sxs-lookup"><span data-stu-id="6e056-163">Example</span></span>

<span data-ttu-id="6e056-164">В следующем примере кода используется событие **После удаления** для обработки некоторых при удалении записи из таблицы пожертвования.</span><span class="sxs-lookup"><span data-stu-id="6e056-164">The following code example uses the **After Delete** event to perform some processing when a record is deleted from the Donations table.</span></span> <span data-ttu-id="6e056-165">При удалении записи объем пожертвования — форма subracted DonationsReceived поля в таблице DonationsReceived и TotalDonatedField в таблице дарители.</span><span class="sxs-lookup"><span data-stu-id="6e056-165">When a record is deleted, the amount of the donation is subracted form the DonationsReceived field in the DonationsReceived table and the TotalDonatedField in the Donors table.</span></span>

<span data-ttu-id="6e056-166">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="6e056-166">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="6e056-167">Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6e056-167">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="6e056-168">Откройте таблицу для записи события **После удаления** .</span><span class="sxs-lookup"><span data-stu-id="6e056-168">Open the table for which you want to capture the **After Delete** event.</span></span>

2.  <span data-ttu-id="6e056-169">На вкладке **таблицы** в группе **После событий** щелкните **После удаления**.</span><span class="sxs-lookup"><span data-stu-id="6e056-169">On the **Table** tab, in the **After Events** group, click **After Delete**.</span></span>

3.  <span data-ttu-id="6e056-170">Выберите код, приведенный ниже и нажмите клавиши CTRL + C для копирования его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="6e056-170">Select the code listed below and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="6e056-171">Активация окно конструктора макросов и нажмите клавиши CTRL + V.</span><span class="sxs-lookup"><span data-stu-id="6e056-171">Activate the macro designer window and then press CTRL+V.</span></span>

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
