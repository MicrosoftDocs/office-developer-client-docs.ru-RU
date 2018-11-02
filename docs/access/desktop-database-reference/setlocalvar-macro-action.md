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
ms.openlocfilehash: b6db77a3cd712717e5aa2eb22e89f90557a1dabf
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926019"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="2f957-102">Макрокоманда SetLocalVar</span><span class="sxs-lookup"><span data-stu-id="2f957-102">SetLocalVar macro action</span></span>


<span data-ttu-id="2f957-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f957-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f957-104">**ЗадатьЛокПеременную** создает временную переменную и присвойте ей значение определенного значения.</span><span class="sxs-lookup"><span data-stu-id="2f957-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="2f957-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="2f957-105">Setting</span></span>

<span data-ttu-id="2f957-106">**ЗадатьЛокПеременную** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2f957-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f957-107">Argument</span><span class="sxs-lookup"><span data-stu-id="2f957-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="2f957-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="2f957-108">Required</span></span></p></th>
<th><p><span data-ttu-id="2f957-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2f957-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f957-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="2f957-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2f957-111">Да</span><span class="sxs-lookup"><span data-stu-id="2f957-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="2f957-112">Строка, задающая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="2f957-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f957-113"><strong>Выражение</strong></span><span class="sxs-lookup"><span data-stu-id="2f957-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="2f957-114">Да</span><span class="sxs-lookup"><span data-stu-id="2f957-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="2f957-115">Выражение, которое будет использоваться для задания значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="2f957-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="2f957-116">Перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="2f957-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="2f957-117">Можно нажмите кнопку <strong>Построить</strong> для задания аргумента с помощью <strong>Построителя выражений</strong> .</span><span class="sxs-lookup"><span data-stu-id="2f957-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2f957-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="2f957-118">Remarks</span></span>

<span data-ttu-id="2f957-119">Переменные, созданные **ЗадатьЛокПеременную** можно использовать только в макросе, в котором они определены.</span><span class="sxs-lookup"><span data-stu-id="2f957-119">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined.</span></span> <span data-ttu-id="2f957-120">Действие **[SetTempVar](settempvar-macro-action.md)** используется для определения переменной, которая может использоваться в другого макроса в процедуре события или на форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="2f957-120">Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="2f957-121">После создания временную переменную в выражении можно обратиться к нему.</span><span class="sxs-lookup"><span data-stu-id="2f957-121">Once a temporary variable has been created, you can refer to it in an expression.</span></span> <span data-ttu-id="2f957-122">Например при создании временную переменную с именем TotalAmount можно использовать переменной как источник элемента управления для текстовое поле, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="2f957-122">For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P><span data-ttu-id="2f957-123">Макрос данных не нужно использовать коллекцию LocalVars для ссылки на переменную.</span><span class="sxs-lookup"><span data-stu-id="2f957-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="2f957-124">К примеру при создании временную переменную в макросе данных с именем TotalAmount можно использовать переменной как источник элемента управления для текстового поля, используя следующий синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f957-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax</span></span><BR><span data-ttu-id="2f957-125">= [TotalAmount]</span><span class="sxs-lookup"><span data-stu-id="2f957-125">=[TotalAmount]</span></span></P>


