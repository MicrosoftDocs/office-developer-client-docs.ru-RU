---
title: Установка примера надстройки с автономным состоянием
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Дата последнего изменения: 06 июля, 2012'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317215"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="73ee9-103">Установка примера надстройки с автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="73ee9-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="73ee9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73ee9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="73ee9-105">В этом разделе описано, как скачать и установить пример надстройки с автономным состоянием.</span><span class="sxs-lookup"><span data-stu-id="73ee9-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="73ee9-106">Надстройка "автономное состояние" — это надстройка COM, которая добавляет меню " **автономное состояние** " в Outlook и использует API автономного состояния.</span><span class="sxs-lookup"><span data-stu-id="73ee9-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="73ee9-107">В меню автономного состояния можно включить или отключить мониторинг состояния, проверить текущее состояние и изменить текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="73ee9-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="73ee9-108">Дополнительные сведения о внедрении надстройки "автономное состояние" приведены в разделе [Настройка надстройки с автономным состоянием](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="73ee9-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="73ee9-109">Установка примера надстройки с автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="73ee9-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="73ee9-110">Скачайте пример надстройки для автономного состояния: [Outlook 2007, примеры кода вспомогательного справочника и распространяемый установщик](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="73ee9-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="73ee9-111">Запустите Visual Studio 2005 от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="73ee9-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="73ee9-112">Если компьютер работает под управлением Windows XP, необходимо войти в систему с учетной записью администратора.</span><span class="sxs-lookup"><span data-stu-id="73ee9-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="73ee9-113">Если компьютер работает под управлением Windows Vista, необходимо войти в систему с учетной записью администратора.</span><span class="sxs-lookup"><span data-stu-id="73ee9-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="73ee9-114">Щелкните правой кнопкой мыши значок Visual Studio 2005 и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="73ee9-115">В Visual Studio 2005 откройте меню **файл**, выберите пункт **Открыть**, а затем выберите **проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="73ee9-116">Перейдите к папке, в которой был сохранен пример, нажмите кнопку **коннектионстатеаддин**, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="73ee9-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="73ee9-118">В диалоговом окне **сохранить файл как** нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="73ee9-119">В меню " **Пуск** " последовательно выберите пункты **все программы**, **стандартные**, щелкните правой кнопкой мыши **Командная строка**и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="73ee9-120">Если вы используете Windows XP, необходимо войти в систему с учетной записью администратора.</span><span class="sxs-lookup"><span data-stu-id="73ee9-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="73ee9-121">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="73ee9-122">В окне **командной строки** измените каталоги на папку Debug, в которой вы сохранили пример.</span><span class="sxs-lookup"><span data-stu-id="73ee9-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="73ee9-123">Например, если вы сохранили пример на странице C:\ диск, введите **CD "к:\коннектионстатеаддин\дебуг"** и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="73ee9-124">Введите **regsvr32 оффлинестатеаддин. dll** и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="73ee9-125">Для удаления примера надстройки с автономным состоянием введите **regsvr32 – u оффлинестатеаддин. dll**</span><span class="sxs-lookup"><span data-stu-id="73ee9-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="73ee9-126">В диалоговом окне **RegSrv32** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="73ee9-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="73ee9-127">Перезапустите Outlook, чтобы увидеть меню " **автономное состояние** ".</span><span class="sxs-lookup"><span data-stu-id="73ee9-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="73ee9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="73ee9-128">See also</span></span>



[<span data-ttu-id="73ee9-129">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="73ee9-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="73ee9-130">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="73ee9-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="73ee9-131">О примере надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="73ee9-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="73ee9-132">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="73ee9-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="73ee9-133">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="73ee9-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="73ee9-134">Отключение надстройки с автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="73ee9-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

