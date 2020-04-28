---
title: Макрокоманда Beep (Справочник по базам данных Access на компьютере)
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
# <a name="beep-macro-action"></a><span data-ttu-id="a2951-102">Макрокоманда Beep</span><span class="sxs-lookup"><span data-stu-id="a2951-102">Beep macro action</span></span>


<span data-ttu-id="a2951-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a2951-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a2951-104">Вы можете использовать действие **Beep** для звукового сигнала в динамике компьютера.</span><span class="sxs-lookup"><span data-stu-id="a2951-104">You can use the **Beep** action to sound a beep tone through the computer's speaker.</span></span>

## <a name="setting"></a><span data-ttu-id="a2951-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="a2951-105">Setting</span></span>

<span data-ttu-id="a2951-106">В действии **Beep** нет аргументов.</span><span class="sxs-lookup"><span data-stu-id="a2951-106">The **Beep** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2951-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="a2951-107">Remarks</span></span>

<span data-ttu-id="a2951-108">Вы можете использовать действие **Beep** для сигнализации следующих вхождений:</span><span class="sxs-lookup"><span data-stu-id="a2951-108">You can use the **Beep** action to signal the following occurrences:</span></span>

  - <span data-ttu-id="a2951-109">Возникли важные изменения экрана.</span><span class="sxs-lookup"><span data-stu-id="a2951-109">Important screen changes have occurred.</span></span>

  - <span data-ttu-id="a2951-110">В элементе управления введен недопустимый тип данных.</span><span class="sxs-lookup"><span data-stu-id="a2951-110">The wrong kind of data has been entered in a control.</span></span> <span data-ttu-id="a2951-111">Например, пользователь ввел числовые данные в элемент управления "текстовое поле".</span><span class="sxs-lookup"><span data-stu-id="a2951-111">For example, the user has entered numeric data in a text box control.</span></span>

  - <span data-ttu-id="a2951-112">Макрос достиг определенной точки или выполнил действия.</span><span class="sxs-lookup"><span data-stu-id="a2951-112">A macro has reached a specified point or has completed its actions.</span></span>

<span data-ttu-id="a2951-113">Частота и продолжительность звукового сигнала зависят от аппаратного обеспечения, которое может различаться для разных компьютеров.</span><span class="sxs-lookup"><span data-stu-id="a2951-113">The frequency and duration of the beep depend on the hardware, which may vary between computers.</span></span>

<span data-ttu-id="a2951-114">Чтобы запустить действие **Beep** в модуле Visual Basic для приложений (VBA), используйте метод **BEEPER** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="a2951-114">To run the **Beep** action in a Visual Basic for Applications (VBA) module, use the **Beep** method of the **DoCmd** object.</span></span>

