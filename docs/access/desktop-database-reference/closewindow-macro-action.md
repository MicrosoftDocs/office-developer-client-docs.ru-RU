---
title: Макрокоманда CloseWindow
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4397846abdc0d10b6bfa0e6a1eb5c0c435fc862a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296292"
---
# <a name="closewindow-macro-action"></a><span data-ttu-id="00997-102">Макрокоманда CloseWindow</span><span class="sxs-lookup"><span data-stu-id="00997-102">CloseWindow macro action</span></span>


<span data-ttu-id="00997-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00997-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="00997-104">Действие **CloseWindow** можно использовать для закрытия указанной вкладки документа Access или активной вкладки документа, если ее нет.</span><span class="sxs-lookup"><span data-stu-id="00997-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="00997-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="00997-105">Setting</span></span>

<span data-ttu-id="00997-106">Действие **CloseWindow** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="00997-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="00997-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="00997-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="00997-108">Описание</span><span class="sxs-lookup"><span data-stu-id="00997-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="00997-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="00997-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="00997-110">Тип объекта, на вкладке документа которого необходимо закрыть.</span><span class="sxs-lookup"><span data-stu-id="00997-110">The type of object whose document tab you want to close.</span></span> <span data-ttu-id="00997-111"><strong>Щелкните</strong> <strong>таблицу,</strong> <strong>запрос,</strong>форма, отчет, макрос, модуль, <strong></strong> <strong></strong>страница доступа <strong></strong> к данным, представление сервера, схема, сохраненная процедура или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="00997-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="00997-112">Чтобы выбрать активную вкладку документа, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="00997-112">To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="00997-113">Если вы закрываете модуль в редакторе Visual Basic, необходимо использовать **модуль** в **аргументе Object Type.**</span><span class="sxs-lookup"><span data-stu-id="00997-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="00997-114"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="00997-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="00997-115">Имя объекта, который будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="00997-115">The name of the object to be closed.</span></span> <span data-ttu-id="00997-116">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="00997-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="00997-117">Щелкните объект, чтобы закрыть.</span><span class="sxs-lookup"><span data-stu-id="00997-117">Click the object to close.</span></span> <span data-ttu-id="00997-118">Если оставить аргумент <strong>Object Type</strong> пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="00997-118">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="00997-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="00997-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="00997-120">Следует ли сохранять изменения в объекте при его закрытии.</span><span class="sxs-lookup"><span data-stu-id="00997-120">Whether to save changes to the object when it is closed.</span></span> <span data-ttu-id="00997-121">Нажмите <strong>кнопку Да</strong> (сохраните объект), <strong>Нет</strong> (закрой объект, не сэкономив его) или Запрос <strong>(подскажут</strong> пользователю, следует ли сохранять объект).</span><span class="sxs-lookup"><span data-stu-id="00997-121">Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object).</span></span> <span data-ttu-id="00997-122">По умолчанию — <strong>запрос</strong>.</span><span class="sxs-lookup"><span data-stu-id="00997-122">The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="00997-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="00997-123">Remarks</span></span>

<span data-ttu-id="00997-124">Действие **CloseWindow работает** на всех объектах базы данных, которые пользователь может открыто открыть или закрыть.</span><span class="sxs-lookup"><span data-stu-id="00997-124">The **CloseWindow** action works on all database objects that the user can explicitly open or close.</span></span> <span data-ttu-id="00997-125">Это действие имеет тот же эффект, что и выбор объекта, а затем его закрытие, щелкнув правой кнопкой мыши  вкладку документа объекта, а затем щелкнув кнопку **Закрыть** в меню ярлык, или нажав кнопку Закрыть для объекта.</span><span class="sxs-lookup"><span data-stu-id="00997-125">This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="00997-126">Если для аргумента **Сохранить** установлено имя **"Запрос",** а объект еще не был сохранен до того, как будет выполнено действие **CloseWindow,** диалоговое окно подсказает пользователю сохранить объект до закрытия макроса.</span><span class="sxs-lookup"><span data-stu-id="00997-126">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it.</span></span> <span data-ttu-id="00997-127">Если для аргумента действия **SetWarnings** заочно установлено предупреждение, диалоговое окно не отображается, и объект автоматически сберегается. </span><span class="sxs-lookup"><span data-stu-id="00997-127">If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="00997-128">Чтобы выполнить действие **CloseWindow** в Visual Basic для приложений (VBA), используйте метод **CloseWindow** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="00997-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

