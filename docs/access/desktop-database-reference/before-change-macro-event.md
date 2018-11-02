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
ms.openlocfilehash: fb513c83e3956a37da019d762c5fd1e0c92da755
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926565"
---
# <a name="before-change-macro-event"></a><span data-ttu-id="320af-102">Событие макроса Before Change</span><span class="sxs-lookup"><span data-stu-id="320af-102">Before Change macro event</span></span>

<span data-ttu-id="320af-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="320af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="320af-104">Событие **Перед изменение** происходит при изменении записи, но перед сохранением изменений.</span><span class="sxs-lookup"><span data-stu-id="320af-104">The **Before Change** event occurs when a record changes, but before the change is committed.</span></span>

> [!NOTE]
> <span data-ttu-id="320af-105">Событие **Change перед** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="320af-105">The **Before Change** event is available only in Data Macros.</span></span>

## <a name="remarks"></a><span data-ttu-id="320af-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="320af-106">Remarks</span></span>

<span data-ttu-id="320af-107">Изменить с помощью события **До изменения** для выполнения действий, которые следует выполнить перед записью.</span><span class="sxs-lookup"><span data-stu-id="320af-107">Use the **Before Change** event to perform any actions that you want to occur before a record is changed.</span></span> <span data-ttu-id="320af-108">**До изменения** обычно используется для выполнения проверки и повысить пользовательские сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="320af-108">The **Before Change** is commonly used to perform validation and to raise custom error messages.</span></span>

<span data-ttu-id="320af-109">Чтобы определить, изменился ли поле можно использовать функцию **Updated ("*Имя поля*")** .</span><span class="sxs-lookup"><span data-stu-id="320af-109">You can use the **Updated("*Field Name*")** function to determine whether a field has changed.</span></span> <span data-ttu-id="320af-110">В следующем примере кода показано, как использовать оператор **If** для определения, были ли изменены в поле PaidInFull.</span><span class="sxs-lookup"><span data-stu-id="320af-110">The following code example shows how to use an **If** statement to determine whether the PaidInFull field has been changed.</span></span>

```vb
    If  Updated("PaidInFull")   Then 
     
        /* Perform actions based on changes to the field.   */ 
     
    End If 
```

<span data-ttu-id="320af-111">Свойство **IsInsert** определяет ли событие **Перед изменение** было включено путем создания новой записи или изменение существующей записи.</span><span class="sxs-lookup"><span data-stu-id="320af-111">Use the **IsInsert** property to determine whether the **Before Change** event was triggered by a new record being created or a change to an existing record.</span></span> <span data-ttu-id="320af-112">Они **IsInsert** свойство содержит **значение True** , если событие было вызвано **новую запись** , если событие было вызвано изменение существующей записи en.</span><span class="sxs-lookup"><span data-stu-id="320af-112">They **IsInsert** property contains **True** if the event was triggered by a new record, **False** if the event was triggered by a change to en existing record.</span></span>

<span data-ttu-id="320af-113">В следующем примере кода показан синтаксис для с помощью свойства **IsInsert** .</span><span class="sxs-lookup"><span data-stu-id="320af-113">The following code example shows the syntax for using the **IsInsert** property.</span></span>

```vb
    If   [IsInsert] = True   Then 
     
       /*  Actions for validating a new record go here.       */ 
     
    Else 
     
       /* Actions for processing a changed record go here.    */ 
     
    End If
```

<span data-ttu-id="320af-114">Можно использовать доступ в предыдущем значение в поле, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="320af-114">You can use access a the previous value in a field by using the following syntax.</span></span>

```vb
    [Old].[Field Name]
```

<span data-ttu-id="320af-115">Например чтобы получить доступ к предыдущей значение поля QuantityInStock, используйте следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="320af-115">For example, to access the previous value of the QuantityInStock field, use the following syntax.</span></span>

```vb
    [Old].[QuantityInStock]
```

<span data-ttu-id="320af-116">Предыдущие значения удаляется без возможности восстановления при окончания события **До изменения** .</span><span class="sxs-lookup"><span data-stu-id="320af-116">The previous values are deleted permanently when the **Before Change** event ends.</span></span>

