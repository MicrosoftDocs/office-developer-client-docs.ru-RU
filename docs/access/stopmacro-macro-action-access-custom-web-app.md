---
title: Действия макроса ОстановитьМакрос (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Можно использовать действие ОстановитьМакрос Остановка текущего выполняемого макроса.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807114"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="8a454-103">Действия макроса ОстановитьМакрос (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="8a454-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="8a454-104">Можно использовать действие **ОстановитьМакрос** Остановка текущего выполняемого макроса.</span><span class="sxs-lookup"><span data-stu-id="8a454-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="8a454-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="8a454-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="8a454-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="8a454-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="8a454-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="8a454-107">Setting</span></span>

<span data-ttu-id="8a454-108">Действие **ОстановитьМакрос** не требует аргументов.</span><span class="sxs-lookup"><span data-stu-id="8a454-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8a454-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="8a454-109">Remarks</span></span>

<span data-ttu-id="8a454-110">Это действие обычно используется для остановки макроса при выполнении определенного условия.</span><span class="sxs-lookup"><span data-stu-id="8a454-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="8a454-111">Например можно создать макрос пользовательского интерфейса пользователя, который открывает представление, отражающая ежедневного итоговых значений для даты, введенных в текущем представлении.</span><span class="sxs-lookup"><span data-stu-id="8a454-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="8a454-112">Чтобы убедиться, что к элементу управления Дата заказа на диалоговое окно содержит допустимая дата можно использовать условного выражения.</span><span class="sxs-lookup"><span data-stu-id="8a454-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="8a454-113">В противном случае действие **MessageBox** может отображаться сообщение об ошибке и завершить действие **ОстановитьМакрос** макрос пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="8a454-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

