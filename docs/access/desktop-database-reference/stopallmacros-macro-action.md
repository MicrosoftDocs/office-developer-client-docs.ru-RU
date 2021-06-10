---
title: Макрокоманда StopAllMacros
TOCTitle: StopAllMacros macro action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4e44182dd4290b05a2cfc8fabdf9240819f4b7aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314478"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="60f33-102">Макрокоманда StopAllMacros</span><span class="sxs-lookup"><span data-stu-id="60f33-102">StopAllMacros macro action</span></span>


<span data-ttu-id="60f33-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60f33-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60f33-104">Вы можете использовать действие **StopAllMacros** для остановки всех запущенных макросов.</span><span class="sxs-lookup"><span data-stu-id="60f33-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="60f33-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="60f33-105">Setting</span></span>

<span data-ttu-id="60f33-106">Действие **StopAllMacros** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="60f33-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="60f33-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="60f33-107">Remarks</span></span>

<span data-ttu-id="60f33-108">Обычно это действие используется, когда из-за условия ошибки необходимо остановить все макрос.</span><span class="sxs-lookup"><span data-stu-id="60f33-108">You typically use this action when an error condition makes it necessary to stop all macros.</span></span> <span data-ttu-id="60f33-109">В строке действий макроса можно использовать условное выражение, которое содержит это действие.</span><span class="sxs-lookup"><span data-stu-id="60f33-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="60f33-110">При оценке выражения **True** (-1) Microsoft Access останавливает все макрос.</span><span class="sxs-lookup"><span data-stu-id="60f33-110">When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="60f33-111">Например, у вас может быть макрос, который отображает поле сообщений в качестве одного из нескольких сложных действий, включая запуск других макрос.</span><span class="sxs-lookup"><span data-stu-id="60f33-111">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros.</span></span> <span data-ttu-id="60f33-112">Если пользователь нажмет **отмену** в этом поле сообщений, действие **StopAllMacros** может остановить все запущенные макросов.</span><span class="sxs-lookup"><span data-stu-id="60f33-112">If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="60f33-113">Если макрос использовал действия **Echo** или **SetWarnings** для отключения эхо или отображения системных сообщений, действие **StopAllMacros** автоматически включает их обратно.</span><span class="sxs-lookup"><span data-stu-id="60f33-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="60f33-114">Это действие не доступно в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="60f33-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