<span data-ttu-id="320af-117">С помощью действия **RaiseError** можно отменить событие **До изменения** .</span><span class="sxs-lookup"><span data-stu-id="320af-117">You can cancel the **Before Change** event by using the **RaiseError** action.</span></span> <span data-ttu-id="320af-118">При возникновении ошибки изменения, содержащиеся в событии **До изменения** будут удалены.</span><span class="sxs-lookup"><span data-stu-id="320af-118">When an error is raised the changes contained in the **Before Change** event are discarded.</span></span>

<span data-ttu-id="320af-119">В следующей таблице перечислены команды макросов, которые можно использовать в событии**До изменения** .</span><span class="sxs-lookup"><span data-stu-id="320af-119">The following table lists macro commands that can be used in the**Before Change** event.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="320af-120">Тип команды</span><span class="sxs-lookup"><span data-stu-id="320af-120">Command Type</span></span></p></th>
<th><p><span data-ttu-id="320af-121">Команда</span><span class="sxs-lookup"><span data-stu-id="320af-121">Command</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="320af-122">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="320af-122">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="320af-123"><a href="comment-macro-statement.md">Оператор макроса Comment</a></span><span class="sxs-lookup"><span data-stu-id="320af-123"><a href="comment-macro-statement.md">Comment macro statement</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="320af-124">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="320af-124">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="320af-125"><a href="group-macro-statement.md">Оператор макроса Group</a></span><span class="sxs-lookup"><span data-stu-id="320af-125"><a href="group-macro-statement.md">Group macro statement</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="320af-126">Выполнение программы</span><span class="sxs-lookup"><span data-stu-id="320af-126">Program Flow</span></span></p></td>
<td><p><span data-ttu-id="320af-127"><a href="if-then-else-macro-block.md">Блок макросов If...Then...Else</a></span><span class="sxs-lookup"><span data-stu-id="320af-127"><a href="if-then-else-macro-block.md">If...Then...Else macro block</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="320af-128">Блок данных</span><span class="sxs-lookup"><span data-stu-id="320af-128">Data Block</span></span></p></td>
<td><p><span data-ttu-id="320af-129"><a href="lookuprecord-data-block.md">Макрокомандой НайтиЗапись, после действия макроса</a></span><span class="sxs-lookup"><span data-stu-id="320af-129"><a href="lookuprecord-data-block.md">LookupRecord macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="320af-130">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="320af-130">Data Action</span></span></p></td>
<td><p><span data-ttu-id="320af-131"><a href="clearmacroerror-macro-action.md">Макрокоманда ClearMacroError</a></span><span class="sxs-lookup"><span data-stu-id="320af-131"><a href="clearmacroerror-macro-action.md">ClearMacroError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="320af-132">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="320af-132">Data Action</span></span></p></td>
<td><p><span data-ttu-id="320af-133"><a href="onerror-macro-action.md">Макрокоманда OnError</a></span><span class="sxs-lookup"><span data-stu-id="320af-133"><a href="onerror-macro-action.md">OnError macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="320af-134">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="320af-134">Data Action</span></span></p></td>
<td><p><span data-ttu-id="320af-135"><a href="raiseerror-macro-action.md">Макрокоманда RaiseError</a></span><span class="sxs-lookup"><span data-stu-id="320af-135"><a href="raiseerror-macro-action.md">RaiseError macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="320af-136">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="320af-136">Data Action</span></span></p></td>
<td><p><span data-ttu-id="320af-137"><a href="setfield-macro-action.md">Макрокоманда SetField</a></span><span class="sxs-lookup"><span data-stu-id="320af-137"><a href="setfield-macro-action.md">SetField macro action</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="320af-138">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="320af-138">Data Action</span></span></p></td>
<td><p><span data-ttu-id="320af-139"><a href="setlocalvar-macro-action.md">Макрокоманда SetLocalVar</a></span><span class="sxs-lookup"><span data-stu-id="320af-139"><a href="setlocalvar-macro-action.md">SetLocalVar macro action</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="320af-140">Действия с данными</span><span class="sxs-lookup"><span data-stu-id="320af-140">Data Action</span></span></p></td>
<td><p><span data-ttu-id="320af-141"><a href="stopmacro-macro-action.md">Макрокоманда StopMacro</a></span><span class="sxs-lookup"><span data-stu-id="320af-141"><a href="stopmacro-macro-action.md">StopMacro macro action</a></span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="320af-142">Чтобы создать макрос данных, который захватывает события **До изменения** , выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="320af-142">To create a Data Macro that captures the **Before Change** event, use the following steps:</span></span>

