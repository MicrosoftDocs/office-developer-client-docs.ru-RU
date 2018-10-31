---
title: Действия макроса DeleteObject
TOCTitle: DeleteObject Macro Action
ms:assetid: a8deb2a7-4e73-8696-b8c1-3a3939d813f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821415(v=office.15)
ms:contentKeyID: 48546912
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm152112
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f9ac791ffd0f11c11358298570db833f8d561d11
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860940"
---
# <a name="deleteobject-macro-action"></a><span data-ttu-id="274af-102">Действия макроса DeleteObject</span><span class="sxs-lookup"><span data-stu-id="274af-102">DeleteObject Macro Action</span></span>


<span data-ttu-id="274af-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="274af-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="274af-104">Действие **DeleteObject** можно использовать для удаления объекта указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="274af-104">You can use the **DeleteObject** action to delete a specified database object.</span></span>


> [!NOTE]
> <span data-ttu-id="274af-p101">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="274af-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>

## <a name="setting"></a><span data-ttu-id="274af-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="274af-107">Setting</span></span>

<span data-ttu-id="274af-108">Действие **DeleteObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="274af-108">The **DeleteObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="274af-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="274af-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="274af-110">Описание</span><span class="sxs-lookup"><span data-stu-id="274af-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="274af-111"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="274af-111"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="274af-112">Тип объекта для удаления.</span><span class="sxs-lookup"><span data-stu-id="274af-112">The type of object to delete.</span></span> <span data-ttu-id="274af-113">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="274af-113">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="274af-114">Для удаления объекта, выделенного в области навигации, оставьте аргумент пустым.</span><span class="sxs-lookup"><span data-stu-id="274af-114">To delete the object selected in the Navigation Pane, leave this argument blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="274af-115"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="274af-115"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="274af-116">Имя объекта для удаления.</span><span class="sxs-lookup"><span data-stu-id="274af-116">The name of the object to delete.</span></span> <span data-ttu-id="274af-117">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="274af-117">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="274af-118">Если в поле <strong>Тип объекта</strong> оставить пустым, оставьте это поле пустым.</span><span class="sxs-lookup"><span data-stu-id="274af-118">If you leave the <strong>Object Type</strong> box blank, leave this box blank also.</span></span> <span data-ttu-id="274af-119">Если макрос, содержащий <strong>DeleteObject</strong> действие в базе данных библиотеки, Microsoft Office Access 2007 сначала выполняет поиск объекта с указанным именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="274af-119">If you run a macro containing the <strong>DeleteObject</strong> action in a library database, Microsoft Office Access 2007 first looks for the object with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>



> [!WARNING]
> <span data-ttu-id="274af-120">Если оставить поля **Тип объекта** и **Имя объекта** , Access удаляет объект, выбранного в области навигации без вывода предупреждающего сообщения при обнаружении **DeleteObject** действие.</span><span class="sxs-lookup"><span data-stu-id="274af-120">If you leave the **Object Type** and **Object Name** boxes blank, Access deletes the object selected in the Navigation Pane without displaying a warning message when it encounters the **DeleteObject** action.</span></span>



## <a name="remarks"></a><span data-ttu-id="274af-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="274af-121">Remarks</span></span>

<span data-ttu-id="274af-122">Чтобы удалить временные объекты, созданные во время выполнения макроса можно использовать действие **DeleteObject** .</span><span class="sxs-lookup"><span data-stu-id="274af-122">You can use the **DeleteObject** action to delete temporary objects you have created while running the macro.</span></span> <span data-ttu-id="274af-123">Например можно использовать **ОткрытьЗапрос** для выполнения запроса создание таблицы, который создает временные таблицы.</span><span class="sxs-lookup"><span data-stu-id="274af-123">For example, you could use the **OpenQuery** action to run a make-table query that creates a temporary table.</span></span> <span data-ttu-id="274af-124">По окончании с помощью временной таблицы, можно использовать действие **DeleteObject** удалить ее.</span><span class="sxs-lookup"><span data-stu-id="274af-124">When you are finished using the temporary table, you can use the **DeleteObject** action to delete it.</span></span>

<span data-ttu-id="274af-125">Это действие имеет тот же эффект, что при выборе объекта в области навигации и затем нажав клавишу DEL или щелкнув правой кнопкой мыши объект в области навигации и выбрав команду **Удалить**.</span><span class="sxs-lookup"><span data-stu-id="274af-125">This action has the same effect as selecting an object in the Navigation Pane and then pressing the DEL key, or right-clicking the object in the Navigation Pane and clicking **Delete**.</span></span>

<span data-ttu-id="274af-126">Чтобы выполнить действие **DeleteObject** в Visual Basic для приложений модуля, можно использовать метод **DeleteObject** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="274af-126">To run the **DeleteObject** action in a Visual Basic for Applications module, you can use the **DeleteObject** method of the **DoCmd** object.</span></span>

