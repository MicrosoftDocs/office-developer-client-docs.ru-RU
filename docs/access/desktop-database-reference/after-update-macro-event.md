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
# <a name="after-update-macro-event"></a><span data-ttu-id="26af2-102">Событие макроса "После обновления"</span><span class="sxs-lookup"><span data-stu-id="26af2-102">After Update macro event</span></span>

<span data-ttu-id="26af2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26af2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26af2-104">Событие макроса **После обновления** возникает после изменения записи.</span><span class="sxs-lookup"><span data-stu-id="26af2-104">The **After Update** event occurs after a record is changed.</span></span>

> [!NOTE]
> <span data-ttu-id="26af2-105">Событие **После обновления** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="26af2-105">The **After Update** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="26af2-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="26af2-106">Remarks</span></span>

<span data-ttu-id="26af2-107">Используйте событие **После обновления**, чтобы выполнять любые действия, которые должны происходить при изменении записи.</span><span class="sxs-lookup"><span data-stu-id="26af2-107">Use the **After Update** event to perform any actions that you want to occur when a record is changed.</span></span> <span data-ttu-id="26af2-108">Распространенные варианты использования события **После вставки** включают применение бизнес-правил, обновление суммарного итогового значения и отправку уведомлений.</span><span class="sxs-lookup"><span data-stu-id="26af2-108">Common uses for the **After Insert** include enforcing business rules, updating an aggregate total, and sending notifications.</span></span>

<span data-ttu-id="26af2-109">Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле.</span><span class="sxs-lookup"><span data-stu-id="26af2-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="26af2-110">В следующем примере кода показано, как использовать инструкцию **If**, чтобы определить, изменилось ли поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="26af2-110">The following code example shows how to use an **If** statement to determine determine whether the PaidInFull field has been changed.</span></span>

```vb 
 
If  Updated("PaidInFull")   Then 
 
    /* Perform actions based on changes to the field.   */ 
 
End If 
 
```

<span data-ttu-id="26af2-111">Можно использовать доступ к предыдущему значению в поле с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="26af2-111">You can use access a the previous value in a field by using the following syntax.</span></span>

`[Old].[Field Name]`

<span data-ttu-id="26af2-112">Например, для доступа к предыдущему значению поля QuantityInStock используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="26af2-112">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

`[Old].[QuantityInStock]`

<span data-ttu-id="26af2-113">Предыдущие значения удаляются без возможности восстановления при завершении события **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="26af2-113">The previous values are deleted permanently when the **After Update** event ends.</span></span>

