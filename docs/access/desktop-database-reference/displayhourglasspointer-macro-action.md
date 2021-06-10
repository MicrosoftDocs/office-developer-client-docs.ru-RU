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
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="04785-102">Макрокоманда DisplayHourglassPointer</span><span class="sxs-lookup"><span data-stu-id="04785-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="04785-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04785-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04785-104">Вы можете использовать **действие DisplayHourglassPointer,** чтобы изменить указатель мыши на изображение песочных часов (или другой выбранный значок) во время работы макроса.</span><span class="sxs-lookup"><span data-stu-id="04785-104">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running.</span></span> <span data-ttu-id="04785-105">Это действие может дать наглядное представление о том, что макрос запущен.</span><span class="sxs-lookup"><span data-stu-id="04785-105">This action can provide a visual indication that the macro is running.</span></span> <span data-ttu-id="04785-106">Это особенно полезно, когда макрос или сам макрос занимает много времени для запуска.</span><span class="sxs-lookup"><span data-stu-id="04785-106">This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="04785-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="04785-107">Setting</span></span>

<span data-ttu-id="04785-108">Действие **DisplayHourglassPointer имеет** следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="04785-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04785-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="04785-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="04785-110">Описание</span><span class="sxs-lookup"><span data-stu-id="04785-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04785-111"><strong>Песочные часы</strong></span><span class="sxs-lookup"><span data-stu-id="04785-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="04785-112">Щелкните <strong>Да</strong> (отобразить значок) или <strong>Нет</strong> <strong></strong> (отобразить <strong></strong> обычную указатель мыши) в поле Песочные часы в разделе Аргументы действий области Macro Builder.</span><span class="sxs-lookup"><span data-stu-id="04785-112">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="04785-113">По умолчанию — <strong>Да.</strong></span><span class="sxs-lookup"><span data-stu-id="04785-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="04785-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="04785-114">Remarks</span></span>

<span data-ttu-id="04785-115">Вы часто используете это действие, если вы отключили эхо с помощью **действия Echo.**</span><span class="sxs-lookup"><span data-stu-id="04785-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="04785-116">Когда эхо отключено, Access приостанавливать обновления экрана до завершения макроса.</span><span class="sxs-lookup"><span data-stu-id="04785-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="04785-117">При запуске макроса доступ автоматически сбрасывает песочные часы **На** **аргументе Нет.**</span><span class="sxs-lookup"><span data-stu-id="04785-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="04785-118">В microsoft Windows это значок, заданной для занят в диалоговом окне **Свойства** мыши Windows панели управления. </span><span class="sxs-lookup"><span data-stu-id="04785-118">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel.</span></span> <span data-ttu-id="04785-119">По умолчанию для всех Windows операционных систем является анимированный значок песочных часов.</span><span class="sxs-lookup"><span data-stu-id="04785-119">The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="04785-120">Вы можете выбрать другой значок, если хотите.</span><span class="sxs-lookup"><span data-stu-id="04785-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="04785-121">Чтобы выполнить **действие DisplayHourglassPointer** в модуле Visual Basic для приложений (VBA), используйте метод **Песочные** часы объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="04785-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

