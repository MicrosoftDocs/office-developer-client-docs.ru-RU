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
ms.openlocfilehash: 253067d61a496073692ea4e462b9b0a67f0e26cd
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026297"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="cbc72-102">Макрокоманда SaveObject</span><span class="sxs-lookup"><span data-stu-id="cbc72-102">SaveObject macro action</span></span>

<span data-ttu-id="cbc72-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cbc72-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cbc72-104">Действие **SaveObject** можно использовать для сохранения указанный объект доступа или активного объекта, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="cbc72-104">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified.</span></span> <span data-ttu-id="cbc72-105">Можно также сохранить активного объекта под новым именем, в некоторых случаях (это работает так же, как команды **Сохранить как** в панели **Быстрого доступа**).</span><span class="sxs-lookup"><span data-stu-id="cbc72-105">You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="cbc72-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="cbc72-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="cbc72-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="cbc72-107">Setting</span></span>

<span data-ttu-id="cbc72-108">Действие **SaveObject** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="cbc72-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cbc72-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="cbc72-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cbc72-110">Описание</span><span class="sxs-lookup"><span data-stu-id="cbc72-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cbc72-111"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="cbc72-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="cbc72-112">Тип объекта, который следует сохранить.</span><span class="sxs-lookup"><span data-stu-id="cbc72-112">The type of object you want to save.</span></span> <span data-ttu-id="cbc72-113">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="cbc72-113">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="cbc72-114">Чтобы выбрать активный объект, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="cbc72-114">To select the active object, leave this argument blank.</span></span> <span data-ttu-id="cbc72-115">Если выбрать тип объекта в этот аргумент, необходимо выбрать имя существующего объекта в качестве аргумента <strong>Имя объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="cbc72-115">If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cbc72-116"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="cbc72-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cbc72-117">Имя объекта будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="cbc72-117">The name of the object to be saved.</span></span> <span data-ttu-id="cbc72-118">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="cbc72-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="cbc72-119">Если <strong>Тип объекта</strong> аргумента оставлено пустым, можно оставить данный аргумент пустым, чтобы сохранить активный объект или, в некоторых случаях, введите новое имя в для сохранения активного объекта с этим именем.</span><span class="sxs-lookup"><span data-stu-id="cbc72-119">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="cbc72-120">Если ввести новое имя, имя должно соответствовать стандартным соглашениям об именах объектов Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="cbc72-120">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cbc72-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="cbc72-121">Remarks</span></span>

<span data-ttu-id="cbc72-122">Действие **SaveObject** работает на все объекты базы данных, которые пользователь может явно открывать и сохранять.</span><span class="sxs-lookup"><span data-stu-id="cbc72-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="cbc72-123">Указанный объект должен быть открыт для выполнения действия **SaveObject** оказывает никакого влияния на объекте.</span><span class="sxs-lookup"><span data-stu-id="cbc72-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="cbc72-124">Это действие имеет тот же эффект, как при выборе объекта и сохранения его, нажав кнопку **Сохранить** на панели **Быстрого доступа**.</span><span class="sxs-lookup"><span data-stu-id="cbc72-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> 

<span data-ttu-id="cbc72-125">Оставить пустым аргумент **Тип объекта** и введите новое имя в качестве аргумента **Имя объекта** имеет тот же эффект, что и нажмите кнопку **Сохранить как** на панели **Быстрого доступа**и введите новое имя для активного объекта.</span><span class="sxs-lookup"><span data-stu-id="cbc72-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="cbc72-126">Действие **SaveObject** позволяет указать объект для сохранения и выполнения команды **Сохранить как** из макроса.</span><span class="sxs-lookup"><span data-stu-id="cbc72-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="cbc72-127">Чтобы сохранить любую из следующих действий с новым именем нельзя использовать действие **SaveObject** :</span><span class="sxs-lookup"><span data-stu-id="cbc72-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="cbc72-128">Формы в режиме формы или таблицы</span><span class="sxs-lookup"><span data-stu-id="cbc72-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="cbc72-129">Отчет в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="cbc72-129">A report in Print Preview</span></span>
> - <span data-ttu-id="cbc72-130">Модуль</span><span class="sxs-lookup"><span data-stu-id="cbc72-130">A module</span></span>
> - <span data-ttu-id="cbc72-131">Представление в режиме таблицы или в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="cbc72-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="cbc72-132">Страницы в представлении Страница доступа к данным</span><span class="sxs-lookup"><span data-stu-id="cbc72-132">A data access page in Page view</span></span>
> - <span data-ttu-id="cbc72-133">Таблица в режиме таблицы или в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="cbc72-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="cbc72-134">Запрос в режиме таблицы или в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="cbc72-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="cbc72-135">Хранимую процедуру в режиме таблицы или в режиме предварительного просмотра</span><span class="sxs-lookup"><span data-stu-id="cbc72-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="cbc72-136">**SaveObject** действия, выполняемые в макросе, в текущей базе данных или в базе данных библиотеки, всегда сохраняет ли указанный объект или активный объект в базе данных, в котором был создан объект.</span><span class="sxs-lookup"><span data-stu-id="cbc72-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="cbc72-137">Сохранение активного объекта под новым именем, но имя совпадает с именем существующего объекта этого типа, диалоговое окно с запросом на перезапись существующего объекта.</span><span class="sxs-lookup"><span data-stu-id="cbc72-137">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object.</span></span> <span data-ttu-id="cbc72-138">Если выбрать **В** аргументе действие **УстановитьСообщения** **Нет**не отображается диалоговое окно и старый объект автоматически перезаписан.</span><span class="sxs-lookup"><span data-stu-id="cbc72-138">If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="cbc72-139">Чтобы выполнить действие **SaveObject** в Visual Basic для приложений (VBA) модуль, используйте метод **сохранения** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="cbc72-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

