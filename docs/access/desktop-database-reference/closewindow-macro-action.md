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
# <a name="closewindow-macro-action"></a><span data-ttu-id="3c8f7-102">Макрокоманда CloseWindow</span><span class="sxs-lookup"><span data-stu-id="3c8f7-102">CloseWindow macro action</span></span>


<span data-ttu-id="3c8f7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c8f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c8f7-104">Вы можете использовать действие **клосевиндов** , чтобы закрыть указанную вкладку документа Access или вкладку активный документ, если ничего не указано.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="3c8f7-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="3c8f7-105">Setting</span></span>

<span data-ttu-id="3c8f7-106">Макрокоманда **клосевиндов** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c8f7-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3c8f7-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3c8f7-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3c8f7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c8f7-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="3c8f7-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="3c8f7-110">Тип объекта, для которого нужно закрыть вкладку документа.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-110">The type of object whose document tab you want to close.</span></span> <span data-ttu-id="3c8f7-111">Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>отчет</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong> в <strong>типе объекта. </strong>в разделе <strong>аргументы макрокоманды</strong> в панели построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="3c8f7-112">Чтобы выбрать вкладку активный документ, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-112">To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="3c8f7-113">При закрытии модуля в редакторе Visual Basic необходимо использовать **модуль** в аргументе " **тип объекта** ".</span><span class="sxs-lookup"><span data-stu-id="3c8f7-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3c8f7-114"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="3c8f7-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="3c8f7-115">Имя объекта, который необходимо закрыть.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-115">The name of the object to be closed.</span></span> <span data-ttu-id="3c8f7-116">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="3c8f7-117">Щелкните объект, который требуется закрыть.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-117">Click the object to close.</span></span> <span data-ttu-id="3c8f7-118">Если оставить аргумент " <strong>тип объекта</strong> " пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-118">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3c8f7-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="3c8f7-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="3c8f7-120">Указывает, следует ли сохранять изменения в объекте при его закрытии.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-120">Whether to save changes to the object when it is closed.</span></span> <span data-ttu-id="3c8f7-121">Нажмите кнопку <strong>Да</strong> (Сохранить объект), <strong>нет</strong> (закройте объект без его сохранения) или выводится <strong>запрос</strong> (запрашивать пользователя, следует ли сохранить объект).</span><span class="sxs-lookup"><span data-stu-id="3c8f7-121">Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object).</span></span> <span data-ttu-id="3c8f7-122">Значение по умолчанию — <strong>Prompt</strong>.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-122">The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3c8f7-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c8f7-123">Remarks</span></span>

<span data-ttu-id="3c8f7-124">Действие **клосевиндов** работает со всеми объектами базы данных, которые пользователь может явно открывать или закрывать.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-124">The **CloseWindow** action works on all database objects that the user can explicitly open or close.</span></span> <span data-ttu-id="3c8f7-125">Это действие имеет тот же результат, что и выбор объекта, а затем его закрытие, щелкнув вкладку документа правой кнопкой мыши и выбрав команду **Закрыть** в контекстном меню или нажав кнопку **Закрыть** для объекта.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-125">This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="3c8f7-126">Если для аргумента **Save** задано значение **Prompt** , а объект еще не был сохранен до выполнения действия **клосевиндов** , диалоговое окно предлагает пользователю сохранить объект до его закрытия макросом.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-126">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it.</span></span> <span data-ttu-id="3c8f7-127">Если для аргумента **сетварнингс** в аргументе " **предупреждения** " задано значение " **нет**", диалоговое окно не отображается и объект автоматически сохраняется.</span><span class="sxs-lookup"><span data-stu-id="3c8f7-127">If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="3c8f7-128">Чтобы запустить действие **клосевиндов** в модуле Visual Basic для приложений (VBA), используйте метод **клосевиндов** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="3c8f7-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

