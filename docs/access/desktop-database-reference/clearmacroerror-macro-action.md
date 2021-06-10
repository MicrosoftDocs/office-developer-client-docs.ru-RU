---
title: Макрокоманда ClearMacroError
TOCTitle: ClearMacroError macro action
ms:assetid: 1091747e-e957-38c6-6454-5169f091323e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845338(v=office.15)
ms:contentKeyID: 48543296
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm109100
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f42386674ff76d550fb47a971860b4e1a5905236
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296376"
---
# <a name="clearmacroerror-macro-action"></a><span data-ttu-id="ad437-102">Макрокоманда ClearMacroError</span><span class="sxs-lookup"><span data-stu-id="ad437-102">ClearMacroError macro action</span></span>


<span data-ttu-id="ad437-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad437-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="ad437-104">Вы можете использовать **действие ClearMacroError** для очистки сведений об ошибке, хранимой в объекте **MacroError.**</span><span class="sxs-lookup"><span data-stu-id="ad437-104">You can use the **ClearMacroError** action to clear information about an error that is stored in the **MacroError** object.</span></span>

## <a name="setting"></a><span data-ttu-id="ad437-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="ad437-105">Setting</span></span>

<span data-ttu-id="ad437-106">Действие **ClearMacroError** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="ad437-106">The **ClearMacroError** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad437-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad437-107">Remarks</span></span>

- <span data-ttu-id="ad437-108">При ошибке макроса сведения об ошибке хранятся в объекте **MacroError.**</span><span class="sxs-lookup"><span data-stu-id="ad437-108">When an error occurs in a macro, information about the error is stored in the **MacroError** object.</span></span> <span data-ttu-id="ad437-109">Если вы не использовали действие **[OnError](onerror-macro-action.md)** для подавления сообщений об ошибках, макрос останавливается, а сведения об ошибках отображаются в стандартном сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ad437-109">If you have not used the **[OnError](onerror-macro-action.md)** action to suppress error messages, the macro stops and the error information is displayed in a standard error message.</span></span> <span data-ttu-id="ad437-110">Однако если для подавления сообщений об ошибках используется действие **OnError,** может потребоваться использовать сведения, хранимые в объекте **MacroError** в состоянии или в настраиваемом сообщении об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ad437-110">However, if you have used the **OnError** action to suppress error messages, you might want to use the information stored in the **MacroError** object in a condition or in a custom error message.</span></span>
    
  <span data-ttu-id="ad437-111">После обработки ошибки сведения в объекте **MacroError** устарели, поэтому лучше очистить объект с помощью действия **ClearMacroError.**</span><span class="sxs-lookup"><span data-stu-id="ad437-111">After an error has been handled, the information in the **MacroError** object is out of date, so it is a good idea to clear the object by using the **ClearMacroError** action.</span></span> <span data-ttu-id="ad437-112">При этом номер ошибки в объекте **MacroError** сбрасывается до 0 и очищается от любых других сведений об ошибке, хранимой в объекте, таких как описание ошибки, имя макроса, имя действия, состояние и аргументы.</span><span class="sxs-lookup"><span data-stu-id="ad437-112">Doing so resets the error number in the **MacroError** object to 0 and clears any other information about the error that is stored in the object, such as the error description, macro name, action name, condition, and arguments.</span></span> <span data-ttu-id="ad437-113">Таким образом, вы можете проверить объект **MacroError** еще раз позже, чтобы узнать, произошла ли еще одна ошибка.</span><span class="sxs-lookup"><span data-stu-id="ad437-113">This way, you can inspect the **MacroError** object again later to see if another error has occurred.</span></span>

- <span data-ttu-id="ad437-114">Объект **MacroError** автоматически очищается после окончания макроса, поэтому в конце макроса не требуется использовать действие **ClearMacroError.**</span><span class="sxs-lookup"><span data-stu-id="ad437-114">The **MacroError** object is automatically cleared when any macro ends, so you do not need to use the **ClearMacroError** action at the end of a macro.</span></span>

- <span data-ttu-id="ad437-115">Объект **MacroError содержит** сведения только об одной ошибке одновременно.</span><span class="sxs-lookup"><span data-stu-id="ad437-115">The **MacroError** object contains information about only one error at a time.</span></span> <span data-ttu-id="ad437-116">Если на макросе произошло несколько ошибок, объект **MacroError** содержит сведения только о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="ad437-116">If more than one error has occurred in a macro, the **MacroError** object contains information only about the last error.</span></span>

