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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721852"
---
# <a name="selectobject-macro-action"></a><span data-ttu-id="1201b-102">Макрокоманда SelectObject</span><span class="sxs-lookup"><span data-stu-id="1201b-102">SelectObject macro action</span></span>

<span data-ttu-id="1201b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1201b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1201b-104">**ВыделитьОбъект** можно использовать для выбора объекта указанной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1201b-104">You can use the **SelectObject** action to select a specified database object.</span></span>

## <a name="setting"></a><span data-ttu-id="1201b-105">Setting</span><span class="sxs-lookup"><span data-stu-id="1201b-105">Setting</span></span>

<span data-ttu-id="1201b-106">**ВыделитьОбъект** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="1201b-106">The **SelectObject** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1201b-107">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="1201b-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1201b-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1201b-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1201b-109"><strong>Тип объекта</strong></span><span class="sxs-lookup"><span data-stu-id="1201b-109"><strong>Object Type</strong></span></span></p></td>
<td><p><span data-ttu-id="1201b-110">Тип объекта базы данных для выбора.</span><span class="sxs-lookup"><span data-stu-id="1201b-110">The type of database object to select.</span></span> <span data-ttu-id="1201b-111">Выберите <strong>таблицы</strong>, <strong>запроса</strong>, <strong>формы</strong>, <strong>отчета</strong>, <strong>макрос</strong>, <strong>модуль</strong>, <strong>страницы доступа к данным</strong>, <strong>представление</strong>, <strong>Схема</strong>, <strong>хранимая процедура</strong>или <strong>функции</strong> в тип объекта <strong> </strong>флажок в разделе <strong>Действие аргументы</strong> области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="1201b-111">Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="1201b-112">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="1201b-112">This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1201b-113"><strong>Имя объекта</strong></span><span class="sxs-lookup"><span data-stu-id="1201b-113"><strong>Object Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1201b-114">Имя объекта для выбора.</span><span class="sxs-lookup"><span data-stu-id="1201b-114">The name of the object to select.</span></span> <span data-ttu-id="1201b-115">В поле <strong>Имя объекта</strong> содержит все объекты базы данных, указанному в аргументе <strong>Тип объекта</strong> типа.</span><span class="sxs-lookup"><span data-stu-id="1201b-115">The <strong>Object Name</strong> box shows all objects in the database of the type selected by the <strong>Object Type</strong> argument.</span></span> <span data-ttu-id="1201b-116">Это аргумент является обязательным, если не выбрано значение " <strong>Да"</strong>аргумент в области переходов.</span><span class="sxs-lookup"><span data-stu-id="1201b-116">This is a required argument, unless you set the In Navigation Pane argument to <strong>Yes</strong>.</span></span></p><p><span data-ttu-id="1201b-117"><strong>Примечание</strong>: имена объектов для объектов- <STRONG>Представление</STRONG>, <STRONG>Схема</STRONG>или <STRONG>Хранимую процедуру</STRONG> не отображается в поле <STRONG>Имя объекта</STRONG> проекта Access (файлы с расширением ADP).</span><span class="sxs-lookup"><span data-stu-id="1201b-117"><strong>NOTE</strong>: The object names for <STRONG>Server View</STRONG>, <STRONG>Diagram</STRONG>, or <STRONG>Stored Procedure</STRONG> objects are not displayed in the <STRONG>Object Name</STRONG> box of an Access project (.adp).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1201b-118"><strong>В области переходов</strong></span><span class="sxs-lookup"><span data-stu-id="1201b-118"><strong>In Navigation Pane</strong></span></span></p></td>
<td><p><span data-ttu-id="1201b-119">Указывает, будет ли Microsoft Access выбирает объект на левой панели навигации.</span><span class="sxs-lookup"><span data-stu-id="1201b-119">Specifies whether Microsoft Access selects the object in the Navigation Pane.</span></span> <span data-ttu-id="1201b-120">Нажмите кнопку <strong>Да</strong> (для выбора объекта в области переходов) или <strong>Нет</strong> (не для выбора объекта в области переходов).</span><span class="sxs-lookup"><span data-stu-id="1201b-120">Click <strong>Yes</strong> (to select the object in the Navigation Pane) or <strong>No</strong> (not to select the object in the Navigation Pane).</span></span> <span data-ttu-id="1201b-121">Значение по умолчанию: <strong>Нет</strong>.</span><span class="sxs-lookup"><span data-stu-id="1201b-121">The default is <strong>No</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1201b-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="1201b-122">Remarks</span></span>

