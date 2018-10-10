---
title: StopMacro Macro Action
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a918fd128456450c21b5a36e74b7266df661cb75
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481480"
---
# <a name="stopmacro-macro-action"></a><span data-ttu-id="8a6f2-102">StopMacro Macro Action</span><span class="sxs-lookup"><span data-stu-id="8a6f2-102">StopMacro Macro Action</span></span>

<span data-ttu-id="8a6f2-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8a6f2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8a6f2-104">Можно использовать действие **ОстановитьМакрос** Остановка текущего выполняемого макроса.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-104">You can use the **StopMacro** action to stop the currently running macro.</span></span>

## <a name="setting"></a><span data-ttu-id="8a6f2-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="8a6f2-105">Setting</span></span>

<span data-ttu-id="8a6f2-106">Действие **ОстановитьМакрос** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-106">The **StopMacro** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6f2-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a6f2-107">Remarks</span></span>

<span data-ttu-id="8a6f2-108">Это действие обычно используется для остановки макроса при выполнении определенного условия.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-108">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="8a6f2-109">В строке действие макрос, содержащий это действие можно использовать условного выражения.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="8a6f2-110">Когда вычисление выражения дает значение **True** (– 1), Microsoft Access останавливает макрос.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-110">When the expression evaluates to **True** (–1), Microsoft Access stops the macro.</span></span>

<span data-ttu-id="8a6f2-111">Например можно создать макрос, который открывает формы с ежедневного итоговых значений для даты, введенные в настраиваемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-111">For example, you might create a macro that opens a form showing the daily order totals for the date entered in a custom dialog box.</span></span> <span data-ttu-id="8a6f2-112">Чтобы убедиться, что к элементу управления **Дата заказа** на диалоговое окно содержит допустимая дата можно использовать условного выражения.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-112">You could use a conditional expression to be sure that the **Order Date** control on the dialog box contains a valid date.</span></span> <span data-ttu-id="8a6f2-113">В противном случае действие **MessageBox** может отображаться сообщение об ошибке и завершить действие **ОстановитьМакрос** макрос.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the macro.</span></span>

<span data-ttu-id="8a6f2-114">Если макрос действия **эхо** или **УстановитьСообщения** эхо или вывод системных сообщений, действие **ОстановитьМакрос** автоматически включает их обратно.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-114">If the macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopMacro** action automatically turns them back on.</span></span>

<span data-ttu-id="8a6f2-115">Это действие недоступно в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-115">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

## <a name="example"></a><span data-ttu-id="8a6f2-116">Пример</span><span class="sxs-lookup"><span data-stu-id="8a6f2-116">Example</span></span>

<span data-ttu-id="8a6f2-117">Следующий макрос демонстрируется использование **ПриОшибке** .</span><span class="sxs-lookup"><span data-stu-id="8a6f2-117">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="8a6f2-118">В этом примере **ПриОшибке** выполнение доступа обработка макрос с именем ErrorHandler при возникновении ошибки настраиваемых ошибок.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-118">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="8a6f2-119">При возникновении ошибки называется вложенный макрос CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-119">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="8a6f2-120">Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса прекращается.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-120">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="8a6f2-121">В противном случае отображается сообщение об ошибке и макрос приостановлен, поэтому можно выполнить дополнительные настройки.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-121">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="8a6f2-122">Макрос ErrorHandler отображается окно сообщения, на который ссылается на объект **MacroError** для отображения сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="8a6f2-122">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="8a6f2-123">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="8a6f2-123">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