1.  <span data-ttu-id="320af-143">Откройте таблицу для записи события **До изменения** .</span><span class="sxs-lookup"><span data-stu-id="320af-143">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="320af-144">На вкладке **таблицы** в группе **Перед событий** щелкните **До изменения**.</span><span class="sxs-lookup"><span data-stu-id="320af-144">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

<span data-ttu-id="320af-145">Макрос пустой данных отображается в конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="320af-145">An empty data macro is displayed in the macro designer.</span></span>

## <a name="example"></a><span data-ttu-id="320af-146">Пример</span><span class="sxs-lookup"><span data-stu-id="320af-146">Example</span></span>

<span data-ttu-id="320af-147">В следующем примере кода используется события **До изменения** для проверки состояния полей.</span><span class="sxs-lookup"><span data-stu-id="320af-147">The following code example uses the **Before Change** event to validate the Status fields.</span></span> <span data-ttu-id="320af-148">Если содержится неверное значение в поле разрешения, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="320af-148">An error is raised if an inappropriate value is contained in the Resolution field.</span></span>

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

<span data-ttu-id="320af-149">Чтобы просмотреть в этом примере в конструктор макросов, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="320af-149">To view this example in the macro designer, use the following steps.</span></span>

1.  <span data-ttu-id="320af-150">Откройте таблицу для записи события **До изменения** .</span><span class="sxs-lookup"><span data-stu-id="320af-150">Open the table for which you want to capture the **Before Change** event.</span></span>

2.  <span data-ttu-id="320af-151">На вкладке **таблицы** в группе **Перед событий** щелкните **До изменения**.</span><span class="sxs-lookup"><span data-stu-id="320af-151">On the **Table** tab, in the **Before Events** group, click **Before Change**.</span></span>

3.  <span data-ttu-id="320af-152">Выберите код в следующем примере кода и нажмите **Клавиши CTRL + C** для копирования его в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="320af-152">Select the code in the following code example and then press **CTRL+C** to copy it to the Clipboard.</span></span>

4.  <span data-ttu-id="320af-153">Активация окно конструктора макросов и нажмите клавиши **CTRL + V**.</span><span class="sxs-lookup"><span data-stu-id="320af-153">Activate the macro designer window and then press **CTRL+V**.</span></span>



```xml
<DataMacros xmlns="https://schemas.microsoft.com/office/accessservices/2009/04/application"> 
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

<span data-ttu-id="320af-154">Следующем примере показано, как использовать действие RaiseError для отмены события макрос данных до изменения.</span><span class="sxs-lookup"><span data-stu-id="320af-154">The following example shows how to use the RaiseError action to cancel the Before Change data macro event.</span></span> <span data-ttu-id="320af-155">При обновлении поля Кому назначено блок данных макрокомандой НайтиЗапись, после используется для определения, назначенный технического специалиста в настоящее время назначен ли запроса на открытие службы.</span><span class="sxs-lookup"><span data-stu-id="320af-155">When the AssignedTo field is updated, a LookupRecord data block is used to determine whether the assigned technician is currently assigned to an open service request.</span></span> <span data-ttu-id="320af-156">Если это так, затем отмене события до изменения и запись не обновляется.</span><span class="sxs-lookup"><span data-stu-id="320af-156">If this is true, then the Before Change event is cancelled and the record is not updated.</span></span>

<span data-ttu-id="320af-157">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="320af-157">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
