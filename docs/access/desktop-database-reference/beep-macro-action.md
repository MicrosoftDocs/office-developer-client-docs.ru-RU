---
title: Звуковые сигналы действия макроса (Справочник по для настольных баз данных Access)
TOCTitle: Beep Macro Action
ms:assetid: 5ca1600f-7934-3b3d-19fd-f305cda0e5d8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194572(v=office.15)
ms:contentKeyID: 48545092
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11853
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 284be6222d0b81e48a061afd1d87dd32c3985feb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867582"
---
# <a name="beep-macro-action"></a><span data-ttu-id="f7309-102">Звуковые сигналы действия макроса</span><span class="sxs-lookup"><span data-stu-id="f7309-102">Beep Macro Action</span></span>


<span data-ttu-id="f7309-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f7309-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f7309-104">Действие **Звуковые** можно использовать для получения сигнала звуковой сигнал через динамик компьютера.</span><span class="sxs-lookup"><span data-stu-id="f7309-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="f7309-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="f7309-105">Setting</span></span>

<span data-ttu-id="f7309-106">Действие **звуковые сигналы** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="f7309-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7309-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="f7309-107">Remarks</span></span>

<span data-ttu-id="f7309-108">Можно использовать действие **Beep** для сигнала в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="f7309-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="f7309-109">На экране изменений.</span><span class="sxs-lookup"><span data-stu-id="f7309-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="f7309-110">Неверный тип данных был введен в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="f7309-110">The wrong kind of data has been entered in a control.</span></span> <span data-ttu-id="f7309-111">Например пользователь ввел числовые данные в элемент управления текстового поля.</span><span class="sxs-lookup"><span data-stu-id="f7309-111">For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="f7309-112">Макрос достиг указанной точки или завершился.</span><span class="sxs-lookup"><span data-stu-id="f7309-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="f7309-113">Частота и продолжительность сигнала зависеть от оборудования, могут отличаться от указанных между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="f7309-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="f7309-114">Чтобы выполнить действие **звуковые сигналы** в Visual Basic для приложений (VBA) модуль, используйте метод **звуковые сигналы** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="f7309-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

