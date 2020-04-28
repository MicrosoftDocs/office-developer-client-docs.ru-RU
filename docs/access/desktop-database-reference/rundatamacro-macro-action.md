---
title: Макрокоманда RunDataMacro
TOCTitle: RunDataMacro macro action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 32945f0822682a9432d75ed1ac59117dde3cc0e9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306813"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="bf228-102">Макрокоманда RunDataMacro</span><span class="sxs-lookup"><span data-stu-id="bf228-102">RunDataMacro macro action</span></span>

<span data-ttu-id="bf228-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf228-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf228-104">Вы можете использовать действие **RunDataMacro** для запуска именованного макроса данных.</span><span class="sxs-lookup"><span data-stu-id="bf228-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="bf228-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="bf228-105">Setting</span></span>

<span data-ttu-id="bf228-106">Действие **RunDataMacro** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="bf228-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bf228-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="bf228-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bf228-108">Описание</span><span class="sxs-lookup"><span data-stu-id="bf228-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf228-109">Имя</span><span class="sxs-lookup"><span data-stu-id="bf228-109">Name</span></span></p></td>
<td><p><span data-ttu-id="bf228-110">Имя запускаемого макроса данных.</span><span class="sxs-lookup"><span data-stu-id="bf228-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bf228-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf228-111">Remarks</span></span>

<span data-ttu-id="bf228-112">Вы можете использовать макрокоманду **RunDataMacro** в макросах, именованных макросах данных и следующих макросах: **[после удаления макроса](after-delete-macro-event.md)** **[после вставки](after-insert-macro-event.md)** макроса и **[после обновления макроса](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="bf228-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete macro event](after-delete-macro-event.md)**, **[After Insert macro event](after-insert-macro-event.md)** and **[After Update macro event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="bf228-113">Имя макроса данных должно включать таблицу, к которой она подключена (например, **Comments. аддкоммент**, а не только **аддкоммент**).</span><span class="sxs-lookup"><span data-stu-id="bf228-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="bf228-114">При выборе макроса данных, который требуется запустить в конструкторе макросов, Access определяет, требуются ли для макроса данных параметры.</span><span class="sxs-lookup"><span data-stu-id="bf228-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="bf228-115">Если макрос данных требует параметров, отображаются текстовые поля, в которых можно вводить аргументы.</span><span class="sxs-lookup"><span data-stu-id="bf228-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="bf228-116">При запуске макроса, содержащего действие **RunDataMacro** , и достижении действия **RunDataMacro** , Access запускает макрос данных, который вызывается.</span><span class="sxs-lookup"><span data-stu-id="bf228-116">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro.</span></span> <span data-ttu-id="bf228-117">После завершения вызываемого макроса данных Access возвращается к исходному макросу и выполняет следующее действие.</span><span class="sxs-lookup"><span data-stu-id="bf228-117">When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="bf228-118">Пример</span><span class="sxs-lookup"><span data-stu-id="bf228-118">Example</span></span>

<span data-ttu-id="bf228-119">В приведенном ниже примере показано, как передать параметр в именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="bf228-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="bf228-120">Макрос данных Дмжеткуррентсервицерекуест таблицы Тблсервицерекуестс вызывается с помощью действия RunDataMacro.</span><span class="sxs-lookup"><span data-stu-id="bf228-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="bf228-121">После завершения Дмжеткуррентсервицерекуест переменная Куррентсервицерекуест, возвращаемая макросом данных, записывается в текстовое поле Тксткуррентср.</span><span class="sxs-lookup"><span data-stu-id="bf228-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="bf228-122">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="bf228-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    RunDataMacro
        Macro Name tblServiceRequests.dmGetCurrentServiceRequest
    
    Parameters
        prmAssignedTo =[ID]
    
    SetProperty
        Control Name txtCurrentSR
        Property Value
        Value =[ReturnVars]![CurrentServiceRequest]
```
