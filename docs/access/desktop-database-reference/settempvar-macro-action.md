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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705233"
---
# <a name="settempvar-macro-action"></a><span data-ttu-id="6b64f-102">Макрокоманда SetTempVar</span><span class="sxs-lookup"><span data-stu-id="6b64f-102">SetTempVar macro action</span></span>


<span data-ttu-id="6b64f-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b64f-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="6b64f-104">Чтобы создать временную переменную и присвойте ей значение определенного значения можно использовать действие **SetTempVar** .</span><span class="sxs-lookup"><span data-stu-id="6b64f-104">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value.</span></span> <span data-ttu-id="6b64f-105">Переменная затем использовать как условие или аргумент в последующие действия или в другой макрос, в процедуре события или на форму или отчет можно использовать переменную.</span><span class="sxs-lookup"><span data-stu-id="6b64f-105">The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="6b64f-106">Setting</span><span class="sxs-lookup"><span data-stu-id="6b64f-106">Setting</span></span>

<span data-ttu-id="6b64f-107">Действие **SetTempVar** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="6b64f-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b64f-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6b64f-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6b64f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6b64f-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b64f-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="6b64f-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6b64f-111">Введите имя временную переменную.</span><span class="sxs-lookup"><span data-stu-id="6b64f-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b64f-112"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="6b64f-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="6b64f-113">Введите выражение, которое будет использоваться для задания значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="6b64f-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="6b64f-114">Перед выражением равенства (<strong>=</strong>) входа.</span><span class="sxs-lookup"><span data-stu-id="6b64f-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="6b64f-115">Можно нажать кнопку <strong>построения</strong></span><span class="sxs-lookup"><span data-stu-id="6b64f-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="6b64f-117">Чтобы использовать построитель выражений для задания аргумента.</span><span class="sxs-lookup"><span data-stu-id="6b64f-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6b64f-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="6b64f-118">Remarks</span></span>

- <span data-ttu-id="6b64f-119">Может быть длиной до 255 временные переменные, определенные за один раз.</span><span class="sxs-lookup"><span data-stu-id="6b64f-119">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="6b64f-120">Если вы не удалите временную переменную, остается в памяти до закрытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="6b64f-120">If you do not remove a temporary variable, it will remain in memory until you close the database.</span></span> <span data-ttu-id="6b64f-121">Рекомендуется удалить временные переменные после завершения их использования.</span><span class="sxs-lookup"><span data-stu-id="6b64f-121">It is a good practice to remove temporary variables when you are finished using them.</span></span> <span data-ttu-id="6b64f-122">Чтобы удалить одного временную переменную, используйте действие **[RemoveTempVar](removetempvar-macro-action.md)** и установите аргумента имя временную переменную, которую требуется удалить.</span><span class="sxs-lookup"><span data-stu-id="6b64f-122">To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove.</span></span> <span data-ttu-id="6b64f-123">Если у вас есть несколько временную переменную, требуется одновременное удаление используйте действие **RemoveAllTempVars** .</span><span class="sxs-lookup"><span data-stu-id="6b64f-123">If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="6b64f-124">Временные переменные являются глобальными.</span><span class="sxs-lookup"><span data-stu-id="6b64f-124">Temporary variables are global.</span></span> <span data-ttu-id="6b64f-125">После создания временную переменную можно обратиться к нему в процедуре события Visual Basic для приложений (VBA) модуля, запроса или выражение.</span><span class="sxs-lookup"><span data-stu-id="6b64f-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="6b64f-126">Например при создании временную переменную с именем *MyVar*можно использовать переменной как источник элемента управления для текстовое поле, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="6b64f-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="6b64f-127">Макросы, запросов и процедур обработки событий перед выражением знак равенства не требуется.</span><span class="sxs-lookup"><span data-stu-id="6b64f-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="6b64f-128">Можно найти временные переменные в любой надстроек или указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="6b64f-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="6b64f-129">Чтобы выполнить действие **SetTempVar** в модуле VBA, используйте метод **Add** объекта **в TempVar** .</span><span class="sxs-lookup"><span data-stu-id="6b64f-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="6b64f-130">Пример</span><span class="sxs-lookup"><span data-stu-id="6b64f-130">Example</span></span>

<span data-ttu-id="6b64f-131">Следующий макрос показано, как создать временную переменную, используя действие **SetTempVar** , а затем временную переменную в окно сообщения и условия и затем удаление временную переменную.</span><span class="sxs-lookup"><span data-stu-id="6b64f-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b64f-132">Условие</span><span class="sxs-lookup"><span data-stu-id="6b64f-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="6b64f-133">Action</span><span class="sxs-lookup"><span data-stu-id="6b64f-133">Action</span></span></p></th>
<th><p><span data-ttu-id="6b64f-134">Arguments</span><span class="sxs-lookup"><span data-stu-id="6b64f-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6b64f-135"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="6b64f-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b64f-136"><strong>Имя</strong>: MyVar<strong>выражение</strong>: InputBox (&quot;введите ненулевое число.&quot;)</span><span class="sxs-lookup"><span data-stu-id="6b64f-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b64f-137">[В TempVar]! [MyVar] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="6b64f-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="6b64f-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="6b64f-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="6b64f-139"><strong>Сообщение</strong>: =&quot;вы ввели &quot; &amp; [в TempVar]! [MyVar] &amp; &quot;. &quot; <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: <strong>сведения</strong></span><span class="sxs-lookup"><span data-stu-id="6b64f-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="6b64f-140"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="6b64f-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="6b64f-141"><strong>Имя</strong>: MyVar</span><span class="sxs-lookup"><span data-stu-id="6b64f-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

