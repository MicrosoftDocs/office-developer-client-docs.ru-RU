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
# <a name="settempvar-macro-action"></a><span data-ttu-id="745b8-102">Макрокоманда SetTempVar</span><span class="sxs-lookup"><span data-stu-id="745b8-102">SetTempVar macro action</span></span>


<span data-ttu-id="745b8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="745b8-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="745b8-104">С помощью действия **SetTempVar можно** создать временную переменную и установить для нее определенное значение.</span><span class="sxs-lookup"><span data-stu-id="745b8-104">You can use the **SetTempVar** action to create a temporary variable and set it to a specific value.</span></span> <span data-ttu-id="745b8-105">Затем переменную можно использовать в качестве условия или аргумента в последующих действиях, или вы можете использовать переменную в другом макросе, в процедуре события или в форме или отчете.</span><span class="sxs-lookup"><span data-stu-id="745b8-105">The variable can then be used as a condition or argument in subsequent actions, or you can use the variable in another macro, in an event procedure, or on a form or report.</span></span>

## <a name="setting"></a><span data-ttu-id="745b8-106">Setting</span><span class="sxs-lookup"><span data-stu-id="745b8-106">Setting</span></span>

<span data-ttu-id="745b8-107">Действие **SetTempVar** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="745b8-107">The **SetTempVar** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="745b8-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="745b8-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="745b8-109">Описание</span><span class="sxs-lookup"><span data-stu-id="745b8-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="745b8-110"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="745b8-110"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="745b8-111">Введите имя временной переменной.</span><span class="sxs-lookup"><span data-stu-id="745b8-111">Enter the name of the temporary variable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="745b8-112"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="745b8-112"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="745b8-113">Введите выражение, которое будет использоваться для ввода значения для этой временной переменной.</span><span class="sxs-lookup"><span data-stu-id="745b8-113">Enter an expression that will be used to set the value for this temporary variable.</span></span> <span data-ttu-id="745b8-114">Не запишите перед выражением знак "равно" <strong>=</strong> ().</span><span class="sxs-lookup"><span data-stu-id="745b8-114">Do not precede the expression with the equal (<strong>=</strong>) sign.</span></span> <span data-ttu-id="745b8-115">Можно нажать кнопку <strong>"Построить"</strong></span><span class="sxs-lookup"><span data-stu-id="745b8-115">You can click the <strong>Build</strong> button</span></span> <img src="media/access-build-button.gif" title="buildbut_ZA06047218" alt="buildbut_ZA06047218" /> <span data-ttu-id="745b8-117">чтобы использовать построитель выражений для этого аргумента.</span><span class="sxs-lookup"><span data-stu-id="745b8-117">to use the Expression Builder to set this argument.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="745b8-118">Заметки</span><span class="sxs-lookup"><span data-stu-id="745b8-118">Remarks</span></span>

- <span data-ttu-id="745b8-119">Одновременно можно определить до 255 временных переменных.</span><span class="sxs-lookup"><span data-stu-id="745b8-119">You can have up to 255 temporary variables defined at one time.</span></span> <span data-ttu-id="745b8-120">Если не удалить временную переменную, она останется в памяти до закрытия базы данных.</span><span class="sxs-lookup"><span data-stu-id="745b8-120">If you do not remove a temporary variable, it will remain in memory until you close the database.</span></span> <span data-ttu-id="745b8-121">По завершению использования временных переменных мы по-настоящему удаляем их.</span><span class="sxs-lookup"><span data-stu-id="745b8-121">It is a good practice to remove temporary variables when you are finished using them.</span></span> <span data-ttu-id="745b8-122">Чтобы удалить одну временную переменную, используйте действие **[RemoveTempVar](removetempvar-macro-action.md)** и установите в качестве аргумента имя временной переменной, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="745b8-122">To remove a single temporary variable, use the **[RemoveTempVar](removetempvar-macro-action.md)** action and set its argument to the name of the temporary variable that you want to remove.</span></span> <span data-ttu-id="745b8-123">Если у вас несколько временных переменных и вы хотите удалить их все одновременно, используйте действие **RemoveAllTempVars.**</span><span class="sxs-lookup"><span data-stu-id="745b8-123">If you have more than one temporary variable and you want to remove them all at once, use the **RemoveAllTempVars** action.</span></span>

