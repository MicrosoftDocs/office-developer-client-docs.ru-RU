---
title: Макрокоманда SetLocalVar
TOCTitle: SetLocalVar macro action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 091b9717b9a2e35cfc8d0c8555e28570628065ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702462"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="9b77e-102">Макрокоманда SetLocalVar</span><span class="sxs-lookup"><span data-stu-id="9b77e-102">SetLocalVar macro action</span></span>

<span data-ttu-id="9b77e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b77e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b77e-104">Действие **SetLocalVar** создает временную переменную и присваивает ей определенное значение.</span><span class="sxs-lookup"><span data-stu-id="9b77e-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="9b77e-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="9b77e-105">Setting</span></span>

<span data-ttu-id="9b77e-106">Действие **GoToControl** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="9b77e-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9b77e-107">Аргумент</span><span class="sxs-lookup"><span data-stu-id="9b77e-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="9b77e-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="9b77e-108">Required</span></span></p></th>
<th><p><span data-ttu-id="9b77e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9b77e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9b77e-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="9b77e-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="9b77e-111">Да</span><span class="sxs-lookup"><span data-stu-id="9b77e-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="9b77e-112">Строка, определяющая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="9b77e-112">A string that specifies the name of the author of the comment.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9b77e-113"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="9b77e-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="9b77e-114">Да</span><span class="sxs-lookup"><span data-stu-id="9b77e-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="9b77e-115">Выражение, которое будет использоваться для задания значений для данной временной переменной.</span><span class="sxs-lookup"><span data-stu-id="9b77e-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="9b77e-116">Не ставьте перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="9b77e-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="9b77e-117">Вы можете нажать кнопку <strong>Build</strong>, чтобы использовать <strong>Создатель выражений</strong> для установки данного аргумента.</span><span class="sxs-lookup"><span data-stu-id="9b77e-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="9b77e-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b77e-118">Remarks</span></span>

<span data-ttu-id="9b77e-119">Переменные, созданные действием **SetLocalVar**, можно использовать только в макросе, в котором они определены.</span><span class="sxs-lookup"><span data-stu-id="9b77e-119">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined.</span></span> <span data-ttu-id="9b77e-120">Используйте действие **[SetTempVar](settempvar-macro-action.md)** для определения переменной, которая может использоваться в других макросах, процедурах обработки событий, формах и отчетах.</span><span class="sxs-lookup"><span data-stu-id="9b77e-120">Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="9b77e-121">После создания временной переменной вы можете ссылаться на нее в выражении.</span><span class="sxs-lookup"><span data-stu-id="9b77e-121">Once a temporary variable has been created, you can refer to it in an expression.</span></span> <span data-ttu-id="9b77e-122">Например, если вы создали временную переменную с именем TotalAmount, вы можете применять ее в качестве источника управления для текстового поля, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="9b77e-122">For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`

> [!NOTE]
> <span data-ttu-id="9b77e-123">В макросе данных у вас нет необходимости использовать коллекцию LocalVars, чтобы сослаться на переменную.</span><span class="sxs-lookup"><span data-stu-id="9b77e-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="9b77e-124">Например, если вы создали временную переменную в макросе данных с именем TotalAmount, вы можете применять ее в качестве источника управления для текстового поля, используя следующий синтаксис: `=[TotalAmount]`.</span><span class="sxs-lookup"><span data-stu-id="9b77e-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax: `=[TotalAmount]`.</span></span>

