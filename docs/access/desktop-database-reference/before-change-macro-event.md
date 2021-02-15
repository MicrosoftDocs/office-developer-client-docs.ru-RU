---
title: Событие макроса Before Change
TOCTitle: Before Change macro event
ms:assetid: da456d55-a773-abeb-1fac-ef58e3331cb5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835322(v=office.15)
ms:contentKeyID: 48548077
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm19867
dev_langs:
- xml
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a180068e805ae11883822ebf26f924e10d34bac5
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538118"
---
# <a name="before-change-macro-event"></a><span data-ttu-id="f8fbc-102">Событие макроса Before Change</span><span class="sxs-lookup"><span data-stu-id="f8fbc-102">Before Change macro event</span></span>

<span data-ttu-id="f8fbc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f8fbc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8fbc-104">Событие **Before Change** возникает при изменении записи, но до его фиксии.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="f8fbc-105">Событие **"До изменения"** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-105">The **Before Change** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8fbc-106">Заметки</span><span class="sxs-lookup"><span data-stu-id="f8fbc-106">Remarks</span></span>

<span data-ttu-id="f8fbc-107">Используйте событие **Before Change** для выполнения любых действий, которые необходимо выполнить перед изменением записи.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-107">Use the **Before Change** event to perform any actions that you want to occur before a record is changed.</span></span> <span data-ttu-id="f8fbc-108">Обычно **перед изменением** выполняется проверка и вызываются пользовательские сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="f8fbc-109">Вы можете использовать функцию **Updated("*Имя поля*")**, чтобы определить, изменилось ли поле.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="f8fbc-110">В следующем примере кода показано, как использовать выписку **If,** чтобы определить, было ли изменено поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-110">The following code example shows how to use an **If** statement to determine whether the PaidInFull field has been changed.</span></span>

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

<span data-ttu-id="f8fbc-111">Используйте свойство **IsInsert,** чтобы определить, вызвано ли событие **before Change** новой записью или изменением существующей записи.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-111">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record.</span></span> <span data-ttu-id="f8fbc-112">Свойство **IsInsert содержит** свойство **True,** если событие вызвано новой записью, **False,** если событие вызвано изменением существующей записи.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-112">They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span></span>

<span data-ttu-id="f8fbc-113">В следующем примере кода показан синтаксис для использования свойства **IsInsert.**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-113">The following code example shows the syntax for using the **IsInsert** property.</span></span>

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

<span data-ttu-id="f8fbc-114">Можно использовать доступ к предыдущему значению в поле с помощью следующего синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-114">You can use access a the previous value in a field by using the following syntax.</span></span>

```vb
    [Old].[Field Name]
```

<span data-ttu-id="f8fbc-115">Например, для доступа к предыдущему значению поля QuantityInStock используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-115">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

```vb
    [Old].[QuantityInStock]
```

<span data-ttu-id="f8fbc-116">Предыдущие значения удаляются окончательно после окончания события **"До** изменения".</span><span class="sxs-lookup"><span data-stu-id="f8fbc-116">The previous values are deleted permanently when the **Before Change** event ends.</span></span>

<span data-ttu-id="f8fbc-117">Событие "До **изменения"** можно отменить с помощью действия **RaiseError.**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-117">You can cancel the **Before Change** event by using the **RaiseError** action.</span></span> <span data-ttu-id="f8fbc-118">При ошибке изменения, содержащиеся в событии **before Change,** удаляются.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-118">When an error is raised the changes contained in the **Before Change** event are discarded.</span></span>

<span data-ttu-id="f8fbc-119">В следующей таблице перечислены команды макроса, которые можно использовать в событии **before Change.**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-119">The following table lists macro commands that can be used in the **Before Change** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f8fbc-120">Тип команды</span><span class="sxs-lookup"><span data-stu-id="f8fbc-120">Command Type</span></span></p></th>
<th><p><span data-ttu-id="f8fbc-121">Команда</span><span class="sxs-lookup"><span data-stu-id="f8fbc-121">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f8fbc-122">Управление</span><span class="sxs-lookup"><span data-stu-id="f8fbc-122">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-123"><a href="comment-macro-statement.md">Оператор макроса "Примечание"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fbc-124">Управление</span><span class="sxs-lookup"><span data-stu-id="f8fbc-124">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-125"><a href="group-macro-statement.md">Оператор макроса "Группа"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-125"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8fbc-126">Управление</span><span class="sxs-lookup"><span data-stu-id="f8fbc-126">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-127"><a href="if-then-else-macro-block.md">Макроблок Если... То... Иначе</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-127"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fbc-128">Блок данных</span><span class="sxs-lookup"><span data-stu-id="f8fbc-128">Data Block</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-129"><a href="lookuprecord-data-block.md">Макрокод LookupRecord</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-129"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8fbc-130">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="f8fbc-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-131"><a href="clearmacroerror-macro-action.md">Макрокоманда "УстранитьОшибкуМакроса"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fbc-132">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="f8fbc-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-133"><a href="onerror-macro-action.md">Макрокоманда "ПриОшибке"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-133"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8fbc-134">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="f8fbc-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-135"><a href="raiseerror-macro-action.md">Макрокоманда "ВыводОшибки"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-135"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fbc-136">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="f8fbc-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-137"><a href="setfield-macro-action.md">Макрокоманда "ЗадатьПоле"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-137"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f8fbc-138">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="f8fbc-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-139"><a href="setlocalvar-macro-action.md">Макрокоманда "ЗадатьЛокПеременную"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-139"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f8fbc-140">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="f8fbc-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="f8fbc-141"><a href="stopmacro-macro-action.md">Макрокоманда "ОстановитьМакрос"</a></span><span class="sxs-lookup"><span data-stu-id="f8fbc-141"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f8fbc-142">Чтобы создать макрос данных, который захватывает событие **before Change,** с помощью следующих действий:</span><span class="sxs-lookup"><span data-stu-id="f8fbc-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span></span>

