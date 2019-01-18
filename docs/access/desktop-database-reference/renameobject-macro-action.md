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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698388"
---
# <a name="renameobject-macro-action"></a><span data-ttu-id="1aa45-102">Макрокоманда RenameObject</span><span class="sxs-lookup"><span data-stu-id="1aa45-102">RenameObject macro action</span></span>

<span data-ttu-id="1aa45-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1aa45-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1aa45-104">Действие **RenameObject** можно использовать для переименования объекта указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1aa45-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="1aa45-105">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="1aa45-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="1aa45-106">Setting</span><span class="sxs-lookup"><span data-stu-id="1aa45-106">Setting</span></span>

<span data-ttu-id="1aa45-107">Действие **RenameObject** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="1aa45-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1aa45-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1aa45-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1aa45-109">Описание</span><span class="sxs-lookup"><span data-stu-id="1aa45-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1aa45-110"><strong>Новое имя</strong></span><span class="sxs-lookup"><span data-stu-id="1aa45-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1aa45-111">Новое имя для объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="1aa45-111">A new name for the database object.</span></span> <span data-ttu-id="1aa45-112">Введите имя объекта в поле <strong>Новое имя</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="1aa45-112">Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="1aa45-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="1aa45-113">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1aa45-114"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="1aa45-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="1aa45-115">Тип объекта, который требуется переименовать.</span><span class="sxs-lookup"><span data-stu-id="1aa45-115">The type of object you want to rename.</span></span> <span data-ttu-id="1aa45-116">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong>.</span><span class="sxs-lookup"><span data-stu-id="1aa45-116">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>.</span></span> <span data-ttu-id="1aa45-117">Чтобы переименовать объект, выделенный в области навигации, оставьте данный аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="1aa45-117">To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1aa45-118"><strong>Старое имя</strong></span><span class="sxs-lookup"><span data-stu-id="1aa45-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1aa45-119">Имя объекта, чтобы переименовать.</span><span class="sxs-lookup"><span data-stu-id="1aa45-119">The name of the object to be renamed.</span></span> <span data-ttu-id="1aa45-120">В поле <strong>Имя старого</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="1aa45-120">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="1aa45-121">Если <strong>Тип объекта</strong> аргумента оставлено пустым, оставьте аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="1aa45-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="1aa45-122"><strong>Примечание</strong>: Если макрос, содержащий действие <STRONG>Переименовать</STRONG> базы данных библиотеки, Microsoft Access сначала выполняет поиск объекта с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="1aa45-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1aa45-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="1aa45-123">Remarks</span></span>

<span data-ttu-id="1aa45-124">Новое имя объекта базы данных необходимо выполнить стандартные соглашения о наименовании для доступа к объектам.</span><span class="sxs-lookup"><span data-stu-id="1aa45-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="1aa45-125">Невозможно переименование open объекта.</span><span class="sxs-lookup"><span data-stu-id="1aa45-125">You can't rename an open object.</span></span>

<span data-ttu-id="1aa45-126">Если оставить аргументы **Старое имя** и **Тип объекта** , Access переименовывает объекта, выбранного в области навигации.</span><span class="sxs-lookup"><span data-stu-id="1aa45-126">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane.</span></span> <span data-ttu-id="1aa45-127">Для выбора объекта в области навигации, можно использовать **ВыделитьОбъект** с аргументом **В области переходов** , значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1aa45-127">To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="1aa45-128">Вы также можете переименовать объект, щелкнув правой кнопкой мыши в области навигации, нажав кнопку **Переименовать**и ввести новое имя.</span><span class="sxs-lookup"><span data-stu-id="1aa45-128">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name.</span></span> <span data-ttu-id="1aa45-129">С действием **RenameObject** не требуется сначала выберите объект в области навигации, и у вас нет для остановки ввести новое имя.</span><span class="sxs-lookup"><span data-stu-id="1aa45-129">With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="1aa45-130">Это действие отличается от **КопироватьОбъект, которая создает копию объекта под новым именем** .</span><span class="sxs-lookup"><span data-stu-id="1aa45-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="1aa45-131">Чтобы выполнить действие **RenameObject** в Visual Basic для приложений (VBA) модуль, используйте метод **Переименование** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="1aa45-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