- <span data-ttu-id="ad437-117">Чтобы выполнить **действие ClearMacroError** в модуле VBA, используйте метод **ClearMacroError** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="ad437-117">To run the **ClearMacroError** action in a VBA module, use the **ClearMacroError** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="ad437-118">Пример</span><span class="sxs-lookup"><span data-stu-id="ad437-118">Example</span></span>

<span data-ttu-id="ad437-119">Следующий макрос использует действие **OnError** с аргументом **Next** для подавления сообщений об ошибках, а затем использует **действие OpenForm** для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="ad437-119">The following macro uses the **OnError** action with the **Next** argument to suppress error messages, and then uses the **OpenForm** action to open a form.</span></span> <span data-ttu-id="ad437-120">В этом примере ошибка намеренно создается с помощью **действия GoToRecord** для перейти к предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="ad437-120">For this example, an error is deliberately created by using the **GoToRecord** action to go to the previous record.</span></span> <span data-ttu-id="ad437-121">Условие **\[ MacroError \] . \[ Номер \] \< \> 0** проверяет **объект MacroError.**</span><span class="sxs-lookup"><span data-stu-id="ad437-121">The condition **\[MacroError\].\[Number\]\<\>0** tests the **MacroError** object.</span></span> <span data-ttu-id="ad437-122">Если произошла ошибка, номер ошибки не нулевой, а действие **MessageBox** выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad437-122">If an error has occurred, the error number is non-zero, and the **MessageBox** action runs.</span></span> <span data-ttu-id="ad437-123">В поле сообщений отображается имя действия, вызываемого ошибкой (в данном случае действия **GoToRecord),** и отображается номер ошибки.</span><span class="sxs-lookup"><span data-stu-id="ad437-123">The message box displays the name of the action that caused the error (in this case, the **GoToRecord** action), and the error number is displayed.</span></span> <span data-ttu-id="ad437-124">Наконец, при запуске **действия ClearMacroError** очищается **объект MacroError.**</span><span class="sxs-lookup"><span data-stu-id="ad437-124">Finally, running the **ClearMacroError** action clears the **MacroError** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ad437-125">Условие</span><span class="sxs-lookup"><span data-stu-id="ad437-125">Condition</span></span></p></th>
<th><p><span data-ttu-id="ad437-126">Action</span><span class="sxs-lookup"><span data-stu-id="ad437-126">Action</span></span></p></th>
<th><p><span data-ttu-id="ad437-127">Аргументы</span><span class="sxs-lookup"><span data-stu-id="ad437-127">Arguments</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ad437-128"><strong>OnError</strong></span><span class="sxs-lookup"><span data-stu-id="ad437-128"><strong>OnError</strong></span></span></p></td>
<td><p><span data-ttu-id="ad437-129"><strong>Перейти к</strong>: <strong>Далее</strong></span><span class="sxs-lookup"><span data-stu-id="ad437-129"><strong>Go to</strong>: <strong>Next</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="ad437-130"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="ad437-130"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="ad437-131"><strong>Имя формы:</strong>Представление<strong></strong>CategoryForm : <strong>FormWindow Mode</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="ad437-131"><strong>Form Name</strong>: CategoryForm<strong>View</strong>: <strong>FormWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ad437-132"><strong>GoToRecord</strong></span><span class="sxs-lookup"><span data-stu-id="ad437-132"><strong>GoToRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="ad437-133"><strong>Тип объекта:</strong> <strong>Имя FormObject</strong>: CategoryForm<strong>Record</strong>: Previous</span><span class="sxs-lookup"><span data-stu-id="ad437-133"><strong>Object Type</strong>: <strong>FormObject Name</strong>: CategoryForm<strong>Record</strong>: Previous</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad437-134">[MacroError]. [Номер] &lt; &gt; 0</span><span class="sxs-lookup"><span data-stu-id="ad437-134">[MacroError].[Number]&lt;&gt;0</span></span></p></td>
<td><p><span data-ttu-id="ad437-135"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="ad437-135"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="ad437-136"><strong>Сообщение:</strong>= &quot; Ошибка # &quot; &amp; [MacroError].[ Номер] &amp; &quot; &quot; &amp; на [MacroError].[ Действие &amp; &quot; ActionName. &quot; <strong>Звуковой сигнал:</strong> <strong>YesType</strong>: Информация</span><span class="sxs-lookup"><span data-stu-id="ad437-136"><strong>Message</strong>: =&quot;Error # &quot; &amp; [MacroError].[Number] &amp; &quot; on &quot; &amp; [MacroError].[ActionName] &amp; &quot; action.&quot;<strong>Beep</strong>: <strong>YesType</strong>: Information</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="ad437-137"><strong>ClearMacroError</strong></span><span class="sxs-lookup"><span data-stu-id="ad437-137"><strong>ClearMacroError</strong></span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

