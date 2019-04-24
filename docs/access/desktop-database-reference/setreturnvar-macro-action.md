---
title: Макрокоманда SetReturnVar
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e0c849fc507d535807bc088e667acd74410ddd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308675"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="e176a-102">Макрокоманда SetReturnVar</span><span class="sxs-lookup"><span data-stu-id="e176a-102">SetReturnVar macro action</span></span>

<span data-ttu-id="e176a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e176a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e176a-104">Действие **SetReturnVar** создает переменную возврата и присваивает ей определенное значение.</span><span class="sxs-lookup"><span data-stu-id="e176a-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="e176a-105">Действие **SetReturnVar** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="e176a-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="e176a-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="e176a-106">Setting</span></span>

<span data-ttu-id="e176a-107">Макрокоманда **SetReturnVar** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="e176a-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e176a-108">Аргумент</span><span class="sxs-lookup"><span data-stu-id="e176a-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="e176a-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="e176a-109">Required</span></span></p></th>
<th><p><span data-ttu-id="e176a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e176a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e176a-111">Имя</span><span class="sxs-lookup"><span data-stu-id="e176a-111">Name</span></span></p></td>
<td><p><span data-ttu-id="e176a-112">Да</span><span class="sxs-lookup"><span data-stu-id="e176a-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="e176a-113">Строка, определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="e176a-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e176a-114">Expression</span><span class="sxs-lookup"><span data-stu-id="e176a-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="e176a-115">Да</span><span class="sxs-lookup"><span data-stu-id="e176a-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="e176a-116">Выражение, которое будет использоваться для задания значений для данной временной переменной.</span><span class="sxs-lookup"><span data-stu-id="e176a-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="e176a-117">Не ставьте перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="e176a-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="e176a-118">Вы можете нажать кнопку <strong>Build</strong>, чтобы использовать <strong>Создатель выражений</strong> для установки данного аргумента.</span><span class="sxs-lookup"><span data-stu-id="e176a-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e176a-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e176a-119">Remarks</span></span>

<span data-ttu-id="e176a-120">Действие **SetReturnVar** используется для создания **ReturnVar**, который представляет собой переменную, которая может использоваться макросами, вызывающими макросы данных с помощью действия **RunDataMacro** .</span><span class="sxs-lookup"><span data-stu-id="e176a-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="e176a-121">После создания **ReturnVar** с помощью действия **SetReturnVar** вызывающий макрос может использовать его в выражении.</span><span class="sxs-lookup"><span data-stu-id="e176a-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="e176a-122">Например, если вы создали **ReturnVar** с именем **упдатесукцесс**, вы можете использовать переменную с помощью следующего синтаксиса:</span><span class="sxs-lookup"><span data-stu-id="e176a-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="e176a-123">Действие **SetReturnVar** можно использовать только в именованных макросах данных.</span><span class="sxs-lookup"><span data-stu-id="e176a-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="e176a-124">Она недоступна в макросах данных, вложенных в событие макросов данных.</span><span class="sxs-lookup"><span data-stu-id="e176a-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="e176a-125">Пример</span><span class="sxs-lookup"><span data-stu-id="e176a-125">Example</span></span>

<span data-ttu-id="e176a-126">В приведенном ниже примере показано, как с помощью действия SetReturnVar вернуть значение из именованного макроса данных.</span><span class="sxs-lookup"><span data-stu-id="e176a-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="e176a-127">ReturnVar с именем **куррентсервицерекуест** возвращается в макрос или подПрограмму Visual Basic для приложений (VBA), которая вызвала именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="e176a-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="e176a-128">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="e176a-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
