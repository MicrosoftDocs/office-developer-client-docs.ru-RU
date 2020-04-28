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
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="0e166-102">Макрокоманда DisplayHourglassPointer</span><span class="sxs-lookup"><span data-stu-id="0e166-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="0e166-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e166-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e166-104">Вы можете использовать действие **дисплайхаургласспоинтер** , чтобы изменить указатель мыши на изображение песочных часов (или другой значок, который вы выбрали) во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="0e166-104">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running.</span></span> <span data-ttu-id="0e166-105">Это действие может предоставить визуальную индикацию выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="0e166-105">This action can provide a visual indication that the macro is running.</span></span> <span data-ttu-id="0e166-106">Это особенно полезно, если для запуска макрокоманды или самого макроса требуется много времени.</span><span class="sxs-lookup"><span data-stu-id="0e166-106">This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="0e166-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="0e166-107">Setting</span></span>

<span data-ttu-id="0e166-108">Действие **дисплайхаургласспоинтер** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="0e166-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e166-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="0e166-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="0e166-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0e166-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e166-111"><strong>Песочные часы</strong></span><span class="sxs-lookup"><span data-stu-id="0e166-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="0e166-112">Нажмите кнопку <strong>Да</strong> (отображать значок) или <strong>нет</strong> (отображать обычный указатель мыши) в поле <strong>Песочные часы</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов.</span><span class="sxs-lookup"><span data-stu-id="0e166-112">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="0e166-113">Значение по умолчанию — <strong>Yes</strong>.</span><span class="sxs-lookup"><span data-stu-id="0e166-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e166-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e166-114">Remarks</span></span>

<span data-ttu-id="0e166-115">Это действие часто используется, если вы отключили эхо с помощью макрокоманды **echo** .</span><span class="sxs-lookup"><span data-stu-id="0e166-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="0e166-116">Когда ECHO отключено, Access приостанавливает обновление экрана до завершения макроса.</span><span class="sxs-lookup"><span data-stu-id="0e166-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="0e166-117">Access автоматически сбрасывает значение параметра " **Песочные часы** " в значение " **нет** " при завершении выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="0e166-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="0e166-118">В Microsoft Windows это значок, заданный для свойства " **занято** " в диалоговом окне " **Свойства мыши** " на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="0e166-118">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel.</span></span> <span data-ttu-id="0e166-119">По умолчанию для всех операционных систем Windows используется анимированный значок песочных часов.</span><span class="sxs-lookup"><span data-stu-id="0e166-119">The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="0e166-120">При необходимости можно выбрать другой значок.</span><span class="sxs-lookup"><span data-stu-id="0e166-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="0e166-121">Чтобы запустить действие **дисплайхаургласспоинтер** в модуле Visual Basic для приложений (VBA), используйте метод **песочных часов** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="0e166-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

