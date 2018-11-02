---
title: Макрокоманда SetWarnings
TOCTitle: SetWarnings macro action
ms:assetid: ff95b919-b1ee-c0a0-851d-71894851bb1d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837313(v=office.15)
ms:contentKeyID: 48548965
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165020
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d72a594a09196f5061ede52b4fbcbbc2cf96253c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923163"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="51724-102">Макрокоманда SetWarnings</span><span class="sxs-lookup"><span data-stu-id="51724-102">SetWarnings macro action</span></span>


<span data-ttu-id="51724-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51724-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51724-104">Действие **УстановитьСообщения** можно использовать для включения системные сообщения включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="51724-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>


> [!NOTE]
> <P><span data-ttu-id="51724-p101">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="51724-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="51724-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="51724-107">Setting</span></span>

<span data-ttu-id="51724-108">Действие **УстановитьСообщения** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="51724-108">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51724-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="51724-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="51724-110">Описание</span><span class="sxs-lookup"><span data-stu-id="51724-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51724-111"><strong>Предупреждения на</strong></span><span class="sxs-lookup"><span data-stu-id="51724-111"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="51724-112">Указывает, отображаются ли системные сообщения.</span><span class="sxs-lookup"><span data-stu-id="51724-112">Specifies whether system messages are displayed.</span></span> <span data-ttu-id="51724-113">Нажмите кнопку <strong>Да</strong> (Чтобы включить системные сообщения) или <strong>Нет</strong> (для отключения системные сообщения) в <strong>Предупреждений на</strong> поле в разделе <strong>Действие аргументы</strong> области конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="51724-113">Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane.</span></span> <span data-ttu-id="51724-114">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="51724-114">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="51724-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="51724-115">Remarks</span></span>

<span data-ttu-id="51724-116">Это действие можно использовать для предотвращения модальные окна предупреждения и окнах сообщений в каждом окне.</span><span class="sxs-lookup"><span data-stu-id="51724-116">You can use this action to prevent modal warnings and message boxes from stopping the macro.</span></span> <span data-ttu-id="51724-117">Тем не менее всегда отображаются сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="51724-117">However, error messages are always displayed.</span></span> <span data-ttu-id="51724-118">Кроме того, Microsoft Access отображает все диалоговые окна, требующие ввода данных, отличных от простого нажатия кнопок (например, **кнопку ОК**, **Отменить**, **Да**или **Нет**), к примеру, любое диалоговое окно, которое требуется для ввода текста или выберите один из несколько вариантов .</span><span class="sxs-lookup"><span data-stu-id="51724-118">Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="51724-119">Выполнение этого действия с **В** аргументе значение **Нет** имеет тот же эффект, как при нажатии клавиши ВВОД каждый раз, когда отображается предупреждение или окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="51724-119">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed.</span></span> <span data-ttu-id="51724-120">Как правило **ОК** или **Да** кнопка выбирается в ответ на предупреждения или сообщения.</span><span class="sxs-lookup"><span data-stu-id="51724-120">Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="51724-121">После завершения макроса Microsoft Access автоматически включает вывод системных сообщений обратно на.</span><span class="sxs-lookup"><span data-stu-id="51724-121">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="51724-122">Часто используется это действие с действием **эхо** , который позволяет скрыть результаты макроса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="51724-122">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished.</span></span> <span data-ttu-id="51724-123">Чтобы скрыть предупреждения и окнах сообщений также можно использовать действие **УстановитьСообщения** .</span><span class="sxs-lookup"><span data-stu-id="51724-123">You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>


> [!WARNING]
> <P><span data-ttu-id="51724-124">Несмотря на то, что действие <STRONG>УстановитьСообщения</STRONG> упрощает взаимодействие с макросами, необходимо соблюдать осторожность отключение системные сообщения.</span><span class="sxs-lookup"><span data-stu-id="51724-124">Although the <STRONG>SetWarnings</STRONG> action can simplify interactions with macros, you must be careful about turning system messages off.</span></span> <span data-ttu-id="51724-125">В некоторых случаях не требуется для продолжения макроса при определенных предупреждение отображается.</span><span class="sxs-lookup"><span data-stu-id="51724-125">In some situations, you won't want to continue a macro if a certain warning message is displayed.</span></span> <span data-ttu-id="51724-126">Если вы не уверены результата все действия макроса, следует использовать это действие.</span><span class="sxs-lookup"><span data-stu-id="51724-126">Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span></P>



<span data-ttu-id="51724-127">Чтобы выполнить действие **УстановитьСообщения** в Visual Basic для приложений (VBA) модуль, используйте метод **УстановитьСообщения** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="51724-127">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

