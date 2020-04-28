---
title: Макрокоманда SetTempVar
TOCTitle: SetTempVar macro action
ms:assetid: 9c3b7bee-02c5-efbf-1276-4c4a1f7802d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198102(v=office.15)
ms:contentKeyID: 48546593
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm150219
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: b630304774e521162687d4c78a6a97cf18ddb419
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306525"
---
# <a name="settempvar-macro-action"></a><span data-ttu-id="d8a8c-102">Макрокоманда SetTempVar</span><span class="sxs-lookup"><span data-stu-id="d8a8c-102">SetTempVar macro action</span></span>


<span data-ttu-id="d8a8c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8a8c-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="d8a8c-104">Вы можете использовать действие **Макрокоманда SetTempVar** , чтобы создать временную переменную и присвоить ей определенное значение.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-104">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value.</span></span> <span data-ttu-id="d8a8c-105">Переменную можно использовать в качестве условия или аргумента в последующих действиях или можно использовать переменную в другом макросе, в процедуре обработки события или в форме или отчете.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-105">The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="d8a8c-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="d8a8c-106">Setting</span></span>

<span data-ttu-id="d8a8c-107">Макрокоманда **Макрокоманда SetTempVar** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8a8c-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="d8a8c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="d8a8c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8a8c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d8a8c-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="d8a8c-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="d8a8c-111">Введите имя временной переменной.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8a8c-112"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="d8a8c-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="d8a8c-113">Введите выражение, которое будет использоваться для задания значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="d8a8c-114">Не ставьте перед выражением знак равенства (<strong>=</strong>).</span><span class="sxs-lookup"><span data-stu-id="d8a8c-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="d8a8c-115">Вы можете нажать кнопку <strong>построить</strong></span><span class="sxs-lookup"><span data-stu-id="d8a8c-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="d8a8c-117">Использование построителя выражений для задания этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d8a8c-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="d8a8c-118">Remarks</span></span>

- <span data-ttu-id="d8a8c-119">Одновременно может быть определено до 255 временных переменных.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-119">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="d8a8c-120">Если не удалить временную переменную, она останется в памяти до тех пор, пока не будет закрыта база данных.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-120">If you do not remove a temporary variable, it will remain in memory until you close the database.</span></span> <span data-ttu-id="d8a8c-121">Рекомендуется удалять временные переменные после завершения их использования.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-121">It is a good practice to remove temporary variables when you are finished using them.</span></span> <span data-ttu-id="d8a8c-122">Чтобы удалить одну временную переменную, используйте действие **[Макрокоманда removetempvar](removetempvar-macro-action.md)** и задайте для аргумента имя временной переменной, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-122">To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove.</span></span> <span data-ttu-id="d8a8c-123">Если у вас есть несколько временных переменных и вы хотите удалить их все сразу, используйте действие **Макрокоманда removealltempvars** .</span><span class="sxs-lookup"><span data-stu-id="d8a8c-123">If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="d8a8c-124">Временные переменные являются глобальными.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-124">Temporary variables are global.</span></span> <span data-ttu-id="d8a8c-125">После создания временной переменной можно ссылаться на нее в процедуре обработки события, модуле Visual Basic для приложений (VBA), запросе или выражении.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="d8a8c-126">Например, если вы создали временную переменную с именем *мивар*, вы можете использовать переменную в качестве источника элемента управления для текстового поля, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="d8a8c-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="d8a8c-127">В макросах, запросах и процедурах обработки событий перед выражением не должно быть знака равенства.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="d8a8c-128">Вы также можете ссылаться на временные переменные в любых надстройках или базах данных, на которые имеются ссылки.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="d8a8c-129">Чтобы выполнить действие **Макрокоманда SetTempVar** в модуле VBA, используйте метод **Add** объекта **TempVars** .</span><span class="sxs-lookup"><span data-stu-id="d8a8c-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="d8a8c-130">Пример</span><span class="sxs-lookup"><span data-stu-id="d8a8c-130">Example</span></span>

<span data-ttu-id="d8a8c-131">В следующем макросе показано, как создать временную переменную с помощью действия **Макрокоманда SetTempVar** , а затем с помощью временной переменной в условии и окне сообщения, а затем удалить временную переменную.</span><span class="sxs-lookup"><span data-stu-id="d8a8c-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d8a8c-132">Условие</span><span class="sxs-lookup"><span data-stu-id="d8a8c-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="d8a8c-133">Action</span><span class="sxs-lookup"><span data-stu-id="d8a8c-133">Action</span></span></p></th>
<th><p><span data-ttu-id="d8a8c-134">Аргументы</span><span class="sxs-lookup"><span data-stu-id="d8a8c-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="d8a8c-135"><strong>Макрокоманда SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="d8a8c-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="d8a8c-136"><strong>Name</strong>:<strong>выражение</strong>мивар: InputBox (&quot;введите ненулевое значение).&quot;</span><span class="sxs-lookup"><span data-stu-id="d8a8c-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d8a8c-137">[TempVars]! [Мивар] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="d8a8c-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="d8a8c-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="d8a8c-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="d8a8c-139"><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [TempVars]! [Мивар] &amp; &quot;. &quot; <strong>Гудок</strong>: <strong>естипе</strong>: <strong>Information</strong></span><span class="sxs-lookup"><span data-stu-id="d8a8c-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="d8a8c-140"><strong>Макрокоманда removetempvar</strong></span><span class="sxs-lookup"><span data-stu-id="d8a8c-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="d8a8c-141"><strong>Name</strong>: мивар</span><span class="sxs-lookup"><span data-stu-id="d8a8c-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

