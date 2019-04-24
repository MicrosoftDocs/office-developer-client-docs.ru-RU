---
title: Макрокоманда StopMacro
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308500"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="ade0d-102">Макрокоманда StopMacro</span><span class="sxs-lookup"><span data-stu-id="ade0d-102">StopMacro macro action</span></span>

<span data-ttu-id="ade0d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ade0d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ade0d-104">Чтобы остановить выполняемый в данный момент макрос, можно использовать действие **Макрокоманда StopMacro** .</span><span class="sxs-lookup"><span data-stu-id="ade0d-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="ade0d-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="ade0d-105">Setting</span></span>

<span data-ttu-id="ade0d-106">Макрокоманда **Макрокоманда StopMacro** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="ade0d-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="ade0d-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="ade0d-107">Remarks</span></span>

<span data-ttu-id="ade0d-108">Обычно это действие используется при условии, что необходимо остановить макрос.</span><span class="sxs-lookup"><span data-stu-id="ade0d-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="ade0d-109">В строке действий макроса, содержащей это действие, можно использовать условное выражение.</span><span class="sxs-lookup"><span data-stu-id="ade0d-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="ade0d-110">Если выражение имеет **значение true** (– 1), макрос будет остановлен.</span><span class="sxs-lookup"><span data-stu-id="ade0d-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="ade0d-111">Например, вы можете создать макрос, который открывает форму, в которой показаны ежедневные итоговые значения для даты, введенной в настраиваемом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="ade0d-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="ade0d-112">Можно использовать условное выражение, чтобы убедиться, что элемент управления " **Дата заказа** " в диалоговом окне содержит допустимую дату.</span><span class="sxs-lookup"><span data-stu-id="ade0d-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="ade0d-113">В противном случае действие **MessageBox** может отобразить сообщение об ошибке, а действие **Макрокоманда StopMacro** может остановить макрос.</span><span class="sxs-lookup"><span data-stu-id="ade0d-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="ade0d-114">Если в макросе используются действия **echo** или **сетварнингс** , чтобы включить эхо или отображение системных сообщений, действие **Макрокоманда StopMacro** автоматически включает их снова.</span><span class="sxs-lookup"><span data-stu-id="ade0d-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="ade0d-115">Это действие недоступно в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="ade0d-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="ade0d-116">Пример</span><span class="sxs-lookup"><span data-stu-id="ade0d-116">Example</span></span>

<span data-ttu-id="ade0d-117">В следующем макросе показано использование действия **OnError** .</span><span class="sxs-lookup"><span data-stu-id="ade0d-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="ade0d-118">В этом примере действие **OnError** указывает, что Access выполняет макрос обработки настраиваемых ошибок с именем ErrorHandler при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="ade0d-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="ade0d-119">При возникновении ошибки вызывается вложенный макрос Катчеррорс.</span><span class="sxs-lookup"><span data-stu-id="ade0d-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="ade0d-120">Если номер ошибки 2102, отображается конкретное сообщение, а выполнение макроса приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="ade0d-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="ade0d-121">В противном случае отображается сообщение об ошибке, и макрос приостанавливается, чтобы можно было выполнить дополнительные действия по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="ade0d-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="ade0d-122">В макросе ErrorHandler отображается окно сообщения, которое ссылается на объект **MacroError** , чтобы отобразить сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ade0d-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="ade0d-123">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="ade0d-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
