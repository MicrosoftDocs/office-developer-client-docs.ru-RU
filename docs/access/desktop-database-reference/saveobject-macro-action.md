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
# <a name="saveobject-macro-action"></a><span data-ttu-id="77c2a-102">Макрокоманда SaveObject</span><span class="sxs-lookup"><span data-stu-id="77c2a-102">SaveObject macro action</span></span>

<span data-ttu-id="77c2a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="77c2a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77c2a-104">Вы можете использовать **действие SaveObject** для сохранения указанного объекта Access или активного объекта, если его нет.</span><span class="sxs-lookup"><span data-stu-id="77c2a-104">You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified.</span></span> <span data-ttu-id="77c2a-105">Кроме того, в некоторых случаях можно сохранить активный объект с новым именем (эта функция выполняется так же, как и команда **Save As** на панели инструментов **быстрого доступа).**</span><span class="sxs-lookup"><span data-stu-id="77c2a-105">You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).</span></span>

> [!NOTE]
> <span data-ttu-id="77c2a-106">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="77c2a-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="77c2a-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="77c2a-107">Setting</span></span>

<span data-ttu-id="77c2a-108">Действие **SaveObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="77c2a-108">The **SaveObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="77c2a-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="77c2a-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="77c2a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="77c2a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="77c2a-111"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="77c2a-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="77c2a-112">Тип объекта, который необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="77c2a-112">The type of object you want to save.</span></span> <span data-ttu-id="77c2a-113"><strong>Щелкните</strong> <strong>таблицу,</strong> <strong>запрос,</strong>форма, отчет, макрос, модуль, <strong></strong> <strong></strong>страница доступа <strong></strong> к данным, представление сервера, схема, сохраненная процедура или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="77c2a-113">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="77c2a-114">Чтобы выбрать активный объект, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="77c2a-114">To select the active object, leave this argument blank.</span></span> <span data-ttu-id="77c2a-115">Если в этом аргументе выбран тип объекта, необходимо выбрать имя существующего объекта в <strong>аргументе "Имя объекта".</strong></span><span class="sxs-lookup"><span data-stu-id="77c2a-115">If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="77c2a-116"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="77c2a-116"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="77c2a-117">Имя объекта, который необходимо сохранить.</span><span class="sxs-lookup"><span data-stu-id="77c2a-117">The name of the object to be saved.</span></span> <span data-ttu-id="77c2a-118">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="77c2a-118">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="77c2a-119">Если оставить аргумент <strong>Object Type</strong> пустым, этот аргумент можно оставить пустым, чтобы сохранить активный объект, или, в некоторых случаях, ввести новое имя в этом аргументе, чтобы сохранить активный объект с этим именем.</span><span class="sxs-lookup"><span data-stu-id="77c2a-119">If you leave the <strong>Object Type</strong> argument blank, you can leave this argument blank to save the active object, or, in some cases, enter a new name in this argument to save the active object with this name.</span></span> <span data-ttu-id="77c2a-120">Если вы вводите новое имя, имя должно следовать стандартным соглашениям именования для объектов Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="77c2a-120">If you enter a new name, the name must follow the standard naming conventions for Microsoft Access objects.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="77c2a-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="77c2a-121">Remarks</span></span>

<span data-ttu-id="77c2a-122">Действие **SaveObject** работает на всех объектах базы данных, которые пользователь может открыто открыть и сохранить.</span><span class="sxs-lookup"><span data-stu-id="77c2a-122">The **SaveObject** action works on all database objects that the user can explicitly open and save.</span></span> <span data-ttu-id="77c2a-123">Указанный объект должен быть открыт, чтобы действие **SaveObject** как-то сказывается на объекте.</span><span class="sxs-lookup"><span data-stu-id="77c2a-123">The specified object must be open for the **SaveObject** action to have any effect on the object.</span></span> <span data-ttu-id="77c2a-124">Это действие имеет тот же эффект, что и выбор объекта, а затем его сохранение, нажав **кнопку Сохранить** на панели инструментов **быстрого доступа**.</span><span class="sxs-lookup"><span data-stu-id="77c2a-124">This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**.</span></span> 

