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
# <a name="renameobject-macro-action"></a><span data-ttu-id="27151-102">Макрокоманда RenameObject</span><span class="sxs-lookup"><span data-stu-id="27151-102">RenameObject macro action</span></span>

<span data-ttu-id="27151-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="27151-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="27151-104">Для переименования указанного объекта базы данных можно использовать действие **RenameObject.**</span><span class="sxs-lookup"><span data-stu-id="27151-104">You can use the **RenameObject** action to rename a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="27151-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="27151-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="27151-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="27151-106">Setting</span></span>

<span data-ttu-id="27151-107">Действие **RenameObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="27151-107">The **RenameObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27151-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="27151-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="27151-109">Описание</span><span class="sxs-lookup"><span data-stu-id="27151-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27151-110"><strong>Новое имя</strong></span><span class="sxs-lookup"><span data-stu-id="27151-110"><strong>New Name</strong></span></span></p></td>
<td><p><span data-ttu-id="27151-111">Новое имя объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="27151-111">A new name for the database object.</span></span> <span data-ttu-id="27151-112">Введите имя объекта в поле <strong>"Новое имя"</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="27151-112">Enter the object name in the <strong>New Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="27151-113">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="27151-113">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27151-114"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="27151-114"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="27151-115">Тип объекта, который необходимо переименовать.</span><span class="sxs-lookup"><span data-stu-id="27151-115">The type of object you want to rename.</span></span> <span data-ttu-id="27151-116">Щелкните <strong>таблицу,</strong> <strong>запрос,</strong> <strong>форма,</strong> <strong>отчет,</strong> <strong>макрос,</strong> <strong>модуль,</strong>страница доступа к <strong>данным,</strong>представление <strong>сервера,</strong> <strong>схема,</strong> <strong>сохраненная</strong>процедура или <strong>функция</strong>.</span><span class="sxs-lookup"><span data-stu-id="27151-116">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong>.</span></span> <span data-ttu-id="27151-117">Чтобы переименовать объект, выбранный в области навигации, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="27151-117">To rename the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27151-118"><strong>Старое имя</strong></span><span class="sxs-lookup"><span data-stu-id="27151-118"><strong>Old Name</strong></span></span></p></td>
<td><p><span data-ttu-id="27151-119">Имя объекта, который необходимо переименовать.</span><span class="sxs-lookup"><span data-stu-id="27151-119">The name of the object to be renamed.</span></span> <span data-ttu-id="27151-120">В <strong>поле Old Name</strong> показаны все объекты в базе данных типа, выбранного <strong>аргументом Object Type.</strong></span><span class="sxs-lookup"><span data-stu-id="27151-120">The <strong>Old Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="27151-121">Если оставить аргумент <strong>Object Type</strong> пустым, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="27151-121">If you leave the <strong>Object Type</strong> argument blank, leave this argument blank also.</span></span></p><p><span data-ttu-id="27151-122"><strong>ПРИМЕЧАНИЕ.</strong>При запуске макроса, содержащего действие переименования в базе данных библиотеки, Microsoft Access сначала ищет объект с этим именем в базе данных библиотеки, а затем в текущей базе данных. <STRONG></STRONG></span><span class="sxs-lookup"><span data-stu-id="27151-122"><strong>NOTE</strong>: If you run a macro containing the <STRONG>Rename</STRONG> action in a library database, Microsoft Access first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="27151-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="27151-123">Remarks</span></span>

<span data-ttu-id="27151-124">Новое имя объекта базы данных должно следовать стандартным соглашениям именования объектов Access.</span><span class="sxs-lookup"><span data-stu-id="27151-124">The new name of the database object must follow the standard naming conventions for Access objects.</span></span>

<span data-ttu-id="27151-125">Нельзя переименовать открытый объект.</span><span class="sxs-lookup"><span data-stu-id="27151-125">You can't rename an open object.</span></span>

<span data-ttu-id="27151-126">Если аргументы типа  **объектов** и старых имен будут пустыми, Access переименует объект, выбранный в области навигации.</span><span class="sxs-lookup"><span data-stu-id="27151-126">If you leave the **Object Type** and **Old Name** arguments blank, Access renames the object selected in the Navigation Pane.</span></span> <span data-ttu-id="27151-127">Чтобы выбрать объект в области навигации, можно использовать действие **SelectObject** с аргументом **В** области навигации, за набором **да.**</span><span class="sxs-lookup"><span data-stu-id="27151-127">To select an object in the Navigation Pane, you can use the **SelectObject** action with the **In Navigation Pane** argument set to **Yes**.</span></span>

<span data-ttu-id="27151-128">Вы также можете переименовать объект, щелкнув его правой кнопкой мыши в области навигации, нажав переименовать и введите новое имя.</span><span class="sxs-lookup"><span data-stu-id="27151-128">You can also rename an object by right-clicking it in the Navigation Pane, clicking **Rename**, and entering a new name.</span></span> <span data-ttu-id="27151-129">С помощью **действия RenameObject** не нужно сначала выбирать объект в области навигации, и для ввода нового имени макроса не нужно останавливать макрос.</span><span class="sxs-lookup"><span data-stu-id="27151-129">With the **RenameObject** action, you don't have to select the object first in the Navigation Pane, and you don't have to stop the macro to enter the new name.</span></span>

<span data-ttu-id="27151-130">Это действие отличается от действия **CopyObject,** которое создает копию объекта под новым именем.</span><span class="sxs-lookup"><span data-stu-id="27151-130">This action differs from the **CopyObject** action, which creates a copy of the object under a new name.</span></span>

<span data-ttu-id="27151-131">Чтобы выполнить действие **RenameObject** в Visual Basic для приложений (VBA), используйте метод **переименования** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="27151-131">To run the **RenameObject** action in a Visual Basic for Applications (VBA) module, use the **Rename** method of the **DoCmd** object.</span></span>

