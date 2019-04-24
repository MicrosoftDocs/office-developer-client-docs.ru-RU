---
title: Макрокоманда MessageBox (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: bdacdafc-728b-4952-b28a-b5c1fe4b4f63
description: С помощью макрокоманды MessageBox можно отобразить окно сообщения с предупреждением или информационным сообщением. Например, вы можете использовать действие MessageBox с макросами проверки. Когда элемент управления или запись не проходит условие проверки в макросе, в окне сообщения отображается сообщение об ошибке и предоставляются инструкции о типе вводимых данных.
ms.openlocfilehash: 9f45101fd269ef863e60fd8e69741e5cd7c56ef1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301717"
---
# <a name="messagebox-macro-action-access-custom-web-app"></a><span data-ttu-id="61616-105">Макрокоманда MessageBox (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="61616-105">MessageBox Macro Action (Access custom web app)</span></span>

<span data-ttu-id="61616-106">С помощью макрокоманды **MessageBox** можно отобразить окно сообщения с предупреждением или информационным сообщением.</span><span class="sxs-lookup"><span data-stu-id="61616-106">You can use the **MessageBox** action to display a message box containing a warning or an informational message.</span></span> <span data-ttu-id="61616-107">Например, вы можете использовать действие **MessageBox** с макросами проверки.</span><span class="sxs-lookup"><span data-stu-id="61616-107">For example, you can use the **MessageBox** action with validation macros.</span></span> <span data-ttu-id="61616-108">Когда элемент управления или запись не проходит условие проверки в макросе, в окне сообщения отображается сообщение об ошибке и предоставляются инструкции о типе вводимых данных.</span><span class="sxs-lookup"><span data-stu-id="61616-108">When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="61616-109">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="61616-109">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="61616-110">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="61616-110">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="61616-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="61616-111">Setting</span></span>

<span data-ttu-id="61616-112">Действие **MessageBox** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="61616-112">The **MessageBox** action has the following argument.</span></span> 
  
|<span data-ttu-id="61616-113">**Аргумент макрокоманды**</span><span class="sxs-lookup"><span data-stu-id="61616-113">**Action argument**</span></span>|<span data-ttu-id="61616-114">**Описание**</span><span class="sxs-lookup"><span data-stu-id="61616-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="61616-115">Сообщение</span><span class="sxs-lookup"><span data-stu-id="61616-115">Message</span></span>  <br/> |<span data-ttu-id="61616-116">Текст в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="61616-116">The text in the message box.</span></span> <span data-ttu-id="61616-117">Можно ввести до 255 символов или ввести выражение (перед ним должен стоять знак равенства).</span><span class="sxs-lookup"><span data-stu-id="61616-117">You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span>  <br/> |
   

