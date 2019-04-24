---
title: Макрокоманда RenameObject
TOCTitle: RenameObject macro action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ce16b86ea06e041d490d0c68917daf18bd80dbb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306722"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="5f91c-102">Макрокоманда RenameObject</span><span class="sxs-lookup"><span data-stu-id="5f91c-102">RenameObject macro action</span></span>

<span data-ttu-id="5f91c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f91c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f91c-104">Вы можете использовать действие **ренамеобжект** для переименования указанного объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f91c-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="5f91c-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="5f91c-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="5f91c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5f91c-106">Setting</span></span>

<span data-ttu-id="5f91c-107">Макрокоманда **ренамеобжект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5f91c-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f91c-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="5f91c-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="5f91c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5f91c-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f91c-110"><strong>Новое имя</strong></span><span class="sxs-lookup"><span data-stu-id="5f91c-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5f91c-111">Новое имя объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="5f91c-111">A new name for the database object.</span></span> <span data-ttu-id="5f91c-112">Введите имя объекта в поле <strong>новое имя</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="5f91c-112">Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="5f91c-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="5f91c-113">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f91c-114"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="5f91c-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="5f91c-115">Тип объекта, который требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="5f91c-115">The type of object you want to rename.</span></span> <span data-ttu-id="5f91c-116">Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>отчет</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong>.</span><span class="sxs-lookup"><span data-stu-id="5f91c-116">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>.</span></span> <span data-ttu-id="5f91c-117">Чтобы переименовать объект, выбранный в области навигации, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="5f91c-117">To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f91c-118"><strong>Старое имя</strong></span><span class="sxs-lookup"><span data-stu-id="5f91c-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="5f91c-119">Имя объекта, который требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="5f91c-119">The name of the object to be renamed.</span></span> <span data-ttu-id="5f91c-120">В поле <strong>старОе имя</strong> отображаются все объекты базы данных с типом, выбранным аргументом <strong>тип объекта</strong> .</span><span class="sxs-lookup"><span data-stu-id="5f91c-120">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="5f91c-121">Если оставить аргумент " <strong>тип объекта</strong> " пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="5f91c-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="5f91c-122"><strong>Note</strong>: при запуске макроса, содержащего действие <STRONG></STRONG> переименования, в библиотечной базе данных Microsoft Access сначала ищет объект с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="5f91c-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5f91c-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="5f91c-123">Remarks</span></span>

<span data-ttu-id="5f91c-124">Новое имя объекта базы данных должно соответствовать стандартным соглашениям об именовании для объектов Access.</span><span class="sxs-lookup"><span data-stu-id="5f91c-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="5f91c-125">Невозможно переименовать открытый объект.</span><span class="sxs-lookup"><span data-stu-id="5f91c-125">You can't rename an open object.</span></span>

<span data-ttu-id="5f91c-126">Если оставить аргументы **тип объекта** и **старый имя** пустыми, Access переименует объект, выбранный в области навигации.</span><span class="sxs-lookup"><span data-stu-id="5f91c-126">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane.</span></span> <span data-ttu-id="5f91c-127">Чтобы выбрать объект в области навигации, можно использовать макрокоманду **"ВыделитьОбъект"**( **ВыделитьОбъект** ) с параметром **в разделе в области навигации** со значением Да.</span><span class="sxs-lookup"><span data-stu-id="5f91c-127">To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="5f91c-128">Вы также можете переименовать объект, щелкнув его правой кнопкой мыши в области навигации, выбрав команду **Переименовать**и введя новое имя.</span><span class="sxs-lookup"><span data-stu-id="5f91c-128">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name.</span></span> <span data-ttu-id="5f91c-129">С помощью действия **ренамеобжект** не нужно сначала выбирать объект в области навигации, а также останавливать макрос для ввода нового имени.</span><span class="sxs-lookup"><span data-stu-id="5f91c-129">With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="5f91c-130">Это действие отличается от команды **КопироватьОбъект** , которая создает копию объекта под новым именем.</span><span class="sxs-lookup"><span data-stu-id="5f91c-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="5f91c-131">Чтобы запустить действие **ренамеобжект** в модуле Visual Basic для приложений (VBA), используйте метод Rename \*\*\*\* объекта DoCmd. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="5f91c-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