- <span data-ttu-id="745b8-124">Временные переменные являются глобальными.</span><span class="sxs-lookup"><span data-stu-id="745b8-124">Temporary variables are global.</span></span> <span data-ttu-id="745b8-125">После создания временной переменной можно сослаться на нее в процедуре события, модуле Visual Basic для приложений VBA, запросе или выражении.</span><span class="sxs-lookup"><span data-stu-id="745b8-125">Once a temporary variable has been created, you can refer to it in an event procedure, a Visual Basic for Applications (VBA) module, a query, or an expression.</span></span> <span data-ttu-id="745b8-126">Например, если вы создали временную переменную с именем *MyVar,* вы можете использовать ее в качестве источника управления для текстового окна, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="745b8-126">For example, if you created a temporary variable named *MyVar*, you could use the variable as the control source for a text box by using the following syntax:</span></span>
    
  `=[TempVars]![MyVar]`
    
  > [!NOTE]
  > <span data-ttu-id="745b8-127">В макросах, запросах и процедурах событий нет необходимости предварять выражение равным знаком.</span><span class="sxs-lookup"><span data-stu-id="745b8-127">In macros, queries and event procedures, you do not need to precede the expression with an equal sign.</span></span>
 
  <span data-ttu-id="745b8-128">Вы также можете ссылаться на временные переменные в любых надстройки или базах данных, на которые есть ссылки.</span><span class="sxs-lookup"><span data-stu-id="745b8-128">You can also refer to temporary variables in any add-ins or referenced databases.</span></span>

- <span data-ttu-id="745b8-129">Чтобы запустить действие **SetTempVar** в модуле VBA, используйте метод **Add** объекта **TempVars.**</span><span class="sxs-lookup"><span data-stu-id="745b8-129">To run the **SetTempVar** action in a VBA module, use the **Add** method of the **TempVars** object.</span></span>

## <a name="example"></a><span data-ttu-id="745b8-130">Пример</span><span class="sxs-lookup"><span data-stu-id="745b8-130">Example</span></span>

<span data-ttu-id="745b8-131">В следующем макросе показано, как создать временную переменную с помощью действия **SetTempVar,** затем использовать временную переменную в условии и в окне сообщения, а затем удалить временную переменную.</span><span class="sxs-lookup"><span data-stu-id="745b8-131">The following macro demonstrates how to create a temporary variable by using the **SetTempVar** action, then using the temporary variable in a condition and a message box, and then removing the temporary variable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="745b8-132">Condition</span><span class="sxs-lookup"><span data-stu-id="745b8-132">Condition</span></span></p></th>
<th><p><span data-ttu-id="745b8-133">Action</span><span class="sxs-lookup"><span data-stu-id="745b8-133">Action</span></span></p></th>
<th><p><span data-ttu-id="745b8-134">Аргументы</span><span class="sxs-lookup"><span data-stu-id="745b8-134">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="745b8-135"><strong>SetTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="745b8-135"><strong>SetTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="745b8-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox( &quot; Enter a non-zero number. &quot; )</span><span class="sxs-lookup"><span data-stu-id="745b8-136"><strong>Name</strong>: MyVar<strong>Expression</strong>: InputBox(&quot;Enter a non-zero number.&quot;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="745b8-137">[TempVars]! [MyVar] &lt; &gt; 0</span><span class="sxs-lookup"><span data-stu-id="745b8-137">[TempVars]![MyVar]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="745b8-138"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="745b8-138"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="745b8-139"><strong>Message</strong>: = &quot; You entered &quot; &amp; [TempVars]![ MyVar] &amp; &quot; . &quot; <strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span><span class="sxs-lookup"><span data-stu-id="745b8-139"><strong>Message</strong>: =&quot;You entered &quot; &amp; [TempVars]![MyVar] &amp; &quot;.&quot;<strong>Beep</strong>: <strong>YesType</strong>: <strong>Information</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="745b8-140"><strong>RemoveTempVar</strong></span><span class="sxs-lookup"><span data-stu-id="745b8-140"><strong>RemoveTempVar</strong></span></span></p></td>
<td><p><span data-ttu-id="745b8-141"><strong>Name</strong>: MyVar</span><span class="sxs-lookup"><span data-stu-id="745b8-141"><strong>Name</strong>: MyVar</span></span></p></td>
</tr>
</tbody>
</table>

