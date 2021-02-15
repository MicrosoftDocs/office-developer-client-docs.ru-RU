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
# <a name="closewindow-macro-action"></a><span data-ttu-id="946c1-102">Макрокоманда CloseWindow</span><span class="sxs-lookup"><span data-stu-id="946c1-102">CloseWindow macro action</span></span>


<span data-ttu-id="946c1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="946c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="946c1-104">С помощью действия **CloseWindow** можно закрыть указанную вкладку документа Access или активную вкладку документа, если она не указана.</span><span class="sxs-lookup"><span data-stu-id="946c1-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="946c1-105">Setting</span><span class="sxs-lookup"><span data-stu-id="946c1-105">Setting</span></span>

<span data-ttu-id="946c1-106">Действие **CloseWindow** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="946c1-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="946c1-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="946c1-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="946c1-108">Описание</span><span class="sxs-lookup"><span data-stu-id="946c1-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="946c1-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="946c1-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="946c1-110">Тип объекта, вкладку документа которого нужно закрыть.</span><span class="sxs-lookup"><span data-stu-id="946c1-110">The type of object whose document tab you want to close.</span></span> <span data-ttu-id="946c1-111">Щелкните <strong>"Таблица",</strong>"Запрос", "Форма", "Отчет", "Макрос", <strong></strong> "Модуль", <strong></strong> "Страница доступа к данным", "Представление сервера", "Схема", "Хранимая процедура" или "Функция" в поле "Тип объекта" в разделе "Аргументы действий" области построитель макроса. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="946c1-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="946c1-112">Чтобы выбрать активную вкладку документа, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="946c1-112">To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="946c1-113">При закрытии модуля в редакторе Visual Basic необходимо использовать **модуль** в аргументе **"Тип объекта".**</span><span class="sxs-lookup"><span data-stu-id="946c1-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="946c1-114"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="946c1-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="946c1-115">Имя объекта, который необходимо закрыть.</span><span class="sxs-lookup"><span data-stu-id="946c1-115">The name of the object to be closed.</span></span> <span data-ttu-id="946c1-116">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="946c1-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="946c1-117">Щелкните объект, чтобы закрыть его.</span><span class="sxs-lookup"><span data-stu-id="946c1-117">Click the object to close.</span></span> <span data-ttu-id="946c1-118">Если оставить аргумент <strong>Object Type</strong> пустым, также оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="946c1-118">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="946c1-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="946c1-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="946c1-120">Следует ли сохранять изменения в объекте при его закрытии.</span><span class="sxs-lookup"><span data-stu-id="946c1-120">Whether to save changes to the object when it is closed.</span></span> <span data-ttu-id="946c1-121">Нажмите <strong>кнопку "Да"</strong> (сохранить объект), <strong>"Нет"</strong> (закроем объект без сохранения) или <strong>"Запрос"</strong> (запросите у пользователя, нужно ли сохранять объект).</span><span class="sxs-lookup"><span data-stu-id="946c1-121">Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object).</span></span> <span data-ttu-id="946c1-122">Значение по умолчанию — <strong>Prompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="946c1-122">The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="946c1-123">Заметки</span><span class="sxs-lookup"><span data-stu-id="946c1-123">Remarks</span></span>

<span data-ttu-id="946c1-124">Действие **CloseWindow** работает на всех объектах базы данных, которые пользователь может явным образом открыть или закрыть.</span><span class="sxs-lookup"><span data-stu-id="946c1-124">The **CloseWindow** action works on all database objects that the user can explicitly open or close.</span></span> <span data-ttu-id="946c1-125">Это действие действует так же, как при выборе объекта и его закрытии, щелкнув правой кнопкой мыши вкладку  документа объекта, а затем нажав кнопку "Закрыть" в меню "Закрыть" или нажав кнопку "Закрыть" для объекта. </span><span class="sxs-lookup"><span data-stu-id="946c1-125">This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="946c1-126">Если для аргумента **Save** установлено имя **Prompt,** а объект еще не был сохранен до того, как будет выполнено действие **CloseWindow,** пользователю будет предложено сохранить объект, прежде чем макрос закроет его.</span><span class="sxs-lookup"><span data-stu-id="946c1-126">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it.</span></span> <span data-ttu-id="946c1-127">Если для аргумента **Warnings On** действия **SetWarnings** установлено **"Нет",** диалоговое окно не отображается, и объект автоматически сохраняются.</span><span class="sxs-lookup"><span data-stu-id="946c1-127">If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="946c1-128">Чтобы запустить действие **CloseWindow** в модуле Visual Basic для приложений (VBA), используйте метод **CloseWindow** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="946c1-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

