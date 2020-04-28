---
title: Макрокоманда DeleteObject
TOCTitle: DeleteObject macro action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dae5718e7b4cb609cb50bd65ee6e2486f4ebaab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294031"
---
# <a name="deleteobject-macro-action"></a><span data-ttu-id="b723e-102">Макрокоманда DeleteObject</span><span class="sxs-lookup"><span data-stu-id="b723e-102">DeleteObject macro action</span></span>

<span data-ttu-id="b723e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b723e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b723e-104">Вы можете использовать действие **DeleteObject** , чтобы удалить указанный объект базы данных.</span><span class="sxs-lookup"><span data-stu-id="b723e-104">You can use the **DeleteObject** action to delete a specified database object.</span></span>

> [!NOTE]
> <span data-ttu-id="b723e-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="b723e-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="b723e-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="b723e-106">Setting</span></span>

<span data-ttu-id="b723e-107">Макрокоманда **DeleteObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="b723e-107">The **DeleteObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b723e-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="b723e-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b723e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b723e-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b723e-110"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="b723e-110"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="b723e-111">Тип удаляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="b723e-111">The type of object to delete.</span></span> <span data-ttu-id="b723e-112">Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>отчет</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong> в поле <strong>тип объекта</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="b723e-112">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="b723e-113">Чтобы удалить объект, выбранный в области навигации, оставьте этот аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="b723e-113">To delete the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b723e-114"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="b723e-114"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b723e-115">Имя удаляемого объекта.</span><span class="sxs-lookup"><span data-stu-id="b723e-115">The name of the object to delete.</span></span> <span data-ttu-id="b723e-116">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="b723e-116">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="b723e-117">Если оставить поле <strong>тип объекта</strong> пустым, также оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="b723e-117">If you leave the <strong>Object Type</strong> box blank, leave this box blank also.</span></span> <span data-ttu-id="b723e-118">При запуске макроса, содержащего действие <strong>DeleteObject</strong> в библиотечной базе данных, Microsoft Office Access 2007 сначала ищет объект с этим именем в библиотечной базе данных, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="b723e-118">If you run a macro containing the <strong>DeleteObject</strong> action in a library database, Microsoft Office Access 2007 first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

> [!WARNING]
> <span data-ttu-id="b723e-119">Если оставить поля **тип объекта** и **имя объекта** пустыми, Access удаляет объект, выбранный в области навигации, без отображения предупреждения при обнаружении действия **DeleteObject** .</span><span class="sxs-lookup"><span data-stu-id="b723e-119">If you leave the **Object Type** and **Object Name** boxes blank, Access deletes the object selected in the Navigation Pane without displaying a warning message when it encounters the **DeleteObject** action.</span></span>

## <a name="remarks"></a><span data-ttu-id="b723e-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b723e-120">Remarks</span></span>

<span data-ttu-id="b723e-121">Вы можете использовать действие **DeleteObject** для удаления временных объектов, созданных во время запуска макроса.</span><span class="sxs-lookup"><span data-stu-id="b723e-121">You can use the **DeleteObject** action to delete temporary objects you have created while running the macro.</span></span> <span data-ttu-id="b723e-122">Например, с помощью действия **OPENQUERY** можно выполнить запрос на создание таблицы, который создает временную таблицу.</span><span class="sxs-lookup"><span data-stu-id="b723e-122">For example, you could use the **OpenQuery** action to run a make-table query that creates a temporary table.</span></span> <span data-ttu-id="b723e-123">По завершении использования временной таблицы можно удалить ее с помощью действия **DeleteObject** .</span><span class="sxs-lookup"><span data-stu-id="b723e-123">When you are finished using the temporary table, you can use the **DeleteObject** action to delete it.</span></span>

<span data-ttu-id="b723e-124">Это действие эквивалентно выбору объекта в области навигации и нажатию клавиши DEL или щелчку правой кнопкой мыши объекта в области навигации и нажатию кнопки **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="b723e-124">This action has the same effect as selecting an object in the Navigation Pane and then pressing the DEL key, or right-clicking the object in the Navigation Pane and clicking **Delete**.</span></span>

<span data-ttu-id="b723e-125">Чтобы запустить действие **DeleteObject** в модуле Visual Basic для приложений, можно использовать метод **DeleteObject** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="b723e-125">To run the **DeleteObject** action in a Visual Basic for Applications module, you can use the **DeleteObject** method of the **DoCmd** object.</span></span>