<span data-ttu-id="1201b-123">**ВыделитьОбъект** работает с любой объект доступа, который может получать фокус.</span><span class="sxs-lookup"><span data-stu-id="1201b-123">The **SelectObject** action works with any Access object that can receive the focus.</span></span> <span data-ttu-id="1201b-124">Это действие предоставляет указанный объект фокус и отображается объект если оно скрыто.</span><span class="sxs-lookup"><span data-stu-id="1201b-124">This action gives the specified object the focus and shows the object if it's hidden.</span></span> <span data-ttu-id="1201b-125">Если объект является формы, **ВыделитьОбъект** задает для свойства **Visible** формы значение **Да** и возвращает форму отключен или не настроен, его свойства формы (например, как модальные окна или всплывающего формы).</span><span class="sxs-lookup"><span data-stu-id="1201b-125">If the object is a form, the **SelectObject** action sets the form's **Visible** property to **Yes** and returns the form to the mode set by its form properties (for example, as a modal or pop-up form).</span></span>

<span data-ttu-id="1201b-126">Если объект не открыт в одном из других окон Microsoft Access, можно выбрать в области навигации, задав аргумент **В области переходов** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1201b-126">If the object isn't open in one of the other Access windows, you can select it in the Navigation Pane by setting the **In Navigation Pane** argument to **Yes**.</span></span> <span data-ttu-id="1201b-127">Если значение аргумента **В области переходов** **Нет**, сообщение об ошибке появляется при попытке выберите объект, который не открыта.</span><span class="sxs-lookup"><span data-stu-id="1201b-127">If you set the **In Navigation Pane** argument to **No**, an error message appears when you try to select an object that isn't open.</span></span>

<span data-ttu-id="1201b-128">Часто это действие можно использовать для выбора объекта, на котором необходимо выполнить дополнительные действия.</span><span class="sxs-lookup"><span data-stu-id="1201b-128">Often, you might use this action to select an object on which you want to perform additional actions.</span></span> <span data-ttu-id="1201b-129">К примеру Если имеется доступ, настроены на использование перекрывающиеся windows вместо документов с вкладками можно для восстановления объект, свернутый (с помощью действия **RestoreWindow** ) или развернуть окно, содержащее объект, который вы хотите работать с (с помощью действия **MaximizeWindow** ).</span><span class="sxs-lookup"><span data-stu-id="1201b-129">For example, if you have Access configured to use overlapping windows instead of tabbed documents, you may want to restore an object that has been minimized (by using the **RestoreWindow** action) or maximize a window that contains an object you want to work with (by using the **MaximizeWindow** action).</span></span>

<span data-ttu-id="1201b-130">При выборе формы **КЭлементуУправления**, **НаЗапись**и **НаСтраницу** действия можно использовать для перемещения для конкретной области формы.</span><span class="sxs-lookup"><span data-stu-id="1201b-130">If you select a form, you can use the **GoToControl**, **GoToRecord**, and **GoToPage** actions to move to specific areas on the form.</span></span> <span data-ttu-id="1201b-131">Действие **НаЗапись** также работает для таблицы данных.</span><span class="sxs-lookup"><span data-stu-id="1201b-131">The **GoToRecord** action also works for datasheets.</span></span>

<span data-ttu-id="1201b-132">Чтобы запустить **ВыделитьОбъект** в Visual Basic для приложений (VBA) модуль, используйте метод **SelectObject** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="1201b-132">To run the **SelectObject** action in a Visual Basic for Applications (VBA) module, use the **SelectObject** method of the **DoCmd** object.</span></span>

