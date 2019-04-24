---
title: Макрокоманда SelectObject
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308731"
---
# <a name="selectobject-macro-action"></a><span data-ttu-id="2b244-102">Макрокоманда SelectObject</span><span class="sxs-lookup"><span data-stu-id="2b244-102">SelectObject macro action</span></span>

<span data-ttu-id="2b244-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2b244-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2b244-104">Макрокоманду "ВыделитьОбъект" ( **ВыделитьОбъект** ) можно использовать для выбора указанного объекта базы данных.</span><span class="sxs-lookup"><span data-stu-id="2b244-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="2b244-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="2b244-105">Setting</span></span>

<span data-ttu-id="2b244-106">Макрокоманда **ВыделитьОбъект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="2b244-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2b244-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="2b244-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="2b244-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2b244-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b244-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="2b244-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="2b244-110">Тип объекта базы данных, который необходимо выбрать.</span><span class="sxs-lookup"><span data-stu-id="2b244-110">The type of database object to select.</span></span> <span data-ttu-id="2b244-111">Щелкните <strong>Таблица</strong>, <strong>запрос</strong>, <strong>форма</strong>, <strong>отчет</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>Страница доступа к данным</strong>, <strong>представление сервера</strong>, <strong>схема</strong>, <strong>хранимая процедура</strong>или <strong>функция</strong> в <strong>типе объекта. </strong>в разделе <strong>аргументы макрокоманды</strong> в панели построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="2b244-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="2b244-112">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="2b244-112">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b244-113"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="2b244-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="2b244-114">Имя выбираемого объекта.</span><span class="sxs-lookup"><span data-stu-id="2b244-114">The name of the object to select.</span></span> <span data-ttu-id="2b244-115">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b244-115">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="2b244-116">Это обязательный аргумент, если для аргумента в области навигации не задано значение <strong>"Да"</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b244-116">This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p><p><span data-ttu-id="2b244-117"><strong>Note</strong>: имена объектов для <STRONG>представления сервера</STRONG>, <STRONG>схемы</STRONG>или хранимых <STRONG>процедур</STRONG> не отображаются в поле <STRONG>имя объекта</STRONG> проекта Access (ADP).</span><span class="sxs-lookup"><span data-stu-id="2b244-117"><strong>NOTE</strong>: The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b244-118"><strong>В области навигации</strong></span><span class="sxs-lookup"><span data-stu-id="2b244-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="2b244-119">Определяет, будет ли Microsoft Access выбирать объект в области навигации.</span><span class="sxs-lookup"><span data-stu-id="2b244-119">Specifies whether Microsoft Access selects the object in the Navigation Pane.</span></span> <span data-ttu-id="2b244-120">Нажмите кнопку <strong>Да</strong> (чтобы выбрать объект в области навигации) или <strong>нет</strong> (не выделять объект в области навигации).</span><span class="sxs-lookup"><span data-stu-id="2b244-120">Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane).</span></span> <span data-ttu-id="2b244-121">По умолчанию используется значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="2b244-121">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2b244-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="2b244-122">Remarks</span></span>

<span data-ttu-id="2b244-123">Макрокоманда **ВыделитьОбъект** работает с любым объектом Access, который может получить фокус.</span><span class="sxs-lookup"><span data-stu-id="2b244-123">The **SelectObject** action works with any Access object that can receive the focus.</span></span> <span data-ttu-id="2b244-124">Это действие приводит к указанному объекту фокуса и отображает объект, если он скрыт.</span><span class="sxs-lookup"><span data-stu-id="2b244-124">This action gives the specified object the focus and shows the object if it's hidden.</span></span> <span data-ttu-id="2b244-125">Если объект является формой, то Макрокоманда **ВыделитьОбъект** устанавливает для свойства **Visible** формы значение **Да** и возвращает форму в режим, заданный свойствами формы (например, в виде модальной или всплывающей формы).</span><span class="sxs-lookup"><span data-stu-id="2b244-125">If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="2b244-126">Если объект не открыт в одном из других окон Access, можно выбрать его в области навигации, указав для аргумента **в области навигации** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="2b244-126">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**.</span></span> <span data-ttu-id="2b244-127">Если для аргумента **в области навигации** задано значение **нет**, при попытке выбрать объект, который не открыт, появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="2b244-127">If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="2b244-128">Это действие часто можно использовать для выбора объекта, для которого требуется выполнить дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="2b244-128">Often, you might use this action to select an object on which you want to perform additional actions.</span></span> <span data-ttu-id="2b244-129">Например, если доступ настроен на использование перекрывающихся окон вместо документов с вкладками, может потребоваться восстановить объект, свернутый (с помощью действия **ресторевиндов** ), или развернуть окно, содержащее объект, с которым вы хотите работать. (с помощью действия **максимизевиндов** ).</span><span class="sxs-lookup"><span data-stu-id="2b244-129">For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="2b244-130">Если выбрана форма, вы можете использовать действия **КЭлементуУправления**, **GoToRecord**и **GoToPage** , чтобы перейти к определенным областям формы.</span><span class="sxs-lookup"><span data-stu-id="2b244-130">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form.</span></span> <span data-ttu-id="2b244-131">Действие **GoToRecord** также работает для таблиц с таблицами.</span><span class="sxs-lookup"><span data-stu-id="2b244-131">The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="2b244-132">Чтобы выполнить макрокоманду **ВыделитьОбъект** в модуле Visual Basic для приложений (VBA), используйте метод **SelectObject** объекта DoCmd. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2b244-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

