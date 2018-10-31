---
title: После обновления макрос события
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
ms.openlocfilehash: 6c4e854e13527f0c20551950aa49dde30cdae9ab
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862263"
---
# <a name="after-update-macro-event"></a><span data-ttu-id="e17cf-102">После обновления макрос события</span><span class="sxs-lookup"><span data-stu-id="e17cf-102">After Update Macro Event</span></span>


<span data-ttu-id="e17cf-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e17cf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e17cf-104">**После обновления** событие происходит после изменения записи.</span><span class="sxs-lookup"><span data-stu-id="e17cf-104">The **After Update** event occurs after a record is changed.</span></span>


> [!NOTE]
> <span data-ttu-id="e17cf-105">Событие **После обновления** можно использовать только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="e17cf-105">The **After Update** event is available only in Data Macros.</span></span>



## <a name="remarks"></a><span data-ttu-id="e17cf-106">Замечания</span><span class="sxs-lookup"><span data-stu-id="e17cf-106">Remarks</span></span>

<span data-ttu-id="e17cf-107">**После обновления** событие используется для выполнения действий, которые следует выполнить при изменении записи.</span><span class="sxs-lookup"><span data-stu-id="e17cf-107">Use the **After Update** event to perform any actions that you want to occur when a record is changed.</span></span> <span data-ttu-id="e17cf-108">Чаще всего используется **После вставки** включают применение бизнес-правил, обновление общую сумму и отправки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e17cf-108">Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="e17cf-109">Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** .</span><span class="sxs-lookup"><span data-stu-id="e17cf-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="e17cf-110">В следующем примере кода показано, как использовать, **Если** оператор, чтобы определить, определить, были ли изменены в поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="e17cf-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="e17cf-111">Можно использовать доступ в предыдущем значение в поле, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="e17cf-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="e17cf-112">Например чтобы получить доступ к предыдущей значение поля QuantityInStock, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="e17cf-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="e17cf-113">Предыдущие значения удаляется без возможности восстановления при окончания события **После обновления** .</span><span class="sxs-lookup"><span data-stu-id="e17cf-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="e17cf-114">В следующей таблице приведены макрос, который можно использовать команды в событие**После обновления** .</span><span class="sxs-lookup"><span data-stu-id="e17cf-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e17cf-115">Тип команды</span><span class="sxs-lookup"><span data-stu-id="e17cf-115">Command Type</span></span></p></th>
<th><p><span data-ttu-id="e17cf-116">Команда</span><span class="sxs-lookup"><span data-stu-id="e17cf-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-117">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="e17cf-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="e17cf-118"><a href="comment-macro-statement.md">Оператор комментария макросов</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-118"><a href="comment-macro-statement.md">Comment Macro Statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-119">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="e17cf-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="e17cf-120"><a href="group-macro-statement.md">Оператор группы макросов</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-120"><a href="group-macro-statement.md">Group Macro Statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-121">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="e17cf-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="e17cf-122"><a href="if-then-else-macro-block.md">If... Затем... Блок else макросов</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-122"><a href="if-then-else-macro-block.md">If...Then...Else Macro Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-123">Блок данных</span><span class="sxs-lookup"><span data-stu-id="e17cf-123">Data Block</span></span></p></td>
<td><p><span data-ttu-id="e17cf-124"><a href="createrecord-data-block.md">Действия СоздатьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-124"><a href="createrecord-data-block.md">CreateRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-125">Блок данных</span><span class="sxs-lookup"><span data-stu-id="e17cf-125">Data Block</span></span></p></td>
<td><p><span data-ttu-id="e17cf-126"><a href="editrecord-data-block.md">Действия ИзменитьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-126"><a href="editrecord-data-block.md">EditRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-127">Блок данных</span><span class="sxs-lookup"><span data-stu-id="e17cf-127">Data Block</span></span></p></td>
<td><p><span data-ttu-id="e17cf-128"><a href="foreachrecord-data-block.md">Действия ДляКаждойЗаписи макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-128"><a href="foreachrecord-data-block.md">ForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-129">Блок данных</span><span class="sxs-lookup"><span data-stu-id="e17cf-129">Data Block</span></span></p></td>
<td><p><span data-ttu-id="e17cf-130"><a href="lookuprecord-data-block.md">Блок данных LookupRecord</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-131">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-132"><a href="cancelrecordchange-macro-action.md">Действия макроса CancelRecordChange</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-134"><a href="clearmacroerror-macro-action.md">Действия макроса ClearMacroError</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-134"><a href="clearmacroerror-macro-action.md">ClearMacroError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-135">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-136"><a href="deleterecord-macro-action.md">Действия макрокоманду УдалитьЗапись макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-136"><a href="deleterecord-macro-action.md">DeleteRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-137">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-138"><a href="exitforeachrecord-macro-action.md">Действия макроса ExitForEachRecord</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-139">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-140"><a href="logevent-macro-action.md">Действия LogEvent макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-140"><a href="logevent-macro-action.md">LogEvent Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-141">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-142"><a href="onerror-macro-action.md">Действия макроса OnError</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-142"><a href="onerror-macro-action.md">OnError Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-143">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-144"><a href="raiseerror-macro-action.md">Действия макроса RaiseError</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-144"><a href="raiseerror-macro-action.md">RaiseError Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-145">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-146"><a href="rundatamacro-macro-action.md">Действия ЗапускМакросаДанных макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-146"><a href="rundatamacro-macro-action.md">RunDataMacro Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-147">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-148"><a href="sendemail-macro-action.md">Действия макроса sendemail действие</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-148"><a href="sendemail-macro-action.md">SendEmail Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-149">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-150"><a href="setfield-macro-action.md">Действия SetField макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-150"><a href="setfield-macro-action.md">SetField Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-151">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-152"><a href="setlocalvar-macro-action.md">Действия макроса SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-152"><a href="setlocalvar-macro-action.md">SetLocalVar Macro Action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e17cf-153">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-154"><a href="stopallmacros-macro-action.md">Действия ОстановитьВсеМакросы макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-154"><a href="stopallmacros-macro-action.md">StopAllMacros Macro Action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e17cf-155">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="e17cf-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="e17cf-156"><a href="stopmacro-macro-action.md">Действия ОстановитьМакрос макроса</a></span><span class="sxs-lookup"><span data-stu-id="e17cf-156"><a href="stopmacro-macro-action.md">StopMacro Macro Action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e17cf-157">Чтобы создать макрос данных, который захватывает событие **После обновления** , используйте folloiwng действия:</span><span class="sxs-lookup"><span data-stu-id="e17cf-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="e17cf-158">Откройте таблицу для записи события **После обновления** .</span><span class="sxs-lookup"><span data-stu-id="e17cf-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="e17cf-159">На вкладке **таблицы** в группе **После событий** щелкните **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="e17cf-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="e17cf-160">Макрос пустой данных отображается в конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="e17cf-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="e17cf-161">Пример</span><span class="sxs-lookup"><span data-stu-id="e17cf-161">Example</span></span>

<span data-ttu-id="e17cf-162">В следующем примере кода используется событие **После обновления** для запуска именованный макрос данных, который добавляет запись в таблицу Комментарий каждый раз, когда обновляется состояние задачи.</span><span class="sxs-lookup"><span data-stu-id="e17cf-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="e17cf-163">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="e17cf-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="e17cf-164">Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e17cf-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="e17cf-165">Откройте таблицу для записи события **После обновления** .</span><span class="sxs-lookup"><span data-stu-id="e17cf-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="e17cf-166">На вкладке **таблицы** в группе **После событий** щелкните **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="e17cf-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="e17cf-167">Выберите код в следующем примере кода и нажмите клавиши CTRL + C для копирования его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="e17cf-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="e17cf-168">Активация окно конструктора макросов и нажмите клавиши CTRL + V.</span><span class="sxs-lookup"><span data-stu-id="e17cf-168">Activate the macro designer window and then press CTRL+V.</span></span>

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

