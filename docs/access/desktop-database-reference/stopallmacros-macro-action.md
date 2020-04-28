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
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="83c9d-102">Макрокоманда StopAllMacros</span><span class="sxs-lookup"><span data-stu-id="83c9d-102">StopAllMacros macro action</span></span>


<span data-ttu-id="83c9d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="83c9d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83c9d-104">Вы можете использовать действие **Макрокоманда stopallmacros** , чтобы остановить все выполняемые в данный момент макросы.</span><span class="sxs-lookup"><span data-stu-id="83c9d-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="83c9d-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="83c9d-105">Setting</span></span>

<span data-ttu-id="83c9d-106">Макрокоманда **Макрокоманда stopallmacros** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="83c9d-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="83c9d-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="83c9d-107">Remarks</span></span>

<span data-ttu-id="83c9d-108">Обычно это действие используется, когда условие ошибки делает необходимо остановить все макросы.</span><span class="sxs-lookup"><span data-stu-id="83c9d-108">You typically use this action when an error condition makes it necessary to stop all macros.</span></span> <span data-ttu-id="83c9d-109">В строке действий макроса, содержащей это действие, можно использовать условное выражение.</span><span class="sxs-lookup"><span data-stu-id="83c9d-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="83c9d-110">Если выражение имеет **значение true** (– 1), Microsoft Access прекратит выполнение всех макросов.</span><span class="sxs-lookup"><span data-stu-id="83c9d-110">When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="83c9d-111">Например, у вас может быть макрос, отображающий окно сообщения в виде одного из нескольких сложных действий, в том числе выполнение других макросов.</span><span class="sxs-lookup"><span data-stu-id="83c9d-111">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros.</span></span> <span data-ttu-id="83c9d-112">Если пользователь нажимает кнопку **Cancel (Отмена** ) в этом окне сообщения, действие **Макрокоманда stopallmacros** может остановить все запущенные макросы.</span><span class="sxs-lookup"><span data-stu-id="83c9d-112">If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="83c9d-113">Если в макросе используются действия **echo** или **сетварнингс** для отключения эхо или отображения системных сообщений, действие **Макрокоманда stopallmacros** автоматически включает их снова.</span><span class="sxs-lookup"><span data-stu-id="83c9d-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="83c9d-114">Это действие недоступно в модуле Visual Basic для приложений (VBA).</span><span class="sxs-lookup"><span data-stu-id="83c9d-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

