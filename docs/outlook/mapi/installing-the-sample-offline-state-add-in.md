---
title: Установка примера надстройки автономного состояния
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Last modified: July 06, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317215"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="09910-103">Установка примера надстройки автономного состояния</span><span class="sxs-lookup"><span data-stu-id="09910-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="09910-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09910-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09910-105">В этом разделе вы можете скачать и установить пример надстройки автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="09910-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="09910-106">Пример надстройки автономного состояния — это надстройка COM, которая добавляет в Outlook меню автономного состояния и использует API автономного состояния. </span><span class="sxs-lookup"><span data-stu-id="09910-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="09910-107">С помощью меню "Автономное состояние" можно включить или отключить мониторинг состояния, проверить текущее состояние и изменить текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="09910-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="09910-108">Дополнительные сведения о реализации надстройки автономного состояния см. в подстройки "Настройка надстройки [автономного состояния".](setting-up-an-offline-state-add-in.md)</span><span class="sxs-lookup"><span data-stu-id="09910-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="09910-109">Установка примера надстройки автономного состояния</span><span class="sxs-lookup"><span data-stu-id="09910-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="09910-110">Скачайте пример надстройки автономного состояния здесь: примеры вспомогательного справочного кода [Outlook 2007 и распространяемый установщик.](https://www.microsoft.com/en-us/download/details.aspx?id=24102)</span><span class="sxs-lookup"><span data-stu-id="09910-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="09910-111">Запустите Visual Studio 2005 от администратора.</span><span class="sxs-lookup"><span data-stu-id="09910-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="09910-112">Если компьютер работает под управлением Windows XP, необходимо войти в систему с учетной записи администратора.</span><span class="sxs-lookup"><span data-stu-id="09910-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="09910-113">Если компьютер работает под управлением Windows Vista, необходимо войти в систему с учетной записи администратора.</span><span class="sxs-lookup"><span data-stu-id="09910-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="09910-114">Щелкните правой кнопкой мыши значок Visual Studio 2005 и выберите "Запуск **от прав администратора".**</span><span class="sxs-lookup"><span data-stu-id="09910-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="09910-115">В Visual Studio 2005 выберите "Файл", "Открыть" и **"Проект/решение".**  </span><span class="sxs-lookup"><span data-stu-id="09910-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="09910-116">Перейдите в расположение, в котором сохранен пример, щелкните **ConnectionStateAddin** и нажмите кнопку **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="09910-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="09910-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="09910-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="09910-118">В **диалоговом окне** "Сохранить файл как" нажмите кнопку **"Сохранить".**</span><span class="sxs-lookup"><span data-stu-id="09910-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="09910-119">Щелкните **меню "Пуск",** выберите пункт "Все **программы",** щелкните "Аксессуары", щелкните правой кнопкой мыши командную подсказку **и** выберите команду "Запуск от **прав администратора".** </span><span class="sxs-lookup"><span data-stu-id="09910-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="09910-120">Если вы работаете под управлением Windows XP, вы должны войти в систему с учетной записи администратора.</span><span class="sxs-lookup"><span data-stu-id="09910-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="09910-121">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="09910-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="09910-122">В **окне командной** подсказки измените каталоги на папку Debug, в которой сохранен пример.</span><span class="sxs-lookup"><span data-stu-id="09910-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="09910-123">Например, если вы сохранили пример на C:\ введите cd **"C:\ConnectionStateAddin\Debug"** и нажмите **ввод.**</span><span class="sxs-lookup"><span data-stu-id="09910-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="09910-124">Введите **regsvr32 OfflineStateAddin.dll** и **нажмите** ввод.</span><span class="sxs-lookup"><span data-stu-id="09910-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="09910-125">Чтобы удалить пример надстройки автономного состояния, введите **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="09910-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="09910-126">В **диалоговом окне RegSrv32** нажмите кнопку **ОК.**</span><span class="sxs-lookup"><span data-stu-id="09910-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="09910-127">Перезапустите Outlook, чтобы увидеть меню **автономного** состояния.</span><span class="sxs-lookup"><span data-stu-id="09910-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="09910-128">См. также</span><span class="sxs-lookup"><span data-stu-id="09910-128">See also</span></span>



[<span data-ttu-id="09910-129">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="09910-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="09910-130">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="09910-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="09910-131">О примере надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="09910-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="09910-132">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="09910-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="09910-133">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="09910-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="09910-134">Отключение надстройки автономного состояния</span><span class="sxs-lookup"><span data-stu-id="09910-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

