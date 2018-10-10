---
title: OnError Macro Action
TOCTitle: OnError Macro Action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b27ffa119d37cd7ddf80292acd9a1e1e131b0359
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481244"
---
# <a name="onerror-macro-action"></a><span data-ttu-id="89925-102">OnError Macro Action</span><span class="sxs-lookup"><span data-stu-id="89925-102">OnError Macro Action</span></span>

<span data-ttu-id="89925-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="89925-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89925-104">Чтобы указать, что должно происходить при возникновении ошибки в макросе, можно использовать **ПриОшибке** .</span><span class="sxs-lookup"><span data-stu-id="89925-104">You can use the **OnError** action to specify what should happen when an error occurs in a macro.</span></span>

## <a name="setting"></a><span data-ttu-id="89925-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="89925-105">Setting</span></span>

<span data-ttu-id="89925-106">**ПриОшибке** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="89925-106">The **OnError** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89925-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="89925-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="89925-108">Описание</span><span class="sxs-lookup"><span data-stu-id="89925-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89925-109">Перейти к разделу</span><span class="sxs-lookup"><span data-stu-id="89925-109">Go to</span></span></p></td>
<td><p><span data-ttu-id="89925-110">Укажите общее поведение, которое должно происходить при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="89925-110">Specify the general behavior that should occur when an error is encountered.</span></span> <span data-ttu-id="89925-111">Щелкните стрелку раскрывающегося списка и выберите один из следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="89925-111">Click the drop-down arrow and then click one of the following settings:</span></span></p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="89925-112">Параметр</span><span class="sxs-lookup"><span data-stu-id="89925-112">Setting</span></span></p></th>
<th><p><span data-ttu-id="89925-113">Описание</span><span class="sxs-lookup"><span data-stu-id="89925-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89925-114"><strong>Далее</strong></span><span class="sxs-lookup"><span data-stu-id="89925-114"><strong>Next</strong></span></span></p></td>
<td><p><span data-ttu-id="89925-115">Microsoft Office Access 2007 записывает сведения об ошибке в объекте <strong>MacroError</strong> , но не останавливается макрос.</span><span class="sxs-lookup"><span data-stu-id="89925-115">Microsoft Office Access 2007 records the details of the error in the <strong>MacroError</strong> object but does not stop the macro.</span></span> <span data-ttu-id="89925-116">Макрос по-прежнему производится с помощью следующего действия.</span><span class="sxs-lookup"><span data-stu-id="89925-116">The macro continues with the next action.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89925-117"><strong>Имя макроса</strong></span><span class="sxs-lookup"><span data-stu-id="89925-117"><strong>Macro Name</strong></span></span></p></td>
<td><p><span data-ttu-id="89925-118">Access останавливает текущего макроса и запускает макрос, который называется в качестве аргумента <strong>Имя макроса</strong> .</span><span class="sxs-lookup"><span data-stu-id="89925-118">Access stops the current macro and runs the macro that is named in the <strong>Macro Name</strong> argument.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89925-119"><strong>Ошибка</strong></span><span class="sxs-lookup"><span data-stu-id="89925-119"><strong>Fail</strong></span></span></p></td>
<td><p><span data-ttu-id="89925-120">Access останавливает текущего макроса и отображает сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="89925-120">Access stops the current macro and displays an error message.</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89925-121">Имя макроса</span><span class="sxs-lookup"><span data-stu-id="89925-121">Macro Name</span></span></p></td>
<td><p><span data-ttu-id="89925-122">Если имя макроса перейти к аргумент, введите имя макроса, которое будет использоваться для обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="89925-122">If the Go to argument is set to Macro Name, type the name of the macro to be used for error handling.</span></span> <span data-ttu-id="89925-123">Имя, введенное должно соответствовать имени в столбце <strong>Имя макроса</strong> текущего макроса; не удается введите имя объекта другого макроса.</span><span class="sxs-lookup"><span data-stu-id="89925-123">The name you type must match a name in the <strong>Macro Name</strong> column of the current macro; you can't enter the name of a different macro object.</span></span> <span data-ttu-id="89925-124">В приведенном ниже примере макрос <strong>ErrorHandler</strong> содержится в один и тот же объект макрос как <strong>ПриОшибке</strong> .</span><span class="sxs-lookup"><span data-stu-id="89925-124">In the example below, the <strong>ErrorHandler</strong> macro is contained in the same macro object as the <strong>OnError</strong> action.</span></span> <span data-ttu-id="89925-125">Этот аргумент должно остаться пустым, если значение перейти к аргумент <strong>следующий</strong> или <strong>с ошибкой</strong>.</span><span class="sxs-lookup"><span data-stu-id="89925-125">This argument must be left blank if the Go to argument is set to <strong>Next</strong> or <strong>Fail</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="89925-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="89925-126">Remarks</span></span>

- <span data-ttu-id="89925-127">**ПриОшибке** обычно размещается в начале макросов, но также можно помещать действие далее в макрос.</span><span class="sxs-lookup"><span data-stu-id="89925-127">The **OnError** action is usually placed at the beginning of a macro, but you can also place the action later in the macro.</span></span> <span data-ttu-id="89925-128">Правила, созданные действие вступят в силу при запуске действия.</span><span class="sxs-lookup"><span data-stu-id="89925-128">The rules established by the action will take effect whenever the action is run.</span></span>

- <span data-ttu-id="89925-129">Если аргумент к **сбою**значение находится вне офиса, Access ведет себя так же, как при не выполнялись никаких действий **OnError** в макрос.</span><span class="sxs-lookup"><span data-stu-id="89925-129">If you set the Go to argument to **Fail**, Access behaves the same way it would if there were no **OnError** action in the macro.</span></span> <span data-ttu-id="89925-130">То есть если обнаружена ошибка, Access останавливает макрос и отображает сообщение об ошибке стандартный.</span><span class="sxs-lookup"><span data-stu-id="89925-130">That is, if an error is encountered, Access stops the macro and displays a standard error message.</span></span> <span data-ttu-id="89925-131">Параметр **с ошибкой** в главном используется для отключения обработки ошибок, установленная ранее в макрос.</span><span class="sxs-lookup"><span data-stu-id="89925-131">The main use for the **Fail** setting is to turn off any error handling that you established earlier in a macro.</span></span>

## <a name="example"></a><span data-ttu-id="89925-132">Пример</span><span class="sxs-lookup"><span data-stu-id="89925-132">Example</span></span>

<span data-ttu-id="89925-133">Следующий макрос демонстрируется использование **ПриОшибке** .</span><span class="sxs-lookup"><span data-stu-id="89925-133">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="89925-134">В этом примере **ПриОшибке** выполнение доступа обработка макрос с именем ErrorHandler при возникновении ошибки настраиваемых ошибок.</span><span class="sxs-lookup"><span data-stu-id="89925-134">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="89925-135">При возникновении ошибки называется вложенный макрос CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="89925-135">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="89925-136">Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса прекращается.</span><span class="sxs-lookup"><span data-stu-id="89925-136">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="89925-137">В противном случае отображается сообщение об ошибке и макрос приостановлен, поэтому можно выполнить дополнительные настройки.</span><span class="sxs-lookup"><span data-stu-id="89925-137">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="89925-138">Макрос ErrorHandler отображается окно сообщения, на который ссылается на объект **MacroError** для отображения сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="89925-138">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="89925-139">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="89925-139">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
