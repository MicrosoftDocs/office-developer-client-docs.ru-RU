---
title: Оператор макроса Submacro
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caabfb0f4e90134c10d5ab728f19e1fd2a4437dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308472"
---
# <a name="submacro-macro-statement"></a><span data-ttu-id="e5f77-102">Оператор макроса Submacro</span><span class="sxs-lookup"><span data-stu-id="e5f77-102">Submacro macro statement</span></span>

<span data-ttu-id="e5f77-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5f77-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e5f77-104">Оператор \*\*\*\* подмакроса определяет отдельный макрос в окне конструктора макросов.</span><span class="sxs-lookup"><span data-stu-id="e5f77-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="e5f77-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="e5f77-105">Setting</span></span>

<span data-ttu-id="e5f77-106">Действие \*\*\*\* вложенного макроса имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e5f77-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e5f77-107">Аргумент</span><span class="sxs-lookup"><span data-stu-id="e5f77-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="e5f77-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e5f77-108">Required</span></span></p></th>
<th><p><span data-ttu-id="e5f77-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e5f77-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5f77-110">Имя</span><span class="sxs-lookup"><span data-stu-id="e5f77-110">Name</span></span></p></td>
<td><p><span data-ttu-id="e5f77-111">Да</span><span class="sxs-lookup"><span data-stu-id="e5f77-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="e5f77-112">Строка, которая отображается как имя макроса.</span><span class="sxs-lookup"><span data-stu-id="e5f77-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="e5f77-113">Пример</span><span class="sxs-lookup"><span data-stu-id="e5f77-113">Example</span></span>

<span data-ttu-id="e5f77-114">В следующем макросе показано использование действия **OnError** .</span><span class="sxs-lookup"><span data-stu-id="e5f77-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="e5f77-115">В этом примере действие **OnError** указывает, что Access выполняет макрос обработки настраиваемых ошибок с именем ErrorHandler при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="e5f77-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="e5f77-116">При возникновении ошибки вызывается вложенный макрос Катчеррорс.</span><span class="sxs-lookup"><span data-stu-id="e5f77-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="e5f77-117">Если номер ошибки 2102, отображается конкретное сообщение, а выполнение макроса приостанавливается.</span><span class="sxs-lookup"><span data-stu-id="e5f77-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="e5f77-118">В противном случае отображается сообщение об ошибке, и макрос приостанавливается, чтобы можно было выполнить дополнительные действия по устранению неполадок.</span><span class="sxs-lookup"><span data-stu-id="e5f77-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="e5f77-119">В макросе ErrorHandler отображается окно сообщения, которое ссылается на объект **MacroError** , чтобы отобразить сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e5f77-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="e5f77-120">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e5f77-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