<span data-ttu-id="77c2a-125">Оставление аргумента **Object Type** пустым и ввод нового имени в аргументе **"Имя** объекта" имеет такой же эффект, как нажатие кнопки **Сохранить** как на панели инструментов быстрого доступа **и** ввод нового имени для активного объекта.</span><span class="sxs-lookup"><span data-stu-id="77c2a-125">Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object.</span></span> <span data-ttu-id="77c2a-126">Использование действия **SaveObject** позволяет указать объект для сохранения и выполнить команду **Сохранить как** из макроса.</span><span class="sxs-lookup"><span data-stu-id="77c2a-126">Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.</span></span>

> [!NOTE]
> <span data-ttu-id="77c2a-127">Вы не можете использовать действие **SaveObject,** чтобы сохранить любое из следующих действий с новым именем:</span><span class="sxs-lookup"><span data-stu-id="77c2a-127">You can't use the **SaveObject** action to save any of the following with a new name:</span></span>
> - <span data-ttu-id="77c2a-128">Форма в представлении формы или представлении таблицы данных</span><span class="sxs-lookup"><span data-stu-id="77c2a-128">A form in Form view or Datasheet view</span></span>
> - <span data-ttu-id="77c2a-129">Отчет в предварительной версии печати</span><span class="sxs-lookup"><span data-stu-id="77c2a-129">A report in Print Preview</span></span>
> - <span data-ttu-id="77c2a-130">Модуль</span><span class="sxs-lookup"><span data-stu-id="77c2a-130">A module</span></span>
> - <span data-ttu-id="77c2a-131">Представление сервера в представлении таблицы данных или предварительный просмотр печати</span><span class="sxs-lookup"><span data-stu-id="77c2a-131">A server view in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="77c2a-132">Страница доступа к данным в представлении Page</span><span class="sxs-lookup"><span data-stu-id="77c2a-132">A data access page in Page view</span></span>
> - <span data-ttu-id="77c2a-133">Таблица в представлении таблицы данных или предварительный просмотр печати</span><span class="sxs-lookup"><span data-stu-id="77c2a-133">A table in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="77c2a-134">Запрос в представлении таблицы данных или предварительном просмотре печати</span><span class="sxs-lookup"><span data-stu-id="77c2a-134">A query in Datasheet view or Print Preview</span></span>
> - <span data-ttu-id="77c2a-135">Сохраненная процедура в представлении таблицы данных или предварительном просмотре печати</span><span class="sxs-lookup"><span data-stu-id="77c2a-135">A stored procedure in Datasheet view or Print Preview</span></span>

<span data-ttu-id="77c2a-136">Действие **SaveObject,** выполнено ли оно в макросах текущей базы данных или в базе данных библиотеки, всегда сохраняет указанный объект или активный объект в базе данных, в которой был создан объект.</span><span class="sxs-lookup"><span data-stu-id="77c2a-136">The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.</span></span>

<span data-ttu-id="77c2a-137">Если вы сохраните активный объект с новым именем, но имя такое же, как имя существующего объекта этого типа, диалоговое окно задает вопрос, хотите ли вы перезаписать существующий объект.</span><span class="sxs-lookup"><span data-stu-id="77c2a-137">If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object.</span></span> <span data-ttu-id="77c2a-138">Если для аргумента  действия **SetWarnings** заочно установлено предупреждение, диалоговое окно не отображается, а старый объект автоматически перезаписывается.</span><span class="sxs-lookup"><span data-stu-id="77c2a-138">If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.</span></span>

<span data-ttu-id="77c2a-139">Чтобы выполнить **действие SaveObject** в Visual Basic для приложений (VBA), используйте метод **Сохранить** объект **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="77c2a-139">To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.</span></span>

