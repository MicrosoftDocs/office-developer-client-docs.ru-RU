---
title: Макрокоманда OnError
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a2288d64241f3289505a8b0fafb98062830b0e97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288457"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="4b2b2-102">Макрокоманда OnError</span><span class="sxs-lookup"><span data-stu-id="4b2b2-102">OnError macro action</span></span>

<span data-ttu-id="4b2b2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b2b2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b2b2-104">Вы можете использовать действие **OnError** , чтобы указать, что должно происходить при возникновении ошибки в макросе.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="4b2b2-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="4b2b2-105">Setting</span></span>

<span data-ttu-id="4b2b2-106">Действие **OnError** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b2b2-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="4b2b2-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="4b2b2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="4b2b2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b2b2-109">Перейти к разделу</span><span class="sxs-lookup"><span data-stu-id="4b2b2-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="4b2b2-110">Укажите общее поведение, которое должно происходить при обнаружении ошибки.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-110">Specify the general behavior that should occur when an error is encountered.</span></span> <span data-ttu-id="4b2b2-111">Щелкните стрелку раскрывающегося списка и выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="4b2b2-111">Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4b2b2-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="4b2b2-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="4b2b2-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4b2b2-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b2b2-114"><strong>Next</strong></span><span class="sxs-lookup"><span data-stu-id="4b2b2-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="4b2b2-115">Microsoft Office Access 2007 записывает сведения об ошибке в объекте <strong>MacroError</strong> , но не останавливает макрос.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-115">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro.</span></span> <span data-ttu-id="4b2b2-116">Макрос переходит к следующему действию.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-116">The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b2b2-117"><strong>Имя макроса</strong></span><span class="sxs-lookup"><span data-stu-id="4b2b2-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="4b2b2-118">Access применяет текущий макрос и запускает макрос с именем в аргументе <strong>имя макроса</strong> .</span><span class="sxs-lookup"><span data-stu-id="4b2b2-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b2b2-119"><strong>Ошибк</strong></span><span class="sxs-lookup"><span data-stu-id="4b2b2-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="4b2b2-120">Access приостановил текущий макрос и выводит сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b2b2-121">Имя макроса</span><span class="sxs-lookup"><span data-stu-id="4b2b2-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="4b2b2-122">Если аргументу Go присвоено значение имя макроса, введите имя макроса, который будет использоваться для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="4b2b2-123">Введенное имя должно соискать имя в столбце " <strong>имя макроса</strong> " текущего макроса; невозможно ввести имя другого объекта макроса.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="4b2b2-124">В приведенном ниже примере макрос <strong>ErrorHandler</strong> находится в том же объекте макроса, что и <strong></strong> действие OnError.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="4b2b2-125">Этот аргумент должен оставаться пустым, если аргументу Go присвоено значение <strong>Next</strong> или <strong>Fail</strong>.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4b2b2-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="4b2b2-126">Remarks</span></span>

- <span data-ttu-id="4b2b2-127">Действие **OnError** обычно размещается в начале макроса, но вы также можете поместить это действие позже в макрос.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-127">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro.</span></span> <span data-ttu-id="4b2b2-128">Правила, установленные с помощью этого действия, вступят в силу при каждом запуске действия.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-128">The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="4b2b2-129">Если присвоить аргументу Go значение **Failed**, то приложение Access работает так же, как при отсутствии действия OnError в макросе. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="4b2b2-129">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro.</span></span> <span data-ttu-id="4b2b2-130">То есть при возникновении ошибки Access отключает макрос и отображает стандартное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-130">That is, if an error is encountered, Access stops the macro and displays a standard error message.</span></span> <span data-ttu-id="4b2b2-131">Основной способ использования параметра **Fail** — отключить обработку ошибок, установленную ранее в макросе.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-131">The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="4b2b2-132">Пример</span><span class="sxs-lookup"><span data-stu-id="4b2b2-132">Example</span></span>

<span data-ttu-id="4b2b2-133">В следующем макросе показано использование действия **OnError** .</span><span class="sxs-lookup"><span data-stu-id="4b2b2-133">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="4b2b2-134">В этом примере действие **OnError** указывает, что Access выполняет макрос обработки настраиваемых ошибок с именем ErrorHandler при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-134">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="4b2b2-135">При возникновении ошибки вызывается вложенный макрос Катчеррорс.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-135">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="4b2b2-136">Если номер ошибки 2102, отображается конкретное сообщение, а выполнение макроса приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-136">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="4b2b2-137">В противном случае отображается сообщение об ошибке, и макрос приостанавливается, чтобы можно было выполнить дополнительные действия по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-137">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="4b2b2-138">В макросе ErrorHandler отображается окно сообщения, которое ссылается на объект **MacroError** , чтобы отобразить сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4b2b2-138">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="4b2b2-139">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="4b2b2-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
