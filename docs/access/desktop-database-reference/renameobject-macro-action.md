---
title: RenameObject Macro Action
TOCTitle: RenameObject Macro Action
ms:assetid: fee04eb0-23c0-5d57-b903-e1ae54f2d25e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837293(v=office.15)
ms:contentKeyID: 48548948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm165893
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6522e85aa0407800ea0aade039a65c79a25c1419
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480825"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="91b40-102">RenameObject Macro Action</span><span class="sxs-lookup"><span data-stu-id="91b40-102">RenameObject Macro Action</span></span>


<span data-ttu-id="91b40-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="91b40-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="91b40-104">Действие **RenameObject** можно использовать для переименования объекта указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="91b40-104">You can use the **RenameObject** action to rename a specified database object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="91b40-p101">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="91b40-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="91b40-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="91b40-107">Setting</span></span>

<span data-ttu-id="91b40-108">Действие **RenameObject** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="91b40-108">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91b40-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="91b40-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="91b40-110">Описание</span><span class="sxs-lookup"><span data-stu-id="91b40-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91b40-111"><strong>Новое имя</strong></span><span class="sxs-lookup"><span data-stu-id="91b40-111"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="91b40-112">Новое имя для объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="91b40-112">A new name for the database object.</span></span> <span data-ttu-id="91b40-113">Введите имя объекта в поле <strong>Новое имя</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="91b40-113">Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="91b40-114">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="91b40-114">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91b40-115"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="91b40-115"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="91b40-116">Тип объекта, который требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="91b40-116">The type of object you want to rename.</span></span> <span data-ttu-id="91b40-117">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong>.</span><span class="sxs-lookup"><span data-stu-id="91b40-117">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>.</span></span> <span data-ttu-id="91b40-118">Чтобы переименовать объект, выделенный в области навигации, оставьте данный аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="91b40-118">To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91b40-119"><strong>Старое имя</strong></span><span class="sxs-lookup"><span data-stu-id="91b40-119"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="91b40-120">Имя объекта, чтобы переименовать.</span><span class="sxs-lookup"><span data-stu-id="91b40-120">The name of the object to be renamed.</span></span> <span data-ttu-id="91b40-121">В поле <strong>Имя старого</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="91b40-121">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="91b40-122">Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="91b40-122">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="91b40-123">Если макрос, содержащий действие <STRONG>Переименовать</STRONG> базы данных библиотеки, Microsoft Access сначала выполняет поиск объекта с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="91b40-123">If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="91b40-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="91b40-124">Remarks</span></span>

<span data-ttu-id="91b40-125">Новое имя объекта базы данных необходимо выполнить стандартные соглашения о наименовании для доступа к объектам.</span><span class="sxs-lookup"><span data-stu-id="91b40-125">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="91b40-126">Невозможно переименование open объекта.</span><span class="sxs-lookup"><span data-stu-id="91b40-126">You can't rename an open object.</span></span>

<span data-ttu-id="91b40-127">Если оставить аргументы **Старое имя** и **Тип объекта** , Access переименовывает объекта, выбранного в области навигации.</span><span class="sxs-lookup"><span data-stu-id="91b40-127">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane.</span></span> <span data-ttu-id="91b40-128">Для выбора объекта в области навигации, можно использовать **ВыделитьОбъект** с аргументом **В области переходов** , значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="91b40-128">To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="91b40-129">Вы также можете переименовать объект, щелкнув правой кнопкой мыши в области навигации, нажав кнопку **Переименовать**и ввести новое имя.</span><span class="sxs-lookup"><span data-stu-id="91b40-129">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name.</span></span> <span data-ttu-id="91b40-130">С действием **RenameObject** не требуется сначала выберите объект в области навигации, и у вас нет для остановки ввести новое имя.</span><span class="sxs-lookup"><span data-stu-id="91b40-130">With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="91b40-131">Это действие отличается от **КопироватьОбъект, которая создает копию объекта под новым именем** .</span><span class="sxs-lookup"><span data-stu-id="91b40-131">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="91b40-132">Чтобы выполнить действие **RenameObject** в Visual Basic для приложений (VBA) модуль, используйте метод **Переименование** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="91b40-132">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

