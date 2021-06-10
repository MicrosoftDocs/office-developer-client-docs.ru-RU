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
# <a name="submacro-macro-statement"></a><span data-ttu-id="22a12-102">Оператор макроса Submacro</span><span class="sxs-lookup"><span data-stu-id="22a12-102">Submacro macro statement</span></span>

<span data-ttu-id="22a12-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22a12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22a12-104">В **заявлении Submacro** определяется отдельный макрос в окне Macro Designer.</span><span class="sxs-lookup"><span data-stu-id="22a12-104">The **Submacro** statement defines a separate macro in the Macro Designer window.</span></span>

## <a name="setting"></a><span data-ttu-id="22a12-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="22a12-105">Setting</span></span>

<span data-ttu-id="22a12-106">Действие **Submacro** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="22a12-106">The **Submacro** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="22a12-107">Аргумент</span><span class="sxs-lookup"><span data-stu-id="22a12-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="22a12-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="22a12-108">Required</span></span></p></th>
<th><p><span data-ttu-id="22a12-109">Описание</span><span class="sxs-lookup"><span data-stu-id="22a12-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22a12-110">Имя</span><span class="sxs-lookup"><span data-stu-id="22a12-110">Name</span></span></p></td>
<td><p><span data-ttu-id="22a12-111">Да</span><span class="sxs-lookup"><span data-stu-id="22a12-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="22a12-112">Строка, которая отображается как имя макроса.</span><span class="sxs-lookup"><span data-stu-id="22a12-112">A string that appears as the name of the macro.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="22a12-113">Пример</span><span class="sxs-lookup"><span data-stu-id="22a12-113">Example</span></span>

<span data-ttu-id="22a12-114">Следующий макрос демонстрирует использование действия **OnError.**</span><span class="sxs-lookup"><span data-stu-id="22a12-114">The following macro demonstrates the use of the **OnError** action.</span></span> <span data-ttu-id="22a12-115">В этом примере действие **OnError** указывает, что при ошибке Access запустится настраиваемый макрос обработки ошибок с именем ErrorHandler.</span><span class="sxs-lookup"><span data-stu-id="22a12-115">In this example, the **OnError** action specifies that Access run a custom error handling macro named ErrorHandler when an error occurs.</span></span> <span data-ttu-id="22a12-116">При ошибке называется submacro CatchErrors.</span><span class="sxs-lookup"><span data-stu-id="22a12-116">When an error occurs, the CatchErrors submacro is called.</span></span> <span data-ttu-id="22a12-117">Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса прекращается.</span><span class="sxs-lookup"><span data-stu-id="22a12-117">If the error number is 2102, a specific message is displayed and macro execution is halted.</span></span> <span data-ttu-id="22a12-118">В противном случае отображается сообщение с описанием ошибки и приостановка макроса, чтобы можно было выполнить дополнительные устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="22a12-118">Otherwise, a message describing the error is displayed and the macro is paused so that you can perform additional troubleshooting.</span></span> <span data-ttu-id="22a12-119">Макрос ErrorHandler отображает поле сообщений, которое ссылается на объект **MacroError** для отображения сведений об ошибке.</span><span class="sxs-lookup"><span data-stu-id="22a12-119">The ErrorHandler macro displays a message box that refers to the **MacroError** object to display information about the error.</span></span>

<span data-ttu-id="22a12-120">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="22a12-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
