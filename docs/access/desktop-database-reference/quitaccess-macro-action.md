---
title: Макрокоманда QuitAccess
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 793e6c2e57f50b5086780d8632952c45f3d4442d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997987"
---
# <a name="quitaccess-macro-action"></a><span data-ttu-id="f46b1-102">Макрокоманда QuitAccess</span><span class="sxs-lookup"><span data-stu-id="f46b1-102">QuitAccess macro action</span></span>

<span data-ttu-id="f46b1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f46b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f46b1-104">Действие **QuitAccess** можно использовать, чтобы выйти из Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f46b1-104">You can use the **QuitAccess** action to exit Microsoft Access.</span></span> <span data-ttu-id="f46b1-105">Действие **QuitAccess** можно указать один из параметров сохранения объектов базы данных.</span><span class="sxs-lookup"><span data-stu-id="f46b1-105">The **QuitAccess** action can also specify one of several options for saving database objects prior to exiting Access.</span></span>

> [!NOTE]
> <span data-ttu-id="f46b1-106">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="f46b1-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="f46b1-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="f46b1-107">Setting</span></span>

<span data-ttu-id="f46b1-108">Действие **QuitAccess** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="f46b1-108">The **QuitAccess** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f46b1-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="f46b1-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f46b1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="f46b1-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f46b1-111"><strong>Варианты</strong></span><span class="sxs-lookup"><span data-stu-id="f46b1-111"><strong>Options</strong></span></span></p></td>
<td><p><span data-ttu-id="f46b1-112">Указывает, что происходит с несохраненными объектами при завершении работы Access.</span><span class="sxs-lookup"><span data-stu-id="f46b1-112">Specifies what happens to unsaved objects when you quit Access.</span></span> <span data-ttu-id="f46b1-113">Выберите <strong>запрос</strong> (для отображения диалоговых окон, которые ли сохранять каждый объект), <strong>Сохранить все</strong> (для сохранения всех объектов без запроса, диалоговые окна), или <strong>выйти из</strong> (без сохранения объектов) в поле <strong>Параметры</strong> в <strong>Действие Аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="f46b1-113">Click <strong>Prompt</strong> (to display dialog boxes that ask whether to save each object), <strong>Save All</strong> (to save all objects without prompting by dialog boxes), or <strong>Exit</strong> (to quit without saving any objects) in the <strong>Options</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="f46b1-114">Значение по умолчанию — <strong>Сохранить все</strong>.</span><span class="sxs-lookup"><span data-stu-id="f46b1-114">The default is <strong>Save All</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f46b1-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f46b1-115">Remarks</span></span>

<span data-ttu-id="f46b1-116">Access не выполните все действия, которые выполните действие **QuitAccess** в макросе.</span><span class="sxs-lookup"><span data-stu-id="f46b1-116">Access doesn't run any actions that follow the **QuitAccess** action in a macro.</span></span>

<span data-ttu-id="f46b1-117">Это действие можно использовать для завершения работы приложения Access без предупреждений из **Сохранить** диалоговых окон с помощью команды меню или кнопки на форме.</span><span class="sxs-lookup"><span data-stu-id="f46b1-117">You can use this action to quit Access without prompts from **Save** dialog boxes by using a custom menu command or a button on a form.</span></span> <span data-ttu-id="f46b1-118">Например возможно главной формы, которая используется для отображения в рабочей области, настраиваемых объектов.</span><span class="sxs-lookup"><span data-stu-id="f46b1-118">For example, you might have a master form that you use to display the objects in your custom workspace.</span></span> <span data-ttu-id="f46b1-119">Эта форма может содержать кнопку **Quit** , которая запускает макрос, содержащий действие **QuitAccess** со значением **Сохранить все** **Параметры** аргумента.</span><span class="sxs-lookup"><span data-stu-id="f46b1-119">This form could have a **Quit** button that runs a macro containing the **QuitAccess** action with the **Options** argument set to **Save All**.</span></span>

<span data-ttu-id="f46b1-120">Это действие имеет тот же эффект, как на вкладку **файл** и выбрав команду **Выход**.</span><span class="sxs-lookup"><span data-stu-id="f46b1-120">This action has the same effect as clicking the **File** tab and then clicking **Exit**.</span></span> <span data-ttu-id="f46b1-121">При наличии несохраненных объектов при выполнении этой команды, диалоговые окна, которые отображаются такие же, как, отображаемые при использовании **приглашениями** для аргумента **Options** **QuitAccess** действие.</span><span class="sxs-lookup"><span data-stu-id="f46b1-121">If you have any unsaved objects when you click this command, the dialog boxes that appear are the same as those displayed when you use **Prompt** for the **Options** argument of the **QuitAccess** action.</span></span>

<span data-ttu-id="f46b1-122">Действие **SaveObject** можно использовать в макросе для сохранения указанный объект без выхода из Access или закрытия объекта.</span><span class="sxs-lookup"><span data-stu-id="f46b1-122">You can use the **SaveObject** action in a macro to save a specified object without having to quit Access or close the object.</span></span>

<span data-ttu-id="f46b1-123">Чтобы выполнить действие **QuitAccess** в Visual Basic для приложений (VBA) модуль, используйте метод **Quit** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="f46b1-123">To run the **QuitAccess** action in a Visual Basic for Applications (VBA) module, use the **Quit** method of the **DoCmd** object.</span></span>