<span data-ttu-id="26af2-114">В следующей таблице перечислены макрокоманды, которые можно использовать в событии **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="26af2-114">The following table lists macro commands can be used in the**After Update** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26af2-115">Тип команды</span><span class="sxs-lookup"><span data-stu-id="26af2-115">Command type</span></span></p></th>
<th><p><span data-ttu-id="26af2-116">Команда</span><span class="sxs-lookup"><span data-stu-id="26af2-116">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26af2-117">Управление</span><span class="sxs-lookup"><span data-stu-id="26af2-117">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="26af2-118"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-118"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-119">Управление</span><span class="sxs-lookup"><span data-stu-id="26af2-119">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="26af2-120"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-120"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-121">Управление</span><span class="sxs-lookup"><span data-stu-id="26af2-121">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="26af2-122"><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></span><span class="sxs-lookup"><span data-stu-id="26af2-122"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-123">Блок данных</span><span class="sxs-lookup"><span data-stu-id="26af2-123">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="26af2-124"><a href="createrecord-data-block.md">Макрокоманда "СоздатьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-124"><a href="createrecord-data-block.md">CreateRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-125">Блок данных</span><span class="sxs-lookup"><span data-stu-id="26af2-125">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="26af2-126"><a href="editrecord-data-block.md">Макрокоманда "ИзменитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-126"><a href="editrecord-data-block.md">EditRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-127">Блок данных</span><span class="sxs-lookup"><span data-stu-id="26af2-127">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="26af2-128"><a href="foreachrecord-data-block.md">Макрокоманда "ДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-128"><a href="foreachrecord-data-block.md">ForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-129">Блок данных</span><span class="sxs-lookup"><span data-stu-id="26af2-129">LookupRecord Data Block</span></span></p></td>
<td><p><span data-ttu-id="26af2-130"><a href="lookuprecord-data-block.md">Блок данных "НайтиЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-130"><a href="lookuprecord-data-block.md">LookupRecord Data Block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-131">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-131">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-132"><a href="cancelrecordchange-macro-action.md">Макрокоманда "ОтменитьИзменениеЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-132"><a href="cancelrecordchange-macro-action.md">CancelRecordChange macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-133">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-133">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-134"><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-134"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-135">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-135">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-136"><a href="deleterecord-macro-action.md">Макрокоманда "УдалитьЗапись"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-136"><a href="deleterecord-macro-action.md">DeleteRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-137">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-137">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-138"><a href="exitforeachrecord-macro-action.md">Макрокоманда "ВыходДляКаждойЗаписи"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-138"><a href="exitforeachrecord-macro-action.md">ExitForEachRecord macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-139">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-139">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-140"><a href="logevent-macro-action.md">Макрокоманда "РегистрацияСобытия"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-140"><a href="logevent-macro-action.md">LogEvent macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-141">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-141">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-142"><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-142"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-143">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-143">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-144"><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-144"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-145">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-145">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-146"><a href="rundatamacro-macro-action.md">Макрокоманда "ЗапускМакросаДанных"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-146"><a href="rundatamacro-macro-action.md">RunDataMacro macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-147">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-147">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-148"><a href="sendemail-macro-action.md">Макрокоманда "ОтправитьПочту"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-148"><a href="sendemail-macro-action.md">SendEmail macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-149">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-149">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-150"><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-150"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-151">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-151">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-152"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-152"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26af2-153">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-153">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-154"><a href="stopallmacros-macro-action.md">Макрокоманда "ОстановитьВсеМакросы"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-154"><a href="stopallmacros-macro-action.md">StopAllMacros macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26af2-155">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="26af2-155">Data Action</span></span></p></td>
<td><p><span data-ttu-id="26af2-156"><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></span><span class="sxs-lookup"><span data-stu-id="26af2-156"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="26af2-157">Чтобы создать макрос данных, который записывает событие **После обновления**, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="26af2-157">To create a Data macro that captures the **After Update** event, use the folloiwng steps:</span></span>

1.  <span data-ttu-id="26af2-158">Откройте таблицу, для которой нужно записать событие **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="26af2-158">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="26af2-159">На вкладке **Таблица** в группе **После событий** щелкните **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="26af2-159">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

<span data-ttu-id="26af2-160">В окне конструктора макросов отобразится пустой макрос данных.</span><span class="sxs-lookup"><span data-stu-id="26af2-160">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="26af2-161">Пример</span><span class="sxs-lookup"><span data-stu-id="26af2-161">Example</span></span>

<span data-ttu-id="26af2-162">В следующем примере кода используется событие **После обновления** для запуска именованного макроса данных, добавляющего запись в таблицу Comment (Примечание) при каждом обновлении состояния проблемы.</span><span class="sxs-lookup"><span data-stu-id="26af2-162">The following code example uses the **After Update** event to run a named data macro that adds a record to the Comment table each time the status of an issue is updated.</span></span>

<span data-ttu-id="26af2-163">**Щелкните здесь, чтобы просмотреть копию макроса, который можно вставить в конструктор макросов.**</span><span class="sxs-lookup"><span data-stu-id="26af2-163">**Click here to view a copy of the macro that you can paste into Macro Designer.**</span></span>

<span data-ttu-id="26af2-164">Чтобы просмотреть этот пример в конструкторе макросов, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="26af2-164">To view this example in the macro designer, use the following steps:</span></span>

1.  <span data-ttu-id="26af2-165">Откройте таблицу, для которой нужно записать событие **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="26af2-165">Open the table for which you want to capture the **After Update** event.</span></span>

2.  <span data-ttu-id="26af2-166">На вкладке **Таблица** в группе **После событий** щелкните **После обновления**.</span><span class="sxs-lookup"><span data-stu-id="26af2-166">On the **Table** tab, in the **After Events** group, click **After Update**.</span></span>

3.  <span data-ttu-id="26af2-167">Выделите код в следующем примере и нажмите клавиши CTRL+C, чтобы скопировать его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="26af2-167">Select the code in the following code example and then press CTRL+C to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="26af2-168">Активируйте окно конструктора макросов и нажмите клавиши CTRL+V.</span><span class="sxs-lookup"><span data-stu-id="26af2-168">Activate the macro designer window and then press CTRL+V.</span></span>

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

