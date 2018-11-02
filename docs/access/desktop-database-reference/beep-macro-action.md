---
title: Звуковые сигналы действия макроса (Справочник по для настольных баз данных Access)
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
ms.openlocfilehash: d8ceb39071335b1600f4e371a357126306fbcf2a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922239"
---
# <a name="beep-macro-action"></a><span data-ttu-id="2709b-102">Макрокоманда Beep</span><span class="sxs-lookup"><span data-stu-id="2709b-102">Beep macro action</span></span>


<span data-ttu-id="2709b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2709b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2709b-104">Действие **Звуковые** можно использовать для получения сигнала звуковой сигнал через динамик компьютера.</span><span class="sxs-lookup"><span data-stu-id="2709b-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="2709b-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="2709b-105">Setting</span></span>

<span data-ttu-id="2709b-106">Действие **звуковые сигналы** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="2709b-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="2709b-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="2709b-107">Remarks</span></span>

<span data-ttu-id="2709b-108">Можно использовать действие **Beep** для сигнала в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="2709b-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="2709b-109">На экране изменений.</span><span class="sxs-lookup"><span data-stu-id="2709b-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="2709b-110">Неверный тип данных был введен в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="2709b-110">The wrong kind of data has been entered in a control.</span></span> <span data-ttu-id="2709b-111">Например пользователь ввел числовые данные в элемент управления текстового поля.</span><span class="sxs-lookup"><span data-stu-id="2709b-111">For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="2709b-112">Макрос достиг указанной точки или завершился.</span><span class="sxs-lookup"><span data-stu-id="2709b-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="2709b-113">Частота и продолжительность сигнала зависеть от оборудования, могут отличаться от указанных между компьютерами.</span><span class="sxs-lookup"><span data-stu-id="2709b-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="2709b-114">Чтобы выполнить действие **звуковые сигналы** в Visual Basic для приложений (VBA) модуль, используйте метод **звуковые сигналы** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="2709b-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

