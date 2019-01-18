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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711422"
---
# <a name="setdisplayedcategories-macro-action"></a><span data-ttu-id="f9a19-102">Макрокоманда SetDisplayedCategories</span><span class="sxs-lookup"><span data-stu-id="f9a19-102">SetDisplayedCategories macro action</span></span>


<span data-ttu-id="f9a19-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f9a19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f9a19-104">Чтобы указать, какие категории отображаются в разделе **Перейти по категории** в строке заголовка области переходов можно использовать действие **SetDisplayedCategories** .</span><span class="sxs-lookup"><span data-stu-id="f9a19-104">You can use the **SetDisplayedCategories** action to specify which categories are displayed under **Navigate to Category** in the title bar of the Navigation Pane.</span></span> <span data-ttu-id="f9a19-105">Например если вы хотите запретить пользователям переходить на панели переходов, чтобы она отображала объекты, отсортированные по **Дата создания**, можно использовать это действие для скрытия соответствующий параметр в строке заголовка раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="f9a19-105">For example, if you want to prevent users from switching the Navigation Pane so that it displays objects sorted by **Created Date**, you can use this action to hide that option in the title bar's drop-down list.</span></span>

## <a name="setting"></a><span data-ttu-id="f9a19-106">Setting</span><span class="sxs-lookup"><span data-stu-id="f9a19-106">Setting</span></span>

<span data-ttu-id="f9a19-107">Действие **SetDisplayedCategories** состоит из следующих аргументов.</span><span class="sxs-lookup"><span data-stu-id="f9a19-107">The **SetDisplayedCategories** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f9a19-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="f9a19-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f9a19-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f9a19-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9a19-110"><strong>Show</strong></span><span class="sxs-lookup"><span data-stu-id="f9a19-110"><strong>Show</strong></span></span></p></td>
<td><p><span data-ttu-id="f9a19-111">Выберите <strong>Да,</strong> чтобы показать категорию или категории.</span><span class="sxs-lookup"><span data-stu-id="f9a19-111">Select <strong>Yes</strong> to show the category or categories.</span></span> <span data-ttu-id="f9a19-112">Выберите <strong>Нет</strong> , чтобы скрыть их.</span><span class="sxs-lookup"><span data-stu-id="f9a19-112">Select <strong>No</strong> to hide them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9a19-113"><strong>Category</strong></span><span class="sxs-lookup"><span data-stu-id="f9a19-113"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="f9a19-114">Введите или выберите имя категории, которые необходимо показать или скрыть.</span><span class="sxs-lookup"><span data-stu-id="f9a19-114">Enter or select the name of the category you want to show or hide.</span></span> <span data-ttu-id="f9a19-115">Оставьте поле пустым, чтобы показать или скрыть все категории.</span><span class="sxs-lookup"><span data-stu-id="f9a19-115">Leave blank to show or hide all categories.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="f9a19-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9a19-116">Remarks</span></span>

  - <span data-ttu-id="f9a19-117">Заголовок в строке заголовка области переходов указывает, какие фильтра при их наличии, в настоящее время активно.</span><span class="sxs-lookup"><span data-stu-id="f9a19-117">The caption in the title bar of the Navigation pane indicates which filter, if any, is currently active.</span></span> <span data-ttu-id="f9a19-118">Щелкните в любом месте панели для отображения раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="f9a19-118">Click anywhere in the bar to display the drop-down list.</span></span> <span data-ttu-id="f9a19-119">Элементы, которыми управляет это действие макроса перечислены в разделе **Перейти по категории**.</span><span class="sxs-lookup"><span data-stu-id="f9a19-119">The items that this macro action controls are listed under **Navigate to Category**.</span></span>

  - <span data-ttu-id="f9a19-120">Это действие только включает или отключает отображение указанной категории, или; не выполняет переключение отображения области переходов.</span><span class="sxs-lookup"><span data-stu-id="f9a19-120">This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display.</span></span> <span data-ttu-id="f9a19-121">К примеру при отображении объектов, отсортированные по **Дата создания** и использовать действие **SetDisplayedCategories** , чтобы отключить параметр **Дата создания** , доступа не переключитесь в области навигации другой категории.</span><span class="sxs-lookup"><span data-stu-id="f9a19-121">For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.</span></span>

  - <span data-ttu-id="f9a19-122">Чтобы выполнить действие **SetDisplayedCategories** в модуле VBA, используйте метод **SetDisplayedCategories** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="f9a19-122">To run the **SetDisplayedCategories** action in a VBA module, use the **SetDisplayedCategories** method of the **DoCmd** object.</span></span>

