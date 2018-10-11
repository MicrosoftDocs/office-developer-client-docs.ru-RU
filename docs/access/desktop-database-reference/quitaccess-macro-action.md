---
title: QuitAccess Macro Action
TOCTitle: QuitAccess Macro Action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5fa3b7ffc97f69b1ebc85799a8b2a27b6acc1d90
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479946"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="40ce8-102">QuitAccess Macro Action</span><span class="sxs-lookup"><span data-stu-id="40ce8-102">QuitAccess Macro Action</span></span>


<span data-ttu-id="40ce8-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40ce8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40ce8-104">Действие **QuitAccess** можно использовать, чтобы выйти из Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="40ce8-104">You can use the **QuitAccess** action to exit Microsoft Access.</span></span> <span data-ttu-id="40ce8-105">Действие **QuitAccess** можно указать один из параметров сохранения объектов базы данных.</span><span class="sxs-lookup"><span data-stu-id="40ce8-105">The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>


> [!NOTE]
> <P><span data-ttu-id="40ce8-p102">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="40ce8-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="40ce8-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="40ce8-108">Setting</span></span>

<span data-ttu-id="40ce8-109">Действие **QuitAccess** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="40ce8-109">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40ce8-110">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="40ce8-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="40ce8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="40ce8-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40ce8-112"><strong>Варианты</strong></span><span class="sxs-lookup"><span data-stu-id="40ce8-112"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="40ce8-113">Указывает, что происходит с несохраненными объектами при завершении работы Access.</span><span class="sxs-lookup"><span data-stu-id="40ce8-113">Specifies what happens to unsaved objects when you quit Access.</span></span> <span data-ttu-id="40ce8-114">Выберите <strong>запрос</strong> (для отображения диалоговых окон, которые ли сохранять каждый объект), <strong>Сохранить все</strong> (для сохранения всех объектов без запроса, диалоговые окна), или <strong>выйти из</strong> (без сохранения объектов) в поле <strong>Параметры</strong> в <strong>Действие Аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="40ce8-114">Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="40ce8-115">Значение по умолчанию — <strong>Сохранить все</strong>.</span><span class="sxs-lookup"><span data-stu-id="40ce8-115">The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="40ce8-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="40ce8-116">Remarks</span></span>

<span data-ttu-id="40ce8-117">Access не выполните все действия, которые выполните действие **QuitAccess** в макросе.</span><span class="sxs-lookup"><span data-stu-id="40ce8-117">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="40ce8-118">Это действие можно использовать для завершения работы приложения Access без предупреждений из **Сохранить** диалоговых окон с помощью команды меню или кнопки на форме.</span><span class="sxs-lookup"><span data-stu-id="40ce8-118">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form.</span></span> <span data-ttu-id="40ce8-119">Например возможно главной формы, которая используется для отображения в рабочей области, настраиваемых объектов.</span><span class="sxs-lookup"><span data-stu-id="40ce8-119">For example, you might have a master form that you use to display the objects in your custom workspace.</span></span> <span data-ttu-id="40ce8-120">Эта форма может содержать кнопку **Quit** , которая запускает макрос, содержащий действие **QuitAccess** со значением **Сохранить все** **Параметры** аргумента.</span><span class="sxs-lookup"><span data-stu-id="40ce8-120">This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="40ce8-121">Это действие имеет тот же эффект, как на вкладку **файл** и выбрав команду **Выход**.</span><span class="sxs-lookup"><span data-stu-id="40ce8-121">This action has the same effect as clicking the **File** tab and then clicking **Exit**.</span></span> <span data-ttu-id="40ce8-122">При наличии несохраненных объектов при выполнении этой команды, диалоговые окна, которые отображаются такие же, как, отображаемые при использовании **приглашениями** для аргумента **Options** **QuitAccess** действие.</span><span class="sxs-lookup"><span data-stu-id="40ce8-122">If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="40ce8-123">Действие **SaveObject** можно использовать в макросе для сохранения указанный объект без выхода из Access или закрытия объекта.</span><span class="sxs-lookup"><span data-stu-id="40ce8-123">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="40ce8-124">Чтобы выполнить действие **QuitAccess** в Visual Basic для приложений (VBA) модуль, используйте метод **Quit** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="40ce8-124">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>

