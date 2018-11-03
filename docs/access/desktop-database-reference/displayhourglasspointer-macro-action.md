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
ms.openlocfilehash: 159e9f1b4cf7beab96a463ff476b4edf577e1371
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926936"
---
# <a name="displayhourglasspointer-macro-action"></a><span data-ttu-id="38c4e-102">Макрокоманда DisplayHourglassPointer</span><span class="sxs-lookup"><span data-stu-id="38c4e-102">DisplayHourglassPointer macro action</span></span>


<span data-ttu-id="38c4e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="38c4e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="38c4e-104">Чтобы изменить указатель мыши на изображение песочными можно использовать действие **DisplayHourglassPointer** (или другой значок выбора) во время выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="38c4e-104">You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running.</span></span> <span data-ttu-id="38c4e-105">Это действие может предоставить визуальный индикатор, на котором выполняется макрос.</span><span class="sxs-lookup"><span data-stu-id="38c4e-105">This action can provide a visual indication that the macro is running.</span></span> <span data-ttu-id="38c4e-106">Эта функция особенно полезна, когда действия макроса или самого макроса занимает много времени для запуска.</span><span class="sxs-lookup"><span data-stu-id="38c4e-106">This is especially useful when a macro action or the macro itself takes a long time to run.</span></span>

## <a name="setting"></a><span data-ttu-id="38c4e-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="38c4e-107">Setting</span></span>

<span data-ttu-id="38c4e-108">Действие **DisplayHourglassPointer** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="38c4e-108">The **DisplayHourglassPointer** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38c4e-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="38c4e-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="38c4e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="38c4e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38c4e-111"><strong>Включить</strong></span><span class="sxs-lookup"><span data-stu-id="38c4e-111"><strong>Hourglass On</strong></span></span></p></td>
<td><p><span data-ttu-id="38c4e-112">Нажмите кнопку <strong>Да</strong> (отображение значка) или <strong>Нет</strong> (Отображение обычной указателем мыши) в поле <strong>Включить</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов.</span><span class="sxs-lookup"><span data-stu-id="38c4e-112">Click <strong>Yes</strong> (display the icon) or <strong>No</strong> (display the normal mouse pointer) in the <strong>Hourglass On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="38c4e-113">По умолчанию используется значение <strong>Да</strong>.</span><span class="sxs-lookup"><span data-stu-id="38c4e-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="38c4e-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="38c4e-114">Remarks</span></span>

<span data-ttu-id="38c4e-115">Это действие часто используется, если вы отключили эхо с помощью действия **эхо** .</span><span class="sxs-lookup"><span data-stu-id="38c4e-115">You often use this action if you have turned echo off by using the **Echo** action.</span></span> <span data-ttu-id="38c4e-116">При отключенном эхо приостанавливается обновления экрана до завершения макроса.</span><span class="sxs-lookup"><span data-stu-id="38c4e-116">When echo is off, Access suspends screen updates until the macro is finished.</span></span>

<span data-ttu-id="38c4e-117">Access автоматически устанавливает **Песочные часы для** аргумента **не** после завершения выполнения макроса.</span><span class="sxs-lookup"><span data-stu-id="38c4e-117">Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.</span></span>

> [!NOTE]
> - <span data-ttu-id="38c4e-118">В Microsoft Windows это значок, заданные для **«занят»** в диалоговом окне **Свойства: мышь** панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="38c4e-118">In Microsoft Windows, this is the icon you set for **Busy** in the **Mouse Properties** dialog box of Windows Control Panel.</span></span> <span data-ttu-id="38c4e-119">Значение по умолчанию для всех операционных систем Windows — значок анимационной песочными часами.</span><span class="sxs-lookup"><span data-stu-id="38c4e-119">The default for all Windows operating systems is an animated hourglass icon.</span></span>
> - <span data-ttu-id="38c4e-120">Если вы хотите, чтобы можно выбрать другой значок.</span><span class="sxs-lookup"><span data-stu-id="38c4e-120">You can choose another icon if you want.</span></span>

<span data-ttu-id="38c4e-121">Чтобы выполнить действие **DisplayHourglassPointer** в Visual Basic для приложений (VBA) модуль, используйте метод **песочные часы** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="38c4e-121">To run the **DisplayHourglassPointer** action in a Visual Basic for Applications (VBA) module, use the **Hourglass** method of the **DoCmd** object.</span></span>

