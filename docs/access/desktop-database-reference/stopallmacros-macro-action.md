---
title: StopAllMacros Macro Action
TOCTitle: StopAllMacros Macro Action
ms:assetid: 6afbf906-03b8-6e68-bbc9-7a4b141cf1c5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195440(v=office.15)
ms:contentKeyID: 48545442
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm104968
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 80da04f7b5f99fd0b249164caaeaca9f25edd172
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479839"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="60a3e-102">StopAllMacros Macro Action</span><span class="sxs-lookup"><span data-stu-id="60a3e-102">StopAllMacros Macro Action</span></span>


<span data-ttu-id="60a3e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="60a3e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="60a3e-104">Чтобы остановить все макросы, которые в настоящее время работает можно использовать действие **ОстановитьВсеМакросы** .</span><span class="sxs-lookup"><span data-stu-id="60a3e-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="60a3e-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="60a3e-105">Setting</span></span>

<span data-ttu-id="60a3e-106">Действие **ОстановитьВсеМакросы** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="60a3e-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="60a3e-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="60a3e-107">Remarks</span></span>

<span data-ttu-id="60a3e-108">Это действие обычно используется для остановки всех макросов при ошибки.</span><span class="sxs-lookup"><span data-stu-id="60a3e-108">You typically use this action when an error condition makes it necessary to stop all macros.</span></span> <span data-ttu-id="60a3e-109">В строке действие макрос, содержащий это действие можно использовать условного выражения.</span><span class="sxs-lookup"><span data-stu-id="60a3e-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="60a3e-110">Когда вычисление выражения дает значение **True** (– 1), Microsoft Access останавливает все макросы.</span><span class="sxs-lookup"><span data-stu-id="60a3e-110">When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="60a3e-111">Например возможно, макрос, который отображает окно сообщения как один из нескольких сложных действий, включая выполнение других макросов.</span><span class="sxs-lookup"><span data-stu-id="60a3e-111">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros.</span></span> <span data-ttu-id="60a3e-112">При нажатии кнопки **Отмена** сообщение, действие **ОстановитьВсеМакросы** можно остановить все макросы, на которых выполняется.</span><span class="sxs-lookup"><span data-stu-id="60a3e-112">If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="60a3e-113">Если макрос **эхо** или **УстановитьСообщения** действий эхо или вывод системных сообщений, действие **ОстановитьВсеМакросы** автоматически включает их обратно.</span><span class="sxs-lookup"><span data-stu-id="60a3e-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="60a3e-114">Это действие недоступно в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="60a3e-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

