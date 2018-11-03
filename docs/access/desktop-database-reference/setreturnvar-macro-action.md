---
title: Макрокоманда SetReturnVar
TOCTitle: SetReturnVar macro action
ms:assetid: 53719857-00bb-4f33-b5d2-93aff92d736e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193989(v=office.15)
ms:contentKeyID: 48544870
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f73ba90b4eae9f5da17e27d466044d97fb815d74
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923793"
---
# <a name="setreturnvar-macro-action"></a><span data-ttu-id="6db30-102">Макрокоманда SetReturnVar</span><span class="sxs-lookup"><span data-stu-id="6db30-102">SetReturnVar macro action</span></span>

<span data-ttu-id="6db30-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6db30-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6db30-104">Действие **SetReturnVar** создает возвращаемое переменной и устанавливает для определенного значения.</span><span class="sxs-lookup"><span data-stu-id="6db30-104">The **SetReturnVar** action creates a return variable and sets it to a specific value.</span></span>

> [!NOTE]
> <span data-ttu-id="6db30-105">**SetReturnVar** действие доступно только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="6db30-105">The **SetReturnVar** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="6db30-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="6db30-106">Setting</span></span>

<span data-ttu-id="6db30-107">Действие **SetReturnVar** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="6db30-107">The **SetReturnVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6db30-108">Argument</span><span class="sxs-lookup"><span data-stu-id="6db30-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="6db30-109">Обязательный</span><span class="sxs-lookup"><span data-stu-id="6db30-109">Required</span></span></p></th>
<th><p><span data-ttu-id="6db30-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6db30-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6db30-111">Имя</span><span class="sxs-lookup"><span data-stu-id="6db30-111">Name</span></span></p></td>
<td><p><span data-ttu-id="6db30-112">Да</span><span class="sxs-lookup"><span data-stu-id="6db30-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="6db30-113">Строка, задающая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="6db30-113">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6db30-114">Выражение</span><span class="sxs-lookup"><span data-stu-id="6db30-114">Expression</span></span></p></td>
<td><p><span data-ttu-id="6db30-115">Да</span><span class="sxs-lookup"><span data-stu-id="6db30-115">Yes</span></span></p></td>
<td><p><span data-ttu-id="6db30-116">Выражение, которое будет использоваться для задания значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="6db30-116">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="6db30-117">Перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="6db30-117">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="6db30-118">Можно нажмите кнопку <strong>Построить</strong> для задания аргумента с помощью <strong>Построителя выражений</strong> .</span><span class="sxs-lookup"><span data-stu-id="6db30-118">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6db30-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="6db30-119">Remarks</span></span>

<span data-ttu-id="6db30-120">Действие **SetReturnVar** используется для создания **ReturnVar**, которая является переменной, которая может использоваться макросы, которые могут вызывать макрос данных с помощью **ЗапускМакросаДанных** .</span><span class="sxs-lookup"><span data-stu-id="6db30-120">The **SetReturnVar** action is used to create a **ReturnVar**, which is variable that can be used by macros that call a data macro by using the **RunDataMacro** action.</span></span>

<span data-ttu-id="6db30-121">После создания **ReturnVar** с **SetReturnVar** действие вызова макроса можно использовать в выражении.</span><span class="sxs-lookup"><span data-stu-id="6db30-121">Once a **ReturnVar** is created by the **SetReturnVar** action, the calling macro can use it in an expression.</span></span> <span data-ttu-id="6db30-122">Например при создании **ReturnVar** с именем **UpdateSuccess**, можно использовать переменную, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="6db30-122">For example, if you created a **ReturnVar** named **UpdateSuccess**, you could use the variable by using the following syntax:</span></span>

```vb
    =[ReturnVars]![UpdateSuccess]
```

<span data-ttu-id="6db30-123">Действие **SetReturnVar** можно использовать только в именованных макросов данных.</span><span class="sxs-lookup"><span data-stu-id="6db30-123">The **SetReturnVar** action can be used only in named data macros.</span></span> <span data-ttu-id="6db30-124">Он недоступен в макросах данных, подключенные к события макрос данных.</span><span class="sxs-lookup"><span data-stu-id="6db30-124">It is not available in data macros that are attached to a data macro event.</span></span>

## <a name="example"></a><span data-ttu-id="6db30-125">Пример</span><span class="sxs-lookup"><span data-stu-id="6db30-125">Example</span></span>

<span data-ttu-id="6db30-126">Следующий пример демонстрирует действие SetReturnVar используется для возврата значения из именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="6db30-126">The following example shows how to use the SetReturnVar action to return a value from a named data macro.</span></span> <span data-ttu-id="6db30-127">ReturnVar, с именем **CurrentServiceRequest** возвращается в макросе или Visual Basic для приложений (VBA) подпрограмму, которая называется именованный макрос данных.</span><span class="sxs-lookup"><span data-stu-id="6db30-127">A ReturnVar named **CurrentServiceRequest** is returned to the macro or Visual Basic for Applications (VBA) subroutine that called the named data macro.</span></span>

<span data-ttu-id="6db30-128">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6db30-128">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
