---
title: Установка надстройки в автономном режиме
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Последнее изменение: 06 июля 2012 г.'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317215"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="907e8-103">Установка надстройки в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="907e8-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="907e8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="907e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="907e8-105">В этом разделе вы можете скачать и установить надстройку Sample Offline State.</span><span class="sxs-lookup"><span data-stu-id="907e8-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="907e8-106">Пример автономной надстройки состояния — это надстройка COM, которая добавляет меню автономного состояния в Outlook и использует API состояния автономного режима. </span><span class="sxs-lookup"><span data-stu-id="907e8-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="907e8-107">В меню автономного состояния можно включить или отключить мониторинг состояния, проверить текущее состояние и изменить текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="907e8-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="907e8-108">Дополнительные сведения о реализации надстройки автономного состояния см. в примере Настройка надстройки [автономного состояния.](setting-up-an-offline-state-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="907e8-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="907e8-109">Установка надстройки "Пример автономного состояния"</span><span class="sxs-lookup"><span data-stu-id="907e8-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="907e8-110">Скачайте пример надстройки автономного состояния здесь: Outlook [2007 вспомогательных](https://www.microsoft.com/en-us/download/details.aspx?id=24102)образцов справочного кода и перераспределяемого установщика .</span><span class="sxs-lookup"><span data-stu-id="907e8-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="907e8-111">Выполнить Visual Studio 2005 в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="907e8-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="907e8-112">Если компьютер работает Windows XP, необходимо войти в систему в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="907e8-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="907e8-113">Если компьютер работает Windows Vista, необходимо войти в систему в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="907e8-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="907e8-114">Щелкните правой кнопкой мыши значок 2005 Visual Studio нажмите **кнопку Выполнить в качестве администратора**.</span><span class="sxs-lookup"><span data-stu-id="907e8-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="907e8-115">В Visual Studio 2005 нажмите **кнопку Файл**, выберите **Открыть**, а затем **нажмите кнопку Project/ решение**.</span><span class="sxs-lookup"><span data-stu-id="907e8-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="907e8-116">Просмотрите расположение, в котором сохранен пример, щелкните **ConnectionStateAddin** и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="907e8-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="907e8-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="907e8-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="907e8-118">В **диалоговом окне Сохранить файл как** диалоговое окно нажмите **кнопку Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="907e8-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="907e8-119">Щелкните **меню Пуск,** нажмите кнопку **Все** программы, щелкните **Аксессуары,** щелкните правой кнопкой мыши **командное** подсказок, а затем нажмите **кнопку Запустить в качестве администратора**.</span><span class="sxs-lookup"><span data-stu-id="907e8-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="907e8-120">Если вы работаете Windows XP, необходимо войти в систему в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="907e8-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="907e8-121">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="907e8-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="907e8-122">В **окне Командная подсказка** измените каталоги в папку Debug, в которой сохранен пример.</span><span class="sxs-lookup"><span data-stu-id="907e8-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="907e8-123">Например, если вы сохранили образец на C:\ диск, вы введите **cd "C:\ConnectionStateAddin\Debug"** и нажмите **КНОПКУ ВВОДА**.</span><span class="sxs-lookup"><span data-stu-id="907e8-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="907e8-124">Введите **regsvr32 OfflineStateAddin.dll** и нажмите **КНОПКУ ВВОДА**.</span><span class="sxs-lookup"><span data-stu-id="907e8-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="907e8-125">Чтобы удалить пример надстройки автономного состояния, введите **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="907e8-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="907e8-126">В **диалоговом окне RegSrv32** нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="907e8-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="907e8-127">Перезапустите Outlook, чтобы увидеть меню **состояния автономного** режима.</span><span class="sxs-lookup"><span data-stu-id="907e8-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="907e8-128">См. также</span><span class="sxs-lookup"><span data-stu-id="907e8-128">See also</span></span>



[<span data-ttu-id="907e8-129">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="907e8-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="907e8-130">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="907e8-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="907e8-131">О примере надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="907e8-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="907e8-132">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="907e8-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="907e8-133">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="907e8-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="907e8-134">Отключение надстройки автономного состояния</span><span class="sxs-lookup"><span data-stu-id="907e8-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

