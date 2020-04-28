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
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="f6bd9-102">Макрокоманда SetDisplayedCategories</span><span class="sxs-lookup"><span data-stu-id="f6bd9-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="f6bd9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6bd9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6bd9-104">Вы можете использовать действие **сетдисплайедкатегориес** для указания категорий, отображаемых в разделе **Перейти к категории** в строке заголовка области навигации.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-104">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane.</span></span> <span data-ttu-id="f6bd9-105">Например, если необходимо запретить пользователям переключать область навигации, чтобы она отображала объекты, отсортированные по **дате создания**, можно использовать это действие для скрытия этого параметра в раскрывающемся списке строки заголовка.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-105">For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="f6bd9-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="f6bd9-106">Setting</span></span>

<span data-ttu-id="f6bd9-107">Макрокоманда **сетдисплайедкатегориес** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6bd9-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="f6bd9-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f6bd9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f6bd9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6bd9-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="f6bd9-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="f6bd9-111">Выберите <strong>Да</strong> , чтобы отобразить категории или категории.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-111">Select <strong>Yes</strong> to show the category or categories.</span></span> <span data-ttu-id="f6bd9-112">Нажмите кнопку <strong>нет</strong> , чтобы скрыть их.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-112">Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6bd9-113"><strong>Категория</strong></span><span class="sxs-lookup"><span data-stu-id="f6bd9-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="f6bd9-114">Введите или выберите имя категории, которую требуется показать или скрыть.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-114">Enter or select the name of the category you want to show or hide.</span></span> <span data-ttu-id="f6bd9-115">Оставьте поле пустым, чтобы показать или скрыть все категории.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-115">Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f6bd9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="f6bd9-116">Remarks</span></span>

  - <span data-ttu-id="f6bd9-117">Заголовок в строке заголовка области навигации указывает, какой фильтр в данный момент активен.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-117">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active.</span></span> <span data-ttu-id="f6bd9-118">Щелкните в любом месте панели, чтобы отобразить раскрывающийся список.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-118">Click anywhere in the bar to display the drop-down list.</span></span> <span data-ttu-id="f6bd9-119">Элементы управления действиями макроса отображаются в разделе **Перейти к категории**.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-119">The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="f6bd9-120">Это действие включает или отключает отображение указанных категорий или категорий. Он не выполняет переключения в область навигации.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-120">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display.</span></span> <span data-ttu-id="f6bd9-121">Например, если вы отображаете объекты, отсортированные по **дате создания** , и используете действие **сетдисплайедкатегориес** для отключения параметра **Дата создания** , Access не переключует область навигации в другую категорию.</span><span class="sxs-lookup"><span data-stu-id="f6bd9-121">For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="f6bd9-122">Чтобы выполнить действие **сетдисплайедкатегориес** в модуле VBA, используйте метод **сетдисплайедкатегориес** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="f6bd9-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

