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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704436"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="6c1c7-102">Макрокоманда StopMacro</span><span class="sxs-lookup"><span data-stu-id="6c1c7-102">StopMacro macro action</span></span>

<span data-ttu-id="6c1c7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c1c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6c1c7-104">Можно использовать действие **ОстановитьМакрос** Остановка текущего выполняемого макроса.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="6c1c7-105">Setting</span><span class="sxs-lookup"><span data-stu-id="6c1c7-105">Setting</span></span>

<span data-ttu-id="6c1c7-106">Действие **ОстановитьМакрос** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c1c7-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="6c1c7-107">Remarks</span></span>

<span data-ttu-id="6c1c7-108">Это действие обычно используется для остановки макроса при выполнении определенного условия.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="6c1c7-109">В строке действие макрос, содержащий это действие можно использовать условного выражения.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="6c1c7-110">Когда вычисление выражения дает значение **True** (– 1), Microsoft Access останавливает макрос.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="6c1c7-111">Например можно создать макрос, который открывает формы с ежедневного итоговых значений для даты, введенные в настраиваемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="6c1c7-112">Чтобы убедиться, что к элементу управления **Дата заказа** на диалоговое окно содержит допустимая дата можно использовать условного выражения.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="6c1c7-113">В противном случае действие **MessageBox** может отображаться сообщение об ошибке и завершить действие **ОстановитьМакрос** макрос.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="6c1c7-114">Если макрос действия **эхо** или **УстановитьСообщения** эхо или вывод системных сообщений, действие **ОстановитьМакрос** автоматически включает их обратно.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="6c1c7-115">Это действие недоступно в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="6c1c7-116">Пример</span><span class="sxs-lookup"><span data-stu-id="6c1c7-116">Example</span></span>

<span data-ttu-id="6c1c7-117">Следующий макрос демонстрируется использование **ПриОшибке** .</span><span class="sxs-lookup"><span data-stu-id="6c1c7-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="6c1c7-118">В этом примере **ПриОшибке** выполнение доступа обработка макрос с именем ErrorHandler при возникновении ошибки настраиваемых ошибок.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="6c1c7-119">При возникновении ошибки называется вложенный макрос CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="6c1c7-120">Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса прекращается.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="6c1c7-121">В противном случае отображается сообщение об ошибке и макрос приостановлен, поэтому можно выполнить дополнительные настройки.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="6c1c7-122">Макрос ErrorHandler отображается окно сообщения, на который ссылается на объект **MacroError** для отображения сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="6c1c7-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="6c1c7-123">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6c1c7-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
