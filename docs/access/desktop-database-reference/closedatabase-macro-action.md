---
title: Макрокоманда CloseDatabase
TOCTitle: CloseDatabase macro action
ms:assetid: c4b4278d-932c-99f6-da2d-8953109b44b3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823085(v=office.15)
ms:contentKeyID: 48547598
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ac29cbdae8c162a992f2763530514150ca0240ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296299"
---
# <a name="closedatabase-macro-action"></a><span data-ttu-id="3e2a0-102">Макрокоманда CloseDatabase</span><span class="sxs-lookup"><span data-stu-id="3e2a0-102">CloseDatabase macro action</span></span>


<span data-ttu-id="3e2a0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e2a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3e2a0-104">Для закрытия текущей базы данных можно использовать действие **CloseDatabase.**</span><span class="sxs-lookup"><span data-stu-id="3e2a0-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="3e2a0-105">Setting</span><span class="sxs-lookup"><span data-stu-id="3e2a0-105">Setting</span></span>

<span data-ttu-id="3e2a0-106">У **действия CloseDatabase** нет аргументов.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e2a0-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="3e2a0-107">Remarks</span></span>

  - <span data-ttu-id="3e2a0-108">Access не будет выполнять действия, которые следуют действию **CloseDatabase** в макросе.</span><span class="sxs-lookup"><span data-stu-id="3e2a0-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="3e2a0-109">Это действие имеет тот же  эффект, что и при нажатии на вкладку "Файл" и нажатии кнопки "Закрыть базу **данных".**</span><span class="sxs-lookup"><span data-stu-id="3e2a0-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="3e2a0-110">Если при запуске действия **CloseDatabase** открываются какие-либо несжатые объекты, отображаются те же диалоги, что и при нажатии кнопки "Закрыть базу **данных".**</span><span class="sxs-lookup"><span data-stu-id="3e2a0-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="3e2a0-111">Чтобы выполнить действие **CloseDatabase** в модуле Visual Basic для приложений (VBA), используйте метод **CloseDatabase** объекта **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="3e2a0-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

