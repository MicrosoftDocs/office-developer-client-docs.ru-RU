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
ms.openlocfilehash: 77fc87ac989d34f5a4e774555c54955cf0bd805e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931353"
---
# <a name="saveobject-macro-action"></a><span data-ttu-id="5cbf7-102">Макрокоманда SaveObject</span><span class="sxs-lookup"><span data-stu-id="5cbf7-102">SaveObject macro action</span></span>


<span data-ttu-id="5cbf7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5cbf7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5cbf7-104">Действие **SaveObject** можно использовать для сохранения указанный объект доступа или активного объекта, если он не задан.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-104">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified.</span></span> <span data-ttu-id="5cbf7-105">Можно также сохранить активного объекта под новым именем, в некоторых случаях (это работает так же, как команды **Сохранить как** в панели **Быстрого доступа**).</span><span class="sxs-lookup"><span data-stu-id="5cbf7-105">You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>


> [!NOTE]
> <P><span data-ttu-id="5cbf7-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="5cbf7-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="5cbf7-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5cbf7-108">Setting</span></span>

<span data-ttu-id="5cbf7-109">Действие **SaveObject** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-109">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5cbf7-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="5cbf7-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5cbf7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="5cbf7-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cbf7-112"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="5cbf7-112"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbf7-113">Тип объекта, который следует сохранить.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-113">The type of object you want to save.</span></span> <span data-ttu-id="5cbf7-114">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-114">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="5cbf7-115">Чтобы выбрать активный объект, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-115">To select the active object, leave this argument blank.</span></span> <span data-ttu-id="5cbf7-116">Если выбрать тип объекта в этот аргумент, необходимо выбрать имя существующего объекта в качестве аргумента <strong>Имя объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="5cbf7-116">If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cbf7-117"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="5cbf7-117"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5cbf7-118">Имя объекта будет сохранен.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-118">The name of the object to be saved.</span></span> <span data-ttu-id="5cbf7-119">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-119">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="5cbf7-120">Если <strong>Тип объекта</strong> аргумента оставлено пустым, можно оставить данный аргумент пустым, чтобы сохранить активный объект или, в некоторых случаях, введите новое имя в для сохранения активного объекта с этим именем.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-120">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="5cbf7-121">Если ввести новое имя, имя должно соответствовать стандартным соглашениям об именах объектов Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-121">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5cbf7-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="5cbf7-122">Remarks</span></span>

<span data-ttu-id="5cbf7-123">Действие **SaveObject** работает на все объекты базы данных, которые пользователь может явно открывать и сохранять.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-123">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="5cbf7-124">Указанный объект должен быть открыт для выполнения действия **SaveObject** оказывает никакого влияния на объекте.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-124">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="5cbf7-125">Это действие имеет тот же эффект, как при выборе объекта и сохранения его, нажав кнопку **Сохранить** на панели **Быстрого доступа**.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-125">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> <span data-ttu-id="5cbf7-126">Оставить пустым аргумент **Тип объекта** и введите новое имя в качестве аргумента **Имя объекта** имеет тот же эффект, что и нажмите кнопку **Сохранить как** на панели **Быстрого доступа**и введите новое имя для активного объекта.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-126">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="5cbf7-127">Действие **SaveObject** позволяет указать объект для сохранения и выполнения команды **Сохранить как** из макроса.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-127">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>


> [!NOTE]
> <P><span data-ttu-id="5cbf7-128">Чтобы сохранить любую из следующих действий с новым именем нельзя использовать действие <STRONG>SaveObject</STRONG> :</span><span class="sxs-lookup"><span data-stu-id="5cbf7-128">You can't use the <STRONG>SaveObject</STRONG> action to save any of the following with a new name:</span></span></P>



  - <span data-ttu-id="5cbf7-129">Форма в режиме формы или таблицы.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-129">A form in Form view or Datasheet view.</span></span>

  - <span data-ttu-id="5cbf7-130">Отчет в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-130">A report in Print Preview.</span></span>

  - <span data-ttu-id="5cbf7-131">Модуль.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-131">A module.</span></span>

  - <span data-ttu-id="5cbf7-132">Представление в режиме или режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-132">A server view in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="5cbf7-133">Страницы в представлении Страница доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-133">A data access page in Page view.</span></span>

  - <span data-ttu-id="5cbf7-134">Таблица в режиме таблицы или в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-134">A table in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="5cbf7-135">Запрос в режиме таблицы или в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-135">A query in Datasheet view or Print Preview.</span></span>

  - <span data-ttu-id="5cbf7-136">Хранимую процедуру в режиме таблицы или в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-136">A stored procedure in Datasheet view or Print Preview.</span></span>

<span data-ttu-id="5cbf7-137">**SaveObject** действия, выполняемые в макросе, в текущей базе данных или в базе данных библиотеки, всегда сохраняет ли указанный объект или активный объект в базе данных, в котором был создан объект.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-137">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="5cbf7-138">Сохранение активного объекта под новым именем, но имя совпадает с именем существующего объекта этого типа, диалоговое окно с запросом на перезапись существующего объекта.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-138">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object.</span></span> <span data-ttu-id="5cbf7-139">Если выбрать **В** аргументе действие **УстановитьСообщения** **Нет**не отображается диалоговое окно и старый объект автоматически перезаписан.</span><span class="sxs-lookup"><span data-stu-id="5cbf7-139">If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="5cbf7-140">Чтобы выполнить действие **SaveObject** в Visual Basic для приложений (VBA) модуль, используйте метод **сохранения** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="5cbf7-140">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

