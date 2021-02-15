---
title: Макрокоманда DisplayHourglassPointer
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a5635b2b97066394b8596dbcdb50c84abf429719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293835"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="3c4e3-102">Макрокоманда DisplayHourglassPointer</span><span class="sxs-lookup"><span data-stu-id="3c4e3-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="3c4e3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c4e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c4e3-104">С помощью действия **DisplayHourglassPointer** можно изменить указатель мыши на изображение песочных часов (или другого выбранного значка) во время работы макроса.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-104">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running.</span></span> <span data-ttu-id="3c4e3-105">Это действие может предоставить визуальное указание на то, что макрос запущен.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-105">This action can provide a visual indication that the macro is running.</span></span> <span data-ttu-id="3c4e3-106">Это особенно полезно, если макрос или сам макрос занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-106">This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="3c4e3-107">Setting</span><span class="sxs-lookup"><span data-stu-id="3c4e3-107">Setting</span></span>

<span data-ttu-id="3c4e3-108">Действие **DisplayHourglassPointer** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3c4e3-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="3c4e3-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3c4e3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="3c4e3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3c4e3-111"><strong>Hourglass On</strong></span><span class="sxs-lookup"><span data-stu-id="3c4e3-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="3c4e3-112">Нажмите <strong>кнопку "Да"</strong> (отобразить значок) или "Нет" <strong></strong> <strong>(отображается</strong> обычный указатель мыши) в поле "Песочные часы <strong>на",</strong> в разделе "Аргументы действий" области построитель макроса.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-112">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="3c4e3-113">Значение по умолчанию <strong>— Да.</strong></span><span class="sxs-lookup"><span data-stu-id="3c4e3-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3c4e3-114">Заметки</span><span class="sxs-lookup"><span data-stu-id="3c4e3-114">Remarks</span></span>

<span data-ttu-id="3c4e3-115">Это действие часто используется, если вы отключили эхо с помощью действия **Echo.**</span><span class="sxs-lookup"><span data-stu-id="3c4e3-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="3c4e3-116">Когда эхо выключено, Access приостанавливать обновления экрана, пока макрос не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="3c4e3-117">Access автоматически сбрасывает аргумент **Hourglass On** на **"Нет",** когда макрос завершает работу.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="3c4e3-118">В Microsoft Windows это значок,  который вы настроите для "Занят" в диалоговом **окне** "Свойства мыши" панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-118">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel.</span></span> <span data-ttu-id="3c4e3-119">По умолчанию для всех операционных систем Windows имеется анимированный значок песочных часов.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-119">The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="3c4e3-120">При этом можно выбрать другой значок.</span><span class="sxs-lookup"><span data-stu-id="3c4e3-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="3c4e3-121">Чтобы запустить действие **DisplayHourglassPointer** в модуле Visual Basic для приложений (VBA), используйте метод **Hourglass** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="3c4e3-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

