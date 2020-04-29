---
title: Макрокоманда Макрокоманда StopMacro (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Чтобы остановить выполняемый в данный момент макрос, можно использовать действие Макрокоманда StopMacro.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429497"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a><span data-ttu-id="1817f-103">Макрокоманда Макрокоманда StopMacro (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="1817f-103">StopMacro Macro Action (Access custom web app)</span></span>

<span data-ttu-id="1817f-104">Чтобы остановить выполняемый в данный момент макрос, можно использовать действие **Макрокоманда StopMacro** .</span><span class="sxs-lookup"><span data-stu-id="1817f-104">You can use the **StopMacro** action to stop the currently running macro.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1817f-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1817f-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="1817f-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="1817f-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="1817f-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="1817f-107">Setting</span></span>

<span data-ttu-id="1817f-108">Макрокоманда **Макрокоманда StopMacro** не содержит аргументов.</span><span class="sxs-lookup"><span data-stu-id="1817f-108">The **StopMacro** action doesn't have any arguments.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1817f-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="1817f-109">Remarks</span></span>

<span data-ttu-id="1817f-110">Обычно это действие используется при условии, что необходимо остановить макрос.</span><span class="sxs-lookup"><span data-stu-id="1817f-110">You typically use this action when a condition makes it necessary to stop the macro.</span></span> <span data-ttu-id="1817f-111">Например, вы можете создать макрос ПОЛЬЗОВАТЕЛЬСКОГО интерфейса, который открывает представление, в котором отображаются итоговые значения ежедневных заказов для даты, введенной в текущем представлении.</span><span class="sxs-lookup"><span data-stu-id="1817f-111">For example, you might create a user interface (UI) macro that opens a view showing the daily order totals for the date entered in the current view.</span></span> <span data-ttu-id="1817f-112">Можно использовать условное выражение, чтобы убедиться, что элемент управления "Дата заказа" в диалоговом окне содержит допустимую дату.</span><span class="sxs-lookup"><span data-stu-id="1817f-112">You could use a conditional expression to be sure that the Order Date control on the dialog box contains a valid date.</span></span> <span data-ttu-id="1817f-113">В противном случае действие **MessageBox** может отобразить сообщение об ошибке, а действие **Макрокоманда StopMacro** может остановить макрос пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1817f-113">If it doesn't, the **MessageBox** action can display an error message and the **StopMacro** action can stop the UI macro.</span></span> 
  

