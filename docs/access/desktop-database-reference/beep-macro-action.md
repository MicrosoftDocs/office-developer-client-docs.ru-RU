---
title: Макрос Beep (справочник по базе данных Access для настольных пк)
TOCTitle: Beep macro action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 96051d8389f4b8ba7005c75ccdb5e2780ba17138
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296866"
---
# <a name="beep-macro-action"></a><span data-ttu-id="dc5be-102">Макрокоманда Beep</span><span class="sxs-lookup"><span data-stu-id="dc5be-102">Beep macro action</span></span>


<span data-ttu-id="dc5be-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc5be-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc5be-104">Действие **Beep** можно использовать для звука звукового сигнала через динамик компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc5be-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="dc5be-105">Setting</span><span class="sxs-lookup"><span data-stu-id="dc5be-105">Setting</span></span>

<span data-ttu-id="dc5be-106">Действие **Beep** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="dc5be-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc5be-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="dc5be-107">Remarks</span></span>

<span data-ttu-id="dc5be-108">Вы можете использовать действие **Beep** для сигнала следующих вхождений:</span><span class="sxs-lookup"><span data-stu-id="dc5be-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="dc5be-109">Произошли важные изменения экрана.</span><span class="sxs-lookup"><span data-stu-id="dc5be-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="dc5be-110">Неправильный тип данных был введен в control.</span><span class="sxs-lookup"><span data-stu-id="dc5be-110">The wrong kind of data has been entered in a control.</span></span> <span data-ttu-id="dc5be-111">Например, пользователь ввели числовые данные в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="dc5be-111">For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="dc5be-112">Макрос достиг определенной точки или завершил свои действия.</span><span class="sxs-lookup"><span data-stu-id="dc5be-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="dc5be-113">Частота и длительность звукового сигнала зависят от оборудования, которое может отличаться в зависимости от компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc5be-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="dc5be-114">Чтобы запустить **действие Beep** в модуле Visual Basic для приложений (VBA), используйте метод **Beep** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="dc5be-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

