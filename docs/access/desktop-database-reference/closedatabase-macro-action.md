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
# <a name="closedatabase-macro-action"></a><span data-ttu-id="74769-102">Макрокоманда CloseDatabase</span><span class="sxs-lookup"><span data-stu-id="74769-102">CloseDatabase macro action</span></span>


<span data-ttu-id="74769-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74769-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74769-104">Для закрытия текущей базы данных можно использовать действие **клоседатабасе** .</span><span class="sxs-lookup"><span data-stu-id="74769-104">You can use the **CloseDatabase** action to close the current database.</span></span>

## <a name="setting"></a><span data-ttu-id="74769-105">Параметр</span><span class="sxs-lookup"><span data-stu-id="74769-105">Setting</span></span>

<span data-ttu-id="74769-106">Действие **клоседатабасе** не имеет аргументов.</span><span class="sxs-lookup"><span data-stu-id="74769-106">The **CloseDatabase** action does not have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="74769-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="74769-107">Remarks</span></span>

  - <span data-ttu-id="74769-108">Access не будет выполнять никакие действия, которые следуют за действием **клоседатабасе** в макросе.</span><span class="sxs-lookup"><span data-stu-id="74769-108">Access will not run any actions that follow the **CloseDatabase** action in a macro.</span></span>

  - <span data-ttu-id="74769-109">Это действие эквивалентно нажатию вкладки **файл** и нажатию кнопки **Закрыть базу данных**.</span><span class="sxs-lookup"><span data-stu-id="74769-109">This action has the same effect as clicking the **File** tab and then clicking **Close Database**.</span></span> <span data-ttu-id="74769-110">Если при выполнении действия **клоседатабасе** открыты несохраненные объекты, отображаются диалоговые окна, которые отображаются при нажатии кнопки **Закрыть базу данных**.</span><span class="sxs-lookup"><span data-stu-id="74769-110">If there are any unsaved objects open when you run the **CloseDatabase** action, the dialog boxes that appear are the same as those displayed when you click **Close Database**.</span></span>

  - <span data-ttu-id="74769-111">Чтобы запустить действие **клоседатабасе** в модуле Visual Basic для приложений (VBA), используйте метод **клоседатабасе** объекта **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="74769-111">To run the **CloseDatabase** action in a Visual Basic for Applications (VBA) module, use the **CloseDatabase** method of the **DoCmd** object.</span></span>

