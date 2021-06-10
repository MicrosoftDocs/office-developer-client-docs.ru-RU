---
title: Макрокоманда SetDisplayedCategories
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314627"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="408f3-102">Макрокоманда SetDisplayedCategories</span><span class="sxs-lookup"><span data-stu-id="408f3-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="408f3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="408f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="408f3-104">Вы можете использовать **действие SetDisplayedCategories,** чтобы указать, какие категории отображаются в статье **Перейдите** к категории в панели заголовков панели навигации.</span><span class="sxs-lookup"><span data-stu-id="408f3-104">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane.</span></span> <span data-ttu-id="408f3-105">Например, если вы хотите запретить пользователям переключение панели навигации, чтобы она отображала объекты, отсортированные по **созданной** дате, вы можете использовать это действие, чтобы скрыть этот параметр в выпадаемом списке панели заголовка.</span><span class="sxs-lookup"><span data-stu-id="408f3-105">For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="408f3-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="408f3-106">Setting</span></span>

<span data-ttu-id="408f3-107">Действие **SetDisplayedCategories** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="408f3-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="408f3-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="408f3-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="408f3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="408f3-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="408f3-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="408f3-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="408f3-111">Выберите <strong>Да,</strong> чтобы показать категорию или категории.</span><span class="sxs-lookup"><span data-stu-id="408f3-111">Select <strong>Yes</strong> to show the category or categories.</span></span> <span data-ttu-id="408f3-112">Выберите <strong>Нет,</strong> чтобы скрыть их.</span><span class="sxs-lookup"><span data-stu-id="408f3-112">Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="408f3-113"><strong>Категория</strong></span><span class="sxs-lookup"><span data-stu-id="408f3-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="408f3-114">Введите или выберите имя категории, которая будет показываться или скрываться.</span><span class="sxs-lookup"><span data-stu-id="408f3-114">Enter or select the name of the category you want to show or hide.</span></span> <span data-ttu-id="408f3-115">Оставьте пустым, чтобы показать или скрыть все категории.</span><span class="sxs-lookup"><span data-stu-id="408f3-115">Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="408f3-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="408f3-116">Remarks</span></span>

  - <span data-ttu-id="408f3-117">Подпись в панели заголовка панели навигации указывает, какой фильтр, если таково, в настоящее время активен.</span><span class="sxs-lookup"><span data-stu-id="408f3-117">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active.</span></span> <span data-ttu-id="408f3-118">Щелкните в любом месте панели, чтобы отобразить выпадаемый список.</span><span class="sxs-lookup"><span data-stu-id="408f3-118">Click anywhere in the bar to display the drop-down list.</span></span> <span data-ttu-id="408f3-119">Элементы, указанные в элементе управления макросами, перечислены в **статье Перейдите к категории**.</span><span class="sxs-lookup"><span data-stu-id="408f3-119">The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="408f3-120">Это действие включает или отключает отображение указанной категории или категорий; он не выполняет переключения экрана навигации.</span><span class="sxs-lookup"><span data-stu-id="408f3-120">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display.</span></span> <span data-ttu-id="408f3-121">Например, если отобразить объекты, отсортированные по дате создания, и вы используете действие **SetDisplayedCategories** для отключения параметра **Дата** создания, Access не переключает области навигации на другую категорию. </span><span class="sxs-lookup"><span data-stu-id="408f3-121">For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="408f3-122">Для запуска **действия SetDisplayedCategories** в модуле VBA используйте метод **SetDisplayedCategories** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="408f3-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

