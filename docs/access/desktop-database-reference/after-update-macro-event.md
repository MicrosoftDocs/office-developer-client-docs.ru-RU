---
title: After Update Macro Event
TOCTitle: After Update Macro Event
ms:assetid: 5213793b-8301-0f18-3a12-4e3764c879ac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193905(v=office.15)
ms:contentKeyID: 48544838
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm85126
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 2927a3ede26487cabf9986b301cfc0617ba155c6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483113"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="47b96-102">After Update Macro Event</span><span class="sxs-lookup"><span data-stu-id="47b96-102">After Update Macro Event</span></span>


<span data-ttu-id="47b96-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="47b96-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="47b96-104">**После обновления** событие происходит после изменения записи.</span><span class="sxs-lookup"><span data-stu-id="47b96-104">The **After Update** event occurs after a record is changed.</span></span>


> [!NOTE]
> <P><span data-ttu-id="47b96-105">Событие <STRONG>После обновления</STRONG> можно использовать только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="47b96-105">The <STRONG>After Update</STRONG> event is available only in Data Macros.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="47b96-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="47b96-106">Remarks</span></span>

<span data-ttu-id="47b96-107">**После обновления** событие используется для выполнения действий, которые следует выполнить при изменении записи.</span><span class="sxs-lookup"><span data-stu-id="47b96-107">Use the **After Update** event to perform any actions that you want to occur when a record is changed.</span></span> <span data-ttu-id="47b96-108">Чаще всего используется **После вставки** включают применение бизнес-правил, обновление общую сумму и отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="47b96-108">Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="47b96-109">Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** .</span><span class="sxs-lookup"><span data-stu-id="47b96-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="47b96-110">В следующем примере кода показано, как использовать, **Если** оператор, чтобы определить, определить, были ли изменены в поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="47b96-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="47b96-111">Можно использовать доступ в предыдущем значение в поле, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="47b96-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="47b96-112">Например чтобы получить доступ к предыдущей значение поля QuantityInStock, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="47b96-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="47b96-113">Предыдущие значения удаляется без возможности восстановления при окончания события **После обновления** .</span><span class="sxs-lookup"><span data-stu-id="47b96-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="47b96-114">В следующей таблице приведены макрос, который можно использовать команды в событие**После обновления** .</span><span class="sxs-lookup"><span data-stu-id="47b96-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47b96-115">Тип команды</span><span class="sxs-lookup"><span data-stu-id="47b96-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="47b96-116">Команда</span><span class="sxs-lookup"><span data-stu-id="47b96-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47b96-117">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="47b96-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="47b96-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="47b96-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-119">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="47b96-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="47b96-120"><a href="group-macro-statement.md">Group Macro Statement</a></span><span class="sxs-lookup"><span data-stu-id="47b96-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-121">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="47b96-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="47b96-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span><span class="sxs-lookup"><span data-stu-id="47b96-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-123">Блок данных</span><span class="sxs-lookup"><span data-stu-id="47b96-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="47b96-124"><a href="createrecord-data-block.md">Действия СоздатьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="47b96-124"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-125">Блок данных</span><span class="sxs-lookup"><span data-stu-id="47b96-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="47b96-126"><a href="editrecord-data-block.md">Действия ИзменитьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="47b96-126"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-127">Блок данных</span><span class="sxs-lookup"><span data-stu-id="47b96-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="47b96-128"><a href="foreachrecord-data-block.md">Действия ДляКаждойЗаписи макроса</a></span><span class="sxs-lookup"><span data-stu-id="47b96-128"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-129">Блок данных</span><span class="sxs-lookup"><span data-stu-id="47b96-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="47b96-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span><span class="sxs-lookup"><span data-stu-id="47b96-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-131">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-134"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-134"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-135">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-136"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-136"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-137">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-139">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-140"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-140"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-141">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-142"><a href="onerror-macro-action.md">OnError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-142"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-143">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-144"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-144"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-145">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-146"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-146"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-147">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-148"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-148"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-149">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-150"><a href="setfield-macro-action.md">SetField Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-150"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-151">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-152"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-152"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47b96-153">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-154"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-154"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47b96-155">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="47b96-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="47b96-156"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span><span class="sxs-lookup"><span data-stu-id="47b96-156"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47b96-157">Чтобы создать макрос данных, который захватывает событие **После обновления** , используйте folloiwng действия:</span><span class="sxs-lookup"><span data-stu-id="47b96-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="47b96-158">Откройте таблицу для записи события **После обновления** .</span><span class="sxs-lookup"><span data-stu-id="47b96-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="47b96-159">На вкладке **таблицы** в группе **После событий** щелкните **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="47b96-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="47b96-160">Макрос пустой данных отображается в конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="47b96-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="47b96-161">Пример</span><span class="sxs-lookup"><span data-stu-id="47b96-161">Example</span></span>

<span data-ttu-id="47b96-162">В следующем примере кода используется событие **После обновления** для запуска именованный макрос данных, который добавляет запись в таблицу Комментарий каждый раз, когда обновляется состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="47b96-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="47b96-163">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="47b96-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="47b96-164">Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="47b96-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="47b96-165">Откройте таблицу для записи события **После обновления** .</span><span class="sxs-lookup"><span data-stu-id="47b96-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="47b96-166">На вкладке **таблицы** в группе **После событий** щелкните **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="47b96-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="47b96-167">Выберите код в следующем примере кода и нажмите клавиши CTRL + C для копирования его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="47b96-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="47b96-168">Активация окно конструктора макросов и нажмите клавиши CTRL + V.</span><span class="sxs-lookup"><span data-stu-id="47b96-168">Activate the macro designer window and then press CTRL+V.</span></span>

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

