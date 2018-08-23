---
title: Установка примера надстройки, позволяющей управлять автономным состоянием
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Последнее изменение: 06 июля 2012 г.'
ms.openlocfilehash: 7616c3a6077b9354cda7046c0949e7c5553f6551
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586839"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="dc995-103">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="dc995-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="dc995-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc995-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc995-105">В этом разделе описываются действия, чтобы загрузить и установить надстройку пример состояние не в сети.</span><span class="sxs-lookup"><span data-stu-id="dc995-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="dc995-106">Надстройки пример состояние не в сети — это надстройка COM, который добавляет меню **Состояния не в сети** в Outlook и использует автономный режим состояния API.</span><span class="sxs-lookup"><span data-stu-id="dc995-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="dc995-107">Через меню состояния не в сети можно включать и отключать мониторинг состояния Проверьте текущее состояние и изменения текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="dc995-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="dc995-108">Дополнительные сведения о добавить состояние не в сети в реализации можно [параметр копирование автономно состояние надстройки](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="dc995-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="dc995-109">Установка примера автономного состояния надстройки</span><span class="sxs-lookup"><span data-stu-id="dc995-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="dc995-110">Загрузить пример состояние не в сети надстройки здесь: [Outlook 2007 примеры Дополнительные справочные кода и распространяемого установщика](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="dc995-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="dc995-111">Запустите Visual Studio 2005 с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="dc995-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="dc995-112">Если компьютер работает под управлением Windows XP, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="dc995-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="dc995-113">Если компьютер работает под управлением ОС Windows Vista, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="dc995-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="dc995-114">Щелкните правой кнопкой мыши значок Visual Studio 2005 и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="dc995-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="dc995-115">В Visual Studio 2005 откройте меню **файл**, выберите команду **Открыть**и щелкните **Проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="dc995-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="dc995-116">Перейдите к папке, в которой вы сохранили примера **ConnectionStateAddin**и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="dc995-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="dc995-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="dc995-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="dc995-118">В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="dc995-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="dc995-119">Нажмите кнопку **Пуск** , последовательно выберите пункты **Все программы**, **Стандартные**, щелкните правой кнопкой мыши **Командная строка**и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="dc995-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="dc995-120">При запуске Windows XP, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="dc995-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="dc995-121">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="dc995-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="dc995-122">В окне **командной строки** перейдите в папку Отладка, которой вы сохранили примера.</span><span class="sxs-lookup"><span data-stu-id="dc995-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="dc995-123">Например если примера сохранен на диск C:\, вы введите **cd «C:\ConnectionStateAddin\Debug»** и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="dc995-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="dc995-124">Введите **regsvr32 OfflineStateAddin.dll** и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="dc995-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="dc995-125">Чтобы удалить надстройку пример состояние не в сети, введите **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="dc995-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="dc995-126">В диалоговом окне **RegSrv32** нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="dc995-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="dc995-127">Перезапустите Outlook, чтобы просмотреть меню **Состояния не в сети** .</span><span class="sxs-lookup"><span data-stu-id="dc995-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dc995-128">См. также</span><span class="sxs-lookup"><span data-stu-id="dc995-128">See also</span></span>



[<span data-ttu-id="dc995-129">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="dc995-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="dc995-130">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="dc995-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="dc995-131">Сведения о примере надстройки с автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="dc995-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="dc995-132">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="dc995-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="dc995-133">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="dc995-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="dc995-134">Отсоединение надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="dc995-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

