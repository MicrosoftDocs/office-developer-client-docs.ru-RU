---
title: Действия макроса ClearMacroError
TOCTitle: ClearMacroError Macro Action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e9b8232f24a837466529f8ce04f9f830af72e7a7
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870193"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="da788-102">Действия макроса ClearMacroError</span><span class="sxs-lookup"><span data-stu-id="da788-102">ClearMacroError Macro Action</span></span>


<span data-ttu-id="da788-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="da788-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="da788-104">Чтобы очистить сведения об ошибке, которая хранится в объекте **MacroError** можно использовать действие **ClearMacroError** .</span><span class="sxs-lookup"><span data-stu-id="da788-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="da788-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="da788-105">Setting</span></span>

<span data-ttu-id="da788-106">Действие **ClearMacroError** не имеет каких-либо аргументов.</span><span class="sxs-lookup"><span data-stu-id="da788-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="da788-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="da788-107">Remarks</span></span>

  - <span data-ttu-id="da788-108">При возникновении ошибки в макросе, в объекте **MacroError** хранятся сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="da788-108">When an error occurs in a macro, information about the error is stored in the **MacroError** object.</span></span> <span data-ttu-id="da788-109">Если вы не использовали **[ПриОшибке](onerror-macro-action.md)** для отмены вывода сообщений об ошибках, останавливает макросов и сведения об ошибке отображается в стандартное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="da788-109">If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message.</span></span> <span data-ttu-id="da788-110">Тем не менее если используется **ПриОшибке** для отмены вывода сообщений об ошибках, можно использовать данные, хранящиеся в объекте **MacroError** в условие или пользовательское сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="da788-110">However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
    <span data-ttu-id="da788-111">После обработки ошибки сведения в объекте **MacroError** является устаревшим, поэтому рекомендуется очистки объекта с помощью действия **ClearMacroError** .</span><span class="sxs-lookup"><span data-stu-id="da788-111">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action.</span></span> <span data-ttu-id="da788-112">Это номер ошибки в объекте **MacroError** восстанавливаются значения по умолчанию 0 и очищает любые другие сведения об ошибке, хранящиеся в объекте, такие как описание ошибки, имя макроса, имя действия, условия и аргументы.</span><span class="sxs-lookup"><span data-stu-id="da788-112">Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments.</span></span> <span data-ttu-id="da788-113">Таким образом, можно проверить объект **MacroError** попытку позже для просмотра, если другой ошибки.</span><span class="sxs-lookup"><span data-stu-id="da788-113">This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

  - <span data-ttu-id="da788-114">Объект **MacroError** автоматически очищается после завершения любой макрос, необходимо использовать действие **ClearMacroError** в конце макроса.</span><span class="sxs-lookup"><span data-stu-id="da788-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

  - <span data-ttu-id="da788-115">Объект **MacroError** содержит сведения об ошибке только один за раз.</span><span class="sxs-lookup"><span data-stu-id="da788-115">The **MacroError** object contains information about only one error at a time.</span></span> <span data-ttu-id="da788-116">Если более одного ошибка в макросе, объект **MacroError** содержит сведения только о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="da788-116">If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

  - <span data-ttu-id="da788-117">Чтобы выполнить действие **ClearMacroError** в модуле VBA, используйте метод **ClearMacroError** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="da788-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="da788-118">Пример</span><span class="sxs-lookup"><span data-stu-id="da788-118">Example</span></span>

<span data-ttu-id="da788-119">Следующий макрос использует **ПриОшибке** с **следующий** аргумент для отмены вывода сообщений об ошибках, а затем использует **ОткрытьФорму** для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="da788-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="da788-120">В данном примере ошибка намеренно создается с помощью **НаЗапись** для перехода к предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="da788-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="da788-121">Условие \*\* \[MacroError\].\[ Номер\]\<\>0\*\* тестирует объект **MacroError** .</span><span class="sxs-lookup"><span data-stu-id="da788-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="da788-122">Если произошла ошибка, номер ошибки не равно нулю, и выполняется действие **MessageBox** .</span><span class="sxs-lookup"><span data-stu-id="da788-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="da788-123">В окне сообщения отображается имя действия, вызвавшей ошибку (в данном случае **НаЗапись** ), и отображается номер ошибки.</span><span class="sxs-lookup"><span data-stu-id="da788-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="da788-124">И, наконец выполнение действия **ClearMacroError** удаляет объект **MacroError** .</span><span class="sxs-lookup"><span data-stu-id="da788-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da788-125">Condition</span><span class="sxs-lookup"><span data-stu-id="da788-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="da788-126">Действие</span><span class="sxs-lookup"><span data-stu-id="da788-126">Action</span></span></p></th>
<th><p><span data-ttu-id="da788-127">Аргументы</span><span class="sxs-lookup"><span data-stu-id="da788-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="da788-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="da788-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="da788-129"><strong>Перейдите к</strong>: <strong>Далее</strong></span><span class="sxs-lookup"><span data-stu-id="da788-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="da788-130"><strong>ОткрытьФорму</strong></span><span class="sxs-lookup"><span data-stu-id="da788-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="da788-131"><strong>Имя формы</strong>: CategoryForm<strong>представление</strong>: <strong>Режим FormWindow</strong>: <strong>Обычный</strong></span><span class="sxs-lookup"><span data-stu-id="da788-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="da788-132"><strong>GoToRecord</strong></span><span class="sxs-lookup"><span data-stu-id="da788-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="da788-133"><strong>Тип объекта</strong>: <strong>Имя FormObject</strong>: CategoryForm<strong>запись</strong>: предыдущей</span><span class="sxs-lookup"><span data-stu-id="da788-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da788-134">[MacroError]. [Число] &lt; &gt;0</span><span class="sxs-lookup"><span data-stu-id="da788-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="da788-135"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="da788-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="da788-136"><strong>Сообщение</strong>: =&quot;ошибка # &quot; &amp; [MacroError]. [Число] &amp; &quot; на &quot; &amp; [MacroError]. [Имя действия] &amp; &quot; действие. &quot; <strong>Звуковые сигналы</strong>: <strong>YesType</strong>: сведения</span><span class="sxs-lookup"><span data-stu-id="da788-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="da788-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="da788-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