1.  <span data-ttu-id="f8fbc-143">Откройте таблицу, для которой необходимо зафиксировать событие **Before Change.**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-143">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="f8fbc-144">На **вкладке "Таблица"** в группе **"События** до" щелкните **"Перед изменением".**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-144">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

<span data-ttu-id="f8fbc-145">В окне конструктора макросов отобразится пустой макрос данных.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-145">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="f8fbc-146">Пример</span><span class="sxs-lookup"><span data-stu-id="f8fbc-146">Example</span></span>

<span data-ttu-id="f8fbc-147">В следующем примере кода для проверки полей состояния используется событие Before **Change.**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-147">The following code example uses the **Before Change** event to validate the Status fields.</span></span> <span data-ttu-id="f8fbc-148">Если в поле "Разрешение" содержится недопустимое значение, вызывается ошибка.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-148">An error is raised if an inappropriate value is contained in the Resolution field.</span></span>

```vb 
 
/* Check to ensure that if the bug is resloved that the user has selected a resolution      */ 
If   [Status]="3 - Resolved" And IsNull([Resolution])   Then 
 
     RaiseError 
             Error Number   1 
        Error Description   You must select a resolution. 
End If 
 
/* Check to ensure that if a bug is closed that the user has selected a resolution first     */ 
If   [Status]="4 - Closed" And IsNull([Resolution])   Then 
 
      RaiseError 
             Error Number   2 
        Error Description   An issue must be resolved before it can be closed. 
End If 
 
If   [Status]<>"3 - Resolved" And [Status]<>"4 - Closed"   Then 
 
      SetField 
             Name   Resolution 
            Value   =Null 
End If 
 
```

<span data-ttu-id="f8fbc-149">Чтобы просмотреть этот пример в конструкторе макроса, с помощью следующих действий.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-149">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="f8fbc-150">Откройте таблицу, для которой необходимо зафиксировать событие **Before Change.**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-150">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="f8fbc-151">На **вкладке "Таблица"** в группе **"События** до" щелкните **"Перед изменением".**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-151">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

3.  <span data-ttu-id="f8fbc-152">Выберите код в следующем примере кода и нажмите **CTRL+C,** чтобы скопировать его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-152">Select the code in the following code example and then press **CTRL+C** to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="f8fbc-153">Активируйте окно конструктора макроса и нажмите **CTRL+V.**</span><span class="sxs-lookup"><span data-stu-id="f8fbc-153">Activate the macro designer window and then press **CTRL+V**.</span></span>



```xml
<DataMacros xmlns="http://schemas.microsoft.com/office/accessservices/2009/04/application"> 
  <DataMacro Event="BeforeChange"> 
    <Statements> 
      <Comment>Check to ensure that if the bug is resloved that the user has selected a resolution </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="3 - Resolved" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">1</Argument> 
              <Argument Name="Description">You must select a resolution.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <Comment>Check to ensure that if a bug is closed that the user has selected a resolution first </Comment> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]="4 - Closed" And IsNull([Resolution])</Condition> 
          <Statements> 
            <Action Name="RaiseError"> 
              <Argument Name="Number">2</Argument> 
              <Argument Name="Description">An issue must be resolved before it can be closed.</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
      <ConditionalBlock> 
        <If> 
          <Condition>[Status]&lt;&gt;"3 - Resolved" And [Status]&lt;&gt;"4 - Closed"</Condition> 
          <Statements> 
            <Action Name="SetField"> 
              <Argument Name="Field">Resolution</Argument> 
              <Argument Name="Value">Null</Argument> 
            </Action> 
          </Statements> 
        </If> 
      </ConditionalBlock> 
    </Statements> 
  </DataMacro> 
</DataMacros>
```

<span data-ttu-id="f8fbc-154">В следующем примере показано, как использовать действие RaiseError для отмены события макроса данных "Перед изменением".</span><span class="sxs-lookup"><span data-stu-id="f8fbc-154">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="f8fbc-155">При обновлении поля AssignedTo блок данных LookupRecord используется для определения того, назначен ли техники в настоящее время открытый запрос на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-155">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="f8fbc-156">Если это так, событие before Change отменяется и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="f8fbc-156">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="f8fbc-157">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="f8fbc-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* Get the name of the technician  */
    Look Up A Record In tblTechnicians
        Where Condition =[tblTechnicians].[ID]=[tblServiceRequests].[AssignedTo]
    SetLocalVar
        Name TechName
        Expression [tblTechnicians].[FirstName] & " " & [tblTechnicians].[LastName]
    /* End LookUpRecord  */
    
    If Updated("AssignedTo") Then
        Look Up A Record In tblServiceRequests
            Where Condition SR.[AssignedTo]=tblServiceRequests[AssignedTo] And 
                SR.[ID]<>tblServiceRequests.[ID] And IsNull(SR.[ActualCompletionDate])
            Alias SR
            RaiseError
                Error Number 1234
                Error Description ="Cannot assign a request to the specified technician: " & [TechName]
    
    End If
```
