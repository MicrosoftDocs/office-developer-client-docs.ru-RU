---
title: Действия макроса SetLocalVar
TOCTitle: SetLocalVar Macro Action
ms:assetid: 8a6af395-0f76-72e2-37f3-2cff22a38b3c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197097(v=office.15)
ms:contentKeyID: 48546190
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm176660
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 299227553481c4f149827c31078111db7b427f7f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886643"
---
# <a name="setlocalvar-macro-action"></a><span data-ttu-id="29bde-102">Действия макроса SetLocalVar</span><span class="sxs-lookup"><span data-stu-id="29bde-102">SetLocalVar Macro Action</span></span>


<span data-ttu-id="29bde-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29bde-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29bde-104">**ЗадатьЛокПеременную** создает временную переменную и присвойте ей значение определенного значения.</span><span class="sxs-lookup"><span data-stu-id="29bde-104">The **SetLocalVar** action creates a temporary variable and set it to a specific value.</span></span>

## <a name="setting"></a><span data-ttu-id="29bde-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="29bde-105">Setting</span></span>

<span data-ttu-id="29bde-106">**ЗадатьЛокПеременную** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="29bde-106">The **SetLocalVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29bde-107">Argument</span><span class="sxs-lookup"><span data-stu-id="29bde-107">Argument</span></span></p></th>
<th><p><span data-ttu-id="29bde-108">Обязательный</span><span class="sxs-lookup"><span data-stu-id="29bde-108">Required</span></span></p></th>
<th><p><span data-ttu-id="29bde-109">Описание</span><span class="sxs-lookup"><span data-stu-id="29bde-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29bde-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="29bde-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="29bde-111">Да</span><span class="sxs-lookup"><span data-stu-id="29bde-111">Yes</span></span></p></td>
<td><p><span data-ttu-id="29bde-112">Строка, задающая имя переменной.</span><span class="sxs-lookup"><span data-stu-id="29bde-112">A string that specifies the name of the variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29bde-113"><strong>Выражение</strong></span><span class="sxs-lookup"><span data-stu-id="29bde-113"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="29bde-114">Да</span><span class="sxs-lookup"><span data-stu-id="29bde-114">Yes</span></span></p></td>
<td><p><span data-ttu-id="29bde-115">Выражение, которое будет использоваться для задания значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="29bde-115">An expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="29bde-116">Перед выражением знак равенства (=).</span><span class="sxs-lookup"><span data-stu-id="29bde-116">Do not precede the expression with the equal sign (=).</span></span> <span data-ttu-id="29bde-117">Можно нажмите кнопку <strong>Построить</strong> для задания аргумента с помощью <strong>Построителя выражений</strong> .</span><span class="sxs-lookup"><span data-stu-id="29bde-117">You can click the <strong>Build</strong> button to use the <strong>Expression Builder</strong> to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="29bde-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="29bde-118">Remarks</span></span>

<span data-ttu-id="29bde-119">Переменные, созданные **ЗадатьЛокПеременную** можно использовать только в макросе, в котором они определены.</span><span class="sxs-lookup"><span data-stu-id="29bde-119">Variables created by the **SetLocalVar** action can be used only in the macro in which they are defined.</span></span> <span data-ttu-id="29bde-120">Действие **[SetTempVar](settempvar-macro-action.md)** используется для определения переменной, которая может использоваться в другого макроса в процедуре события или на форму или отчет.</span><span class="sxs-lookup"><span data-stu-id="29bde-120">Use the **[SetTempVar](settempvar-macro-action.md)** action to define a variable that can be used in another macro, in an event procedure, or on a form or report.</span></span>

<span data-ttu-id="29bde-121">После создания временную переменную в выражении можно обратиться к нему.</span><span class="sxs-lookup"><span data-stu-id="29bde-121">Once a temporary variable has been created, you can refer to it in an expression.</span></span> <span data-ttu-id="29bde-122">Например при создании временную переменную с именем TotalAmount можно использовать переменной как источник элемента управления для текстовое поле, используя следующий синтаксис.</span><span class="sxs-lookup"><span data-stu-id="29bde-122">For example, if you created a temporary variable named TotalAmount, you could use the variable as the control source for a text box by using the following syntax.</span></span>

`=[LocalVars]![TotalAmount]`


> [!NOTE]
> <P><span data-ttu-id="29bde-123">Макрос данных не нужно использовать коллекцию LocalVars для ссылки на переменную.</span><span class="sxs-lookup"><span data-stu-id="29bde-123">In a Data Macro, you do not have to use the LocalVars collection to refer to a variable.</span></span> <span data-ttu-id="29bde-124">К примеру при создании временную переменную в макросе данных с именем TotalAmount можно использовать переменной как источник элемента управления для текстового поля, используя следующий синтаксис</span><span class="sxs-lookup"><span data-stu-id="29bde-124">For example, if you created a temporary variable in a Data Macro named TotalAmount, you could use the variable as the control source for a text box by using the following syntax</span></span><BR><span data-ttu-id="29bde-125">= [TotalAmount]</span><span class="sxs-lookup"><span data-stu-id="29bde-125">=[TotalAmount]</span></span></P>


