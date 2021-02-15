---
title: Макрокоманда SaveObject
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: cf6fe02616134f864a0e07092951ab9cf49aadbc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308934"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="6b5db-102">Макрокоманда SaveObject</span><span class="sxs-lookup"><span data-stu-id="6b5db-102">SaveObject macro action</span></span>

<span data-ttu-id="6b5db-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b5db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b5db-104">С помощью действия **SaveObject** можно сохранить либо указанный объект Access, либо активный объект, если не задан ни один из них.</span><span class="sxs-lookup"><span data-stu-id="6b5db-104">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified.</span></span> <span data-ttu-id="6b5db-105">В некоторых случаях можно также сохранить активный объект с новым именем (это выполняется так же, как команда **"Сохранить** как" на панели быстрого **доступа).**</span><span class="sxs-lookup"><span data-stu-id="6b5db-105">You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="6b5db-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="6b5db-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="6b5db-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="6b5db-107">Setting</span></span>

<span data-ttu-id="6b5db-108">Действие **SaveObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6b5db-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b5db-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="6b5db-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="6b5db-110">Описание</span><span class="sxs-lookup"><span data-stu-id="6b5db-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b5db-111"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="6b5db-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="6b5db-112">Тип объекта, который нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="6b5db-112">The type of object you want to save.</span></span> <span data-ttu-id="6b5db-113">Щелкните <strong>"Таблица",</strong>"Запрос", "Форма", "Отчет", "Макрос", <strong></strong> "Модуль", <strong></strong> "Страница доступа к данным", "Представление сервера", "Схема", "Хранимая процедура" или "Функция" в поле "Тип объекта" в разделе "Аргументы действий" области построитель макроса. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="6b5db-113">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="6b5db-114">Чтобы выбрать активный объект, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="6b5db-114">To select the active object, leave this argument blank.</span></span> <span data-ttu-id="6b5db-115">При выборе типа объекта в этом аргументе необходимо выбрать имя существующего объекта в <strong>аргументе Object Name.</strong></span><span class="sxs-lookup"><span data-stu-id="6b5db-115">If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b5db-116"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="6b5db-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="6b5db-117">Имя объекта, который необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="6b5db-117">The name of the object to be saved.</span></span> <span data-ttu-id="6b5db-118">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b5db-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="6b5db-119">Если оставить аргумент <strong>Object Type</strong> пустым, можно оставить этот аргумент пустым, чтобы сохранить активный объект, или, в некоторых случаях, ввести новое имя в этом аргументе, чтобы сохранить активный объект с этим именем.</span><span class="sxs-lookup"><span data-stu-id="6b5db-119">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="6b5db-120">Если ввести новое имя, имя должно следовать стандартным соглашениям об именовывом имени для объектов Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6b5db-120">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6b5db-121">Заметки</span><span class="sxs-lookup"><span data-stu-id="6b5db-121">Remarks</span></span>

<span data-ttu-id="6b5db-122">Действие **SaveObject работает** со всеми объектами базы данных, которые пользователь может явным образом открыть и сохранить.</span><span class="sxs-lookup"><span data-stu-id="6b5db-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="6b5db-123">Указанный объект должен быть открыт, чтобы действие **SaveObject** как-либо влияло на объект.</span><span class="sxs-lookup"><span data-stu-id="6b5db-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="6b5db-124">Это действие действует так же, как при выборе объекта и его сохранении, нажав кнопку **"Сохранить"** на панели быстрого **доступа.**</span><span class="sxs-lookup"><span data-stu-id="6b5db-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> 

<span data-ttu-id="6b5db-125">Оставление аргумента Object **Type** пустым и ввод нового имени в  аргументе Object  **Name** имеет тот же эффект, что и нажатие кнопки "Сохранить как" на панели быстрого доступа и ввод нового имени активного объекта.</span><span class="sxs-lookup"><span data-stu-id="6b5db-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="6b5db-126">С помощью **действия SaveObject** можно указать объект для сохранения и выполнить команду **"Сохранить** как" из макроса.</span><span class="sxs-lookup"><span data-stu-id="6b5db-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="6b5db-127">С помощью действия **SaveObject** нельзя сохранить любое из следующих проектов с новым именем:</span><span class="sxs-lookup"><span data-stu-id="6b5db-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="6b5db-128">Форма в представлении формы или в представлении таблицы</span><span class="sxs-lookup"><span data-stu-id="6b5db-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="6b5db-129">Отчет в предварительной версии</span><span class="sxs-lookup"><span data-stu-id="6b5db-129">A report in Print Preview</span></span>
> - <span data-ttu-id="6b5db-130">Модуль</span><span class="sxs-lookup"><span data-stu-id="6b5db-130">A module</span></span>
> - <span data-ttu-id="6b5db-131">Представление сервера в представлении таблицы или предварительного просмотра печати</span><span class="sxs-lookup"><span data-stu-id="6b5db-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="6b5db-132">Страница доступа к данным в представлении страницы</span><span class="sxs-lookup"><span data-stu-id="6b5db-132">A data access page in Page view</span></span>
> - <span data-ttu-id="6b5db-133">Таблица в представлении "Таблица" или "Предварительный просмотр печати"</span><span class="sxs-lookup"><span data-stu-id="6b5db-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="6b5db-134">Запрос в представлении таблицы или предварительного просмотра печати</span><span class="sxs-lookup"><span data-stu-id="6b5db-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="6b5db-135">Хранимая процедура в представлении таблицы или предварительного просмотра печати</span><span class="sxs-lookup"><span data-stu-id="6b5db-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="6b5db-136">Действие **SaveObject,** независимо от того, выполнено ли оно в макросах, запускаемом в текущей базе данных или в базе данных библиотеки, всегда сохраняет указанный объект или активный объект в базе данных, в которой был создан объект.</span><span class="sxs-lookup"><span data-stu-id="6b5db-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="6b5db-137">Если активный объект сохраняется с новым именем, но имя такое же, как имя существующего объекта этого типа, диалоговое окно спросит, нужно ли перезаписать существующий объект.</span><span class="sxs-lookup"><span data-stu-id="6b5db-137">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object.</span></span> <span data-ttu-id="6b5db-138">Если для аргумента **Warnings On** действия **SetWarnings** установлено **"Нет",** диалоговое окно не отображается, а старый объект автоматически перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="6b5db-138">If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="6b5db-139">Чтобы запустить действие **SaveObject** в модуле Visual Basic для приложений (VBA), используйте метод **Save** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="6b5db-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

