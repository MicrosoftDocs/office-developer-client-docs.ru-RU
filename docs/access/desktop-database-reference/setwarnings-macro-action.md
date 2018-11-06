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
ms.openlocfilehash: 7642c7a727853005cb6cf664bf44f29bcd6e14ed
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997974"
---
# <a name="setwarnings-macro-action"></a><span data-ttu-id="a39ac-102">Макрокоманда SetWarnings</span><span class="sxs-lookup"><span data-stu-id="a39ac-102">SetWarnings macro action</span></span>

<span data-ttu-id="a39ac-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a39ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a39ac-104">Действие **УстановитьСообщения** можно использовать для включения системные сообщения включено или отключено.</span><span class="sxs-lookup"><span data-stu-id="a39ac-104">You can use the **SetWarnings** action to turn system messages on or off.</span></span>

> [!NOTE]
> <span data-ttu-id="a39ac-105">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="a39ac-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="a39ac-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="a39ac-106">Setting</span></span>

<span data-ttu-id="a39ac-107">Действие **УстановитьСообщения** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="a39ac-107">The **SetWarnings** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a39ac-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="a39ac-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a39ac-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a39ac-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a39ac-110"><strong>Предупреждения на</strong></span><span class="sxs-lookup"><span data-stu-id="a39ac-110"><strong>Warnings On</strong></span></span></p></td>
<td><p><span data-ttu-id="a39ac-111">Указывает, отображаются ли системные сообщения.</span><span class="sxs-lookup"><span data-stu-id="a39ac-111">Specifies whether system messages are displayed.</span></span> <span data-ttu-id="a39ac-112">Нажмите кнопку <strong>Да</strong> (Чтобы включить системные сообщения) или <strong>Нет</strong> (для отключения системные сообщения) в <strong>Предупреждений на</strong> поле в разделе <strong>Действие аргументы</strong> области конструктор макросов.</span><span class="sxs-lookup"><span data-stu-id="a39ac-112">Click <strong>Yes</strong> (to turn on system messages) or <strong>No</strong> (to turn off system messages) in the <strong>Warnings On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder Pane.</span></span> <span data-ttu-id="a39ac-113">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="a39ac-113">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a39ac-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="a39ac-114">Remarks</span></span>

<span data-ttu-id="a39ac-115">Это действие можно использовать для предотвращения модальные окна предупреждения и окнах сообщений в каждом окне.</span><span class="sxs-lookup"><span data-stu-id="a39ac-115">You can use this action to prevent modal warnings and message boxes from stopping the macro.</span></span> <span data-ttu-id="a39ac-116">Тем не менее всегда отображаются сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="a39ac-116">However, error messages are always displayed.</span></span> <span data-ttu-id="a39ac-117">Кроме того, Microsoft Access отображает все диалоговые окна, требующие ввода данных, отличных от простого нажатия кнопок (например, **кнопку ОК**, **Отменить**, **Да**или **Нет**), к примеру, любое диалоговое окно, которое требуется для ввода текста или выберите один из несколько вариантов .</span><span class="sxs-lookup"><span data-stu-id="a39ac-117">Also, Microsoft Access displays any dialog boxes that require input other than just choosing a button (such as **OK**, **Cancel**, **Yes**, or **No**) — for example, any dialog box that requires you to enter text or select one of several options.</span></span>

<span data-ttu-id="a39ac-118">Выполнение этого действия с **В** аргументе значение **Нет** имеет тот же эффект, как при нажатии клавиши ВВОД каждый раз, когда отображается предупреждение или окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="a39ac-118">Carrying out this action with the **Warnings On** argument set to **No** has the same effect as pressing ENTER whenever a warning or message box is displayed.</span></span> <span data-ttu-id="a39ac-119">Как правило **ОК** или **Да** кнопка выбирается в ответ на предупреждения или сообщения.</span><span class="sxs-lookup"><span data-stu-id="a39ac-119">Typically, an **OK** or **Yes** button is chosen in response to the warning or message.</span></span>

<span data-ttu-id="a39ac-120">После завершения макроса Microsoft Access автоматически включает вывод системных сообщений обратно на.</span><span class="sxs-lookup"><span data-stu-id="a39ac-120">When the macro finishes, Access automatically turns the display of system messages back on.</span></span>

<span data-ttu-id="a39ac-121">Часто используется это действие с действием **эхо** , который позволяет скрыть результаты макроса до его завершения.</span><span class="sxs-lookup"><span data-stu-id="a39ac-121">Often, you'll use this action with the **Echo** action, which hides the results of a macro until it's finished.</span></span> <span data-ttu-id="a39ac-122">Чтобы скрыть предупреждения и окнах сообщений также можно использовать действие **УстановитьСообщения** .</span><span class="sxs-lookup"><span data-stu-id="a39ac-122">You can use the **SetWarnings** action to hide the warnings and message boxes as well.</span></span>

> [!WARNING]
> <span data-ttu-id="a39ac-123">Несмотря на то, что действие **УстановитьСообщения** упрощает взаимодействие с макросами, необходимо соблюдать осторожность отключение системные сообщения.</span><span class="sxs-lookup"><span data-stu-id="a39ac-123">Although the **SetWarnings** action can simplify interactions with macros, you must be careful about turning system messages off.</span></span> <span data-ttu-id="a39ac-124">В некоторых случаях не требуется для продолжения макроса при определенных предупреждение отображается.</span><span class="sxs-lookup"><span data-stu-id="a39ac-124">In some situations, you won't want to continue a macro if a certain warning message is displayed.</span></span> <span data-ttu-id="a39ac-125">Если вы не уверены результата все действия макроса, следует использовать это действие.</span><span class="sxs-lookup"><span data-stu-id="a39ac-125">Unless you're confident of the outcome of all macro actions, you should avoid using this action.</span></span>

<span data-ttu-id="a39ac-126">Чтобы выполнить действие **УстановитьСообщения** в Visual Basic для приложений (VBA) модуль, используйте метод **УстановитьСообщения** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="a39ac-126">To run the **SetWarnings** action in a Visual Basic for Applications (VBA) module, use the **SetWarnings** method of the **DoCmd** object.</span></span>

