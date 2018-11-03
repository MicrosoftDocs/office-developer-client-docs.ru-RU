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
ms.openlocfilehash: f9bffbd129d8fb4fc1334dbd884556d98e7f140c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929323"
---
# <a name="closewindow-macro-action"></a><span data-ttu-id="a3324-102">Макрокоманда CloseWindow</span><span class="sxs-lookup"><span data-stu-id="a3324-102">CloseWindow macro action</span></span>


<span data-ttu-id="a3324-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3324-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3324-104">Действие **CloseWindow** можно использовать для закрытия указанного вкладку документ Access или активный документ, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="a3324-104">You can use the **CloseWindow** action to close either a specified Access document tab or the active document tab if none is specified.</span></span>

## <a name="setting"></a><span data-ttu-id="a3324-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="a3324-105">Setting</span></span>

<span data-ttu-id="a3324-106">Действие **CloseWindow** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="a3324-106">The **CloseWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3324-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="a3324-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a3324-108">Описание</span><span class="sxs-lookup"><span data-stu-id="a3324-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3324-109"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="a3324-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a3324-110">Тип объекта, вкладку документа, которую нужно закрыть.</span><span class="sxs-lookup"><span data-stu-id="a3324-110">The type of object whose document tab you want to close.</span></span> <span data-ttu-id="a3324-111">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="a3324-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="a3324-112">Выберите вкладку активный документ, оставьте данный аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="a3324-112">To select the active document tab, leave this argument blank.</span></span></p>

> [!NOTE]
> <span data-ttu-id="a3324-113">При закрытии модуля в редакторе Visual Basic, необходимо использовать **модуль** в аргументе **Тип объекта** .</span><span class="sxs-lookup"><span data-stu-id="a3324-113">If you are closing a module in the Visual Basic Editor, you must use **Module** in the **Object Type** argument.</span></span>


<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3324-114"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="a3324-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="a3324-115">Имя возвращаемого объекта будет закрыто.</span><span class="sxs-lookup"><span data-stu-id="a3324-115">The name of the object to be closed.</span></span> <span data-ttu-id="a3324-116">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="a3324-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="a3324-117">Щелкните объект, чтобы закрыть.</span><span class="sxs-lookup"><span data-stu-id="a3324-117">Click the object to close.</span></span> <span data-ttu-id="a3324-118">Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="a3324-118">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3324-119"><strong>Save</strong></span><span class="sxs-lookup"><span data-stu-id="a3324-119"><strong>Save</strong></span></span></p></td>
<td><p><span data-ttu-id="a3324-120">Следует ли сохранить изменения в объекте при ее закрытии.</span><span class="sxs-lookup"><span data-stu-id="a3324-120">Whether to save changes to the object when it is closed.</span></span> <span data-ttu-id="a3324-121">Нажмите кнопку <strong>Yes</strong> (Сохранить объект), <strong>No</strong> (закрытия объекта без сохранения), и не <strong>запрашивать пользователя</strong> (запрашивать у пользователя ли сохранить объект).</span><span class="sxs-lookup"><span data-stu-id="a3324-121">Click <strong>Yes</strong> (save the object), <strong>No</strong> (close the object without saving it), or <strong>Prompt</strong> (prompt the user whether or not to save the object).</span></span> <span data-ttu-id="a3324-122">Значение по умолчанию — <strong>приглашения</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3324-122">The default is <strong>Prompt</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3324-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="a3324-123">Remarks</span></span>

<span data-ttu-id="a3324-124">Действие **CloseWindow** работает на все объекты базы данных, которые пользователь может явно открыть или закрыть.</span><span class="sxs-lookup"><span data-stu-id="a3324-124">The **CloseWindow** action works on all database objects that the user can explicitly open or close.</span></span> <span data-ttu-id="a3324-125">Это действие имеет тот же эффект, как при выборе объекта и закрывая его, щелкнув правой кнопкой мыши вкладку документа объекта и затем нажмите кнопку **Закрыть** в контекстном меню или нажав кнопку **Закрыть** для объекта.</span><span class="sxs-lookup"><span data-stu-id="a3324-125">This action has the same effect as selecting an object and then closing it by right-clicking the object's document tab and then clicking **Close** on the shortcut menu, or clicking the **Close** button for the object.</span></span>

<span data-ttu-id="a3324-126">Если аргумент **Сохранить** задано значение **запроса** и объект не был сохранен перед выполняемые действия **CloseWindow** , диалоговое окно предлагать пользователю сохранить объект макрос закрывает его.</span><span class="sxs-lookup"><span data-stu-id="a3324-126">If the **Save** argument is set to **Prompt** and the object hasn't already been saved before the **CloseWindow** action is carried out, a dialog box prompts the user to save the object before the macro closes it.</span></span> <span data-ttu-id="a3324-127">Если выбрать **В** аргументе действие **УстановитьСообщения** **Нет**диалоговое окно не отображается и объект автоматически сохраняются.</span><span class="sxs-lookup"><span data-stu-id="a3324-127">If you have set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box is not displayed and the object is automatically saved.</span></span>

<span data-ttu-id="a3324-128">Чтобы выполнить действие **CloseWindow** в Visual Basic для приложений (VBA) модуль, используйте метод **CloseWindow** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="a3324-128">To run the **CloseWindow** action in a Visual Basic for Applications (VBA) module, use the **CloseWindow** method of the **DoCmd** object.</span></span>

