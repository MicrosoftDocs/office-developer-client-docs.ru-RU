---
title: RunDataMacro Macro Action
TOCTitle: RunDataMacro Macro Action
ms:assetid: fe4ac2f4-7851-7797-ce91-5f2dd3ba4d22
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837269(v=office.15)
ms:contentKeyID: 48548933
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm168493
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9790faf03ba0f6ea02520abb525c4301ac2181e2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480240"
---
# <a name="rundatamacro-macro-action"></a><span data-ttu-id="9e8c6-102">RunDataMacro Macro Action</span><span class="sxs-lookup"><span data-stu-id="9e8c6-102">RunDataMacro Macro Action</span></span>

<span data-ttu-id="9e8c6-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e8c6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e8c6-104">**ЗапускМакросаДанных** можно использовать для запуска именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-104">You can use the **RunDataMacro** action to run a named data macro.</span></span>

## <a name="setting"></a><span data-ttu-id="9e8c6-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="9e8c6-105">Setting</span></span>

<span data-ttu-id="9e8c6-106">**ЗапускМакросаДанных** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-106">The **RunDataMacro** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9e8c6-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="9e8c6-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="9e8c6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="9e8c6-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e8c6-109">Имя</span><span class="sxs-lookup"><span data-stu-id="9e8c6-109">Name</span></span></p></td>
<td><p><span data-ttu-id="9e8c6-110">Имя макроса данных для запуска.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-110">The name of the data macro to run.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="9e8c6-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="9e8c6-111">Remarks</span></span>

<span data-ttu-id="9e8c6-112">Можно использовать **ЗапускМакросаДанных** в макросы, с именем макросов данных и следующие события макрос: **[После удаления события макрос](after-delete-macro-event.md)**, **[После вставки события макросов](after-insert-macro-event.md)** и **[После обновления макрос события](after-update-macro-event.md)**.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-112">You can use the **RunDataMacro** action in macros, named data macros, and the following macro events: **[After Delete Macro Event](after-delete-macro-event.md)**, **[After Insert Macro Event](after-insert-macro-event.md)** and **[After Update Macro Event](after-update-macro-event.md)**.</span></span>

<span data-ttu-id="9e8c6-113">Имя макроса данных необходимо включить таблицу, к которой он подключен (например, **Comments.AddComment**, не только **AddComment**).</span><span class="sxs-lookup"><span data-stu-id="9e8c6-113">The name of the data macro must include the table to which it is attached (for example, **Comments.AddComment**, not just **AddComment**).</span></span>

<span data-ttu-id="9e8c6-114">При выборе макрос данных, которая должна работать в конструктор макросов Access определяет необходимость в макрос данных параметров.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-114">When you select the data macro that you want to run in the macro designer, Access determines if the data macro requires parameters.</span></span> <span data-ttu-id="9e8c6-115">Если макрос данных требуются параметры, текстовых полей отображаются для ввода в аргументах.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-115">If the data macro requires parameters, text boxes appear where you can type in the arguments.</span></span>

<span data-ttu-id="9e8c6-116">При запуске макроса, содержащего **ЗапускМакросаДанных** и достигает **ЗапускМакросаДанных** , Access запускает макрос называемое данных.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-116">When you run a macro that contains the **RunDataMacro** action and it reaches the **RunDataMacro** action, Access runs the called data macro.</span></span> <span data-ttu-id="9e8c6-117">По завершении макрос называемое данных Access возвращает исходное макрос и выполняется следующее действие.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-117">When the called data macro has finished, Access returns to the original macro and runs the next action.</span></span>

## <a name="example"></a><span data-ttu-id="9e8c6-118">Пример</span><span class="sxs-lookup"><span data-stu-id="9e8c6-118">Example</span></span>

<span data-ttu-id="9e8c6-119">Следующем примере показано, как передать параметр именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-119">The following example shows how to pass a parameter to a named data macro.</span></span> <span data-ttu-id="9e8c6-120">Макрос данных dmGetCurrentServiceRequest таблицы tblServiceRequests вызывается с помощью ЗапускМакросаДанных.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-120">The dmGetCurrentServiceRequest data macro of the tblServiceRequests table is called by using the RunDataMacro action.</span></span> <span data-ttu-id="9e8c6-121">По завершении dmGetCurrentServiceRequest переменной CurrentServiceRequest возвращаются записи макроса данных в текстовом поле txtCurrentSR формы.</span><span class="sxs-lookup"><span data-stu-id="9e8c6-121">When the dmGetCurrentServiceRequest is finished, the CurrentServiceRequest variable returned form the data macro is written to the txtCurrentSR text box.</span></span>

<span data-ttu-id="9e8c6-122">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9e8c6-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
