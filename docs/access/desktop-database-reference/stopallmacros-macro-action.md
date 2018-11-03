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
ms.openlocfilehash: 34dbfc3504744dd446a018e797ebacfb79066d96
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923353"
---
# <a name="stopallmacros-macro-action"></a><span data-ttu-id="0c4da-102">Макрокоманда StopAllMacros</span><span class="sxs-lookup"><span data-stu-id="0c4da-102">StopAllMacros macro action</span></span>


<span data-ttu-id="0c4da-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c4da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0c4da-104">Чтобы остановить все макросы, которые в настоящее время работает можно использовать действие **ОстановитьВсеМакросы** .</span><span class="sxs-lookup"><span data-stu-id="0c4da-104">You can use the **StopAllMacros** action to stop all macros that are currently running.</span></span>

## <a name="setting"></a><span data-ttu-id="0c4da-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="0c4da-105">Setting</span></span>

<span data-ttu-id="0c4da-106">Действие **ОстановитьВсеМакросы** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="0c4da-106">The **StopAllMacros** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c4da-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c4da-107">Remarks</span></span>

<span data-ttu-id="0c4da-108">Это действие обычно используется для остановки всех макросов при ошибки.</span><span class="sxs-lookup"><span data-stu-id="0c4da-108">You typically use this action when an error condition makes it necessary to stop all macros.</span></span> <span data-ttu-id="0c4da-109">В строке действие макрос, содержащий это действие можно использовать условного выражения.</span><span class="sxs-lookup"><span data-stu-id="0c4da-109">You can use a conditional expression in the macro's action row that contains this action.</span></span> <span data-ttu-id="0c4da-110">Когда вычисление выражения дает значение **True** (– 1), Microsoft Access останавливает все макросы.</span><span class="sxs-lookup"><span data-stu-id="0c4da-110">When the expression evaluates to **True** (–1), Microsoft Access stops all macros.</span></span>

<span data-ttu-id="0c4da-111">Например возможно, макрос, который отображает окно сообщения как один из нескольких сложных действий, включая выполнение других макросов.</span><span class="sxs-lookup"><span data-stu-id="0c4da-111">For example, you might have a macro that displays a message box as one of a number of complex actions, including running other macros.</span></span> <span data-ttu-id="0c4da-112">При нажатии кнопки **Отмена** сообщение, действие **ОстановитьВсеМакросы** можно остановить все макросы, на которых выполняется.</span><span class="sxs-lookup"><span data-stu-id="0c4da-112">If the user clicks **Cancel** in this message box, the **StopAllMacros** action can stop all the macros that are running.</span></span>

<span data-ttu-id="0c4da-113">Если макрос **эхо** или **УстановитьСообщения** действий эхо или вывод системных сообщений, действие **ОстановитьВсеМакросы** автоматически включает их обратно.</span><span class="sxs-lookup"><span data-stu-id="0c4da-113">If a macro has used the **Echo** or **SetWarnings** actions to turn echo or the display of system messages off, the **StopAllMacros** action automatically turns them back on.</span></span>

<span data-ttu-id="0c4da-114">Это действие недоступно в Visual Basic для приложений (VBA) модуля.</span><span class="sxs-lookup"><span data-stu-id="0c4da-114">This action isn't available in a Visual Basic for Applications (VBA) module.</span></span>

