---
title: Оператор макрос вложенный макрос
TOCTitle: Submacro Macro Statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 379680fc527b3c5165ae5df99dd354b37dfb9322
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910798"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="70a75-102">Оператор макрос вложенный макрос</span><span class="sxs-lookup"><span data-stu-id="70a75-102">Submacro Macro Statement</span></span>

<span data-ttu-id="70a75-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70a75-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70a75-104">Оператор **Вложенный макрос** определяет отдельные макроса в окне конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="70a75-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="70a75-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="70a75-105">Setting</span></span>

<span data-ttu-id="70a75-106">Действие **Вложенный макрос** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="70a75-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="70a75-107">Argument</span><span class="sxs-lookup"><span data-stu-id="70a75-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="70a75-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="70a75-108">Required</span></span></p></th>
<th><p><span data-ttu-id="70a75-109">Описание</span><span class="sxs-lookup"><span data-stu-id="70a75-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="70a75-110">Имя</span><span class="sxs-lookup"><span data-stu-id="70a75-110">Name</span></span></p></td>
<td><p><span data-ttu-id="70a75-111">Да</span><span class="sxs-lookup"><span data-stu-id="70a75-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="70a75-112">Строка, которая отображается как имя макроса.</span><span class="sxs-lookup"><span data-stu-id="70a75-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="70a75-113">Пример</span><span class="sxs-lookup"><span data-stu-id="70a75-113">Example</span></span>

<span data-ttu-id="70a75-114">Следующий макрос демонстрируется использование **ПриОшибке** .</span><span class="sxs-lookup"><span data-stu-id="70a75-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="70a75-115">В этом примере **ПриОшибке** выполнение доступа обработка макрос с именем ErrorHandler при возникновении ошибки настраиваемых ошибок.</span><span class="sxs-lookup"><span data-stu-id="70a75-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="70a75-116">При возникновении ошибки называется вложенный макрос CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="70a75-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="70a75-117">Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса прекращается.</span><span class="sxs-lookup"><span data-stu-id="70a75-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="70a75-118">В противном случае отображается сообщение об ошибке и макрос приостановлен, поэтому можно выполнить дополнительные настройки.</span><span class="sxs-lookup"><span data-stu-id="70a75-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="70a75-119">Макрос ErrorHandler отображается окно сообщения, на который ссылается на объект **MacroError** для отображения сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="70a75-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="70a75-120">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="70a75-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
