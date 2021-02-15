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
# <a name="selectobject-macro-action"></a><span data-ttu-id="53ddc-102">Макрокоманда SelectObject</span><span class="sxs-lookup"><span data-stu-id="53ddc-102">SelectObject macro action</span></span>

<span data-ttu-id="53ddc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="53ddc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53ddc-104">С помощью действия **SelectObject можно** выбрать указанный объект базы данных.</span><span class="sxs-lookup"><span data-stu-id="53ddc-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="53ddc-105">Setting</span><span class="sxs-lookup"><span data-stu-id="53ddc-105">Setting</span></span>

<span data-ttu-id="53ddc-106">Действие **SelectObject** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="53ddc-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53ddc-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="53ddc-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="53ddc-108">Описание</span><span class="sxs-lookup"><span data-stu-id="53ddc-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53ddc-109"><strong>Object Type</strong></span><span class="sxs-lookup"><span data-stu-id="53ddc-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="53ddc-110">Тип объекта базы данных, который необходимо выбрать.</span><span class="sxs-lookup"><span data-stu-id="53ddc-110">The type of database object to select.</span></span> <span data-ttu-id="53ddc-111">Щелкните <strong>"Таблица",</strong>"Запрос", "Форма", "Отчет", "Макрос", <strong></strong> "Модуль", <strong></strong> "Страница доступа к данным", "Представление сервера", "Схема", "Хранимая процедура" или "Функция" в поле "Тип объекта" в разделе "Аргументы действий" области построитель макроса. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong></span><span class="sxs-lookup"><span data-stu-id="53ddc-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="53ddc-112">Это обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="53ddc-112">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53ddc-113"><strong>Object Name</strong></span><span class="sxs-lookup"><span data-stu-id="53ddc-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="53ddc-114">Имя выбираемого объекта.</span><span class="sxs-lookup"><span data-stu-id="53ddc-114">The name of the object to select.</span></span> <span data-ttu-id="53ddc-115">Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>.</span><span class="sxs-lookup"><span data-stu-id="53ddc-115">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="53ddc-116">Это необходимый аргумент, если только для аргумента "В области навигации" не установлено <strong>"Да".</strong></span><span class="sxs-lookup"><span data-stu-id="53ddc-116">This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p><p><span data-ttu-id="53ddc-117"><strong>ПРИМЕЧАНИЕ.</strong>Имена объектов <STRONG>представления</STRONG> <STRONG>сервера,</STRONG>схемы или хранимых <STRONG></STRONG> процедур не отображаются в поле "Имя объекта" проекта Access (ADP). <STRONG></STRONG></span><span class="sxs-lookup"><span data-stu-id="53ddc-117"><strong>NOTE</strong>: The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53ddc-118"><strong>В области навигации</strong></span><span class="sxs-lookup"><span data-stu-id="53ddc-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="53ddc-119">Указывает, выбирает ли Microsoft Access объект в области навигации.</span><span class="sxs-lookup"><span data-stu-id="53ddc-119">Specifies whether Microsoft Access selects the object in the Navigation Pane.</span></span> <span data-ttu-id="53ddc-120">Нажмите <strong>кнопку</strong> "Да" (чтобы выбрать объект в области навигации) или <strong>"Нет"</strong> (чтобы не выбирать объект в области навигации).</span><span class="sxs-lookup"><span data-stu-id="53ddc-120">Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane).</span></span> <span data-ttu-id="53ddc-121">По умолчанию используется значение <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="53ddc-121">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="53ddc-122">Заметки</span><span class="sxs-lookup"><span data-stu-id="53ddc-122">Remarks</span></span>

<span data-ttu-id="53ddc-123">Действие **SelectObject** работает с любым объектом Access, который может получить фокус.</span><span class="sxs-lookup"><span data-stu-id="53ddc-123">The **SelectObject** action works with any Access object that can receive the focus.</span></span> <span data-ttu-id="53ddc-124">Это действие предоставляет указанному объекту фокус и показывает объект, если он скрыт.</span><span class="sxs-lookup"><span data-stu-id="53ddc-124">This action gives the specified object the focus and shows the object if it's hidden.</span></span> <span data-ttu-id="53ddc-125">Если объект является формой, действие **SelectObject** задает для свойства **Visible** формы свойство **Yes** и возвращает форму в режим, замеенный свойствами формы (например, в виде модальной или всплывающее формы).</span><span class="sxs-lookup"><span data-stu-id="53ddc-125">If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="53ddc-126">Если объект не открыт в одном из других окон Access, его можно выбрать  в области навигации, установив для аргумента в области навигации **"Да".**</span><span class="sxs-lookup"><span data-stu-id="53ddc-126">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**.</span></span> <span data-ttu-id="53ddc-127">Если для  аргумента в области навигации установлено **"Нет",** при попытке выбрать объект, который не открыт, появляется сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="53ddc-127">If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="53ddc-128">Часто это действие можно использовать для выбора объекта, для которого необходимо выполнить дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="53ddc-128">Often, you might use this action to select an object on which you want to perform additional actions.</span></span> <span data-ttu-id="53ddc-129">Например, если в Access настроено использование перекрывающихся окон вместо документов с вкладками, может потребоваться восстановить свернутый объект (с помощью действия **RestoreWindow)** или развернуть окно с объектом, с помощью действия **MaximizeWindow.**</span><span class="sxs-lookup"><span data-stu-id="53ddc-129">For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="53ddc-130">При выборе формы можно использовать действия **GoToControl,** **GoToRecord** и **GoToPage** для перемещения в определенные области формы.</span><span class="sxs-lookup"><span data-stu-id="53ddc-130">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form.</span></span> <span data-ttu-id="53ddc-131">Действие **GoToRecord** также работает для таблиц.</span><span class="sxs-lookup"><span data-stu-id="53ddc-131">The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="53ddc-132">Чтобы запустить **действие SelectObject** в модуле Visual Basic для приложений (VBA), используйте метод **SelectObject** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="53ddc-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

