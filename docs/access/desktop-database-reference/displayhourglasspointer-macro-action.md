---
title: Действия макроса DisplayHourglassPointer
TOCTitle: DisplayHourglassPointer Macro Action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4d9f370fdc1ea2100178a489ad1c81225cd05199
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874617"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="62f59-102">Действия макроса DisplayHourglassPointer</span><span class="sxs-lookup"><span data-stu-id="62f59-102">DisplayHourglassPointer Macro Action</span></span>


<span data-ttu-id="62f59-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62f59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62f59-104">Чтобы изменить указатель мыши на изображение песочными можно использовать действие **DisplayHourglassPointer** (или другой значок выбора) во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="62f59-104">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running.</span></span> <span data-ttu-id="62f59-105">Это действие может предоставить визуальный индикатор, на котором выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="62f59-105">This action can provide a visual indication that the macro is running.</span></span> <span data-ttu-id="62f59-106">Эта функция особенно полезна, когда действия макроса или самого макроса занимает много времени для запуска.</span><span class="sxs-lookup"><span data-stu-id="62f59-106">This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="62f59-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="62f59-107">Setting</span></span>

<span data-ttu-id="62f59-108">Действие **DisplayHourglassPointer** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="62f59-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="62f59-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="62f59-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="62f59-110">Описание</span><span class="sxs-lookup"><span data-stu-id="62f59-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="62f59-111"><strong>Включить</strong></span><span class="sxs-lookup"><span data-stu-id="62f59-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="62f59-112">Нажмите кнопку <strong>Да</strong> (отображение значка) или <strong>Нет</strong> (Отображение обычной указателем мыши) в поле <strong>Включить</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="62f59-112">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="62f59-113">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="62f59-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="62f59-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="62f59-114">Remarks</span></span>

<span data-ttu-id="62f59-115">Это действие часто используется, если вы отключили эхо с помощью действия **эхо** .</span><span class="sxs-lookup"><span data-stu-id="62f59-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="62f59-116">При отключенном эхо приостанавливается обновления экрана до завершения макроса.</span><span class="sxs-lookup"><span data-stu-id="62f59-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="62f59-117">Access автоматически устанавливает **Песочные часы для** аргумента **не** после завершения выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="62f59-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="62f59-118">В Microsoft Windows это значок, заданные для **«занят»** в диалоговом окне **Свойства: мышь** панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="62f59-118">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel.</span></span> <span data-ttu-id="62f59-119">Значение по умолчанию для всех операционных систем Windows — значок анимационной песочными часами.</span><span class="sxs-lookup"><span data-stu-id="62f59-119">The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="62f59-120">Если вы хотите, чтобы можно выбрать другой значок.</span><span class="sxs-lookup"><span data-stu-id="62f59-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="62f59-121">Чтобы выполнить действие **DisplayHourglassPointer** в Visual Basic для приложений (VBA) модуль, используйте метод **песочные часы** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="62f59-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

