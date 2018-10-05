---
title: Установка примера надстройки, позволяющей управлять автономным состоянием
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: 'Последнее изменение: 06 июля 2012 г.'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389199"
---
# <a name="installing-the-sample-offline-state-add-in"></a><span data-ttu-id="de833-103">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="de833-103">Installing the Sample Offline State Add-in</span></span>

  
  
<span data-ttu-id="de833-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de833-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de833-105">В этом разделе описываются действия, чтобы загрузить и установить надстройку пример состояние не в сети.</span><span class="sxs-lookup"><span data-stu-id="de833-105">This topic takes you through the steps to download and install the Sample Offline State Add-in.</span></span> <span data-ttu-id="de833-106">Надстройки пример состояние не в сети — это надстройка COM, который добавляет меню **Состояния не в сети** в Outlook и использует автономный режим состояния API.</span><span class="sxs-lookup"><span data-stu-id="de833-106">The Sample Offline State Add-in is a COM add-in that adds an **Offline State** menu to Outlook and utilizes the Offline State API.</span></span> <span data-ttu-id="de833-107">Через меню состояния не в сети можно включать и отключать мониторинг состояния Проверьте текущее состояние и изменения текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="de833-107">Through the Offline State menu you can enable or disable state monitoring, check the current state, and change the current state.</span></span> <span data-ttu-id="de833-108">Дополнительные сведения о добавить состояние не в сети в реализации можно [параметр копирование автономно состояние надстройки](setting-up-an-offline-state-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="de833-108">For more information about how the Offline State Add-in is implemented, see [Setting Up an Offline State Add-in](setting-up-an-offline-state-add-in.md).</span></span>
  
## <a name="install-the-sample-offline-state-add-in"></a><span data-ttu-id="de833-109">Установка примера автономного состояния надстройки</span><span class="sxs-lookup"><span data-stu-id="de833-109">Install the Sample Offline State Add-in</span></span>

1. <span data-ttu-id="de833-110">Загрузить пример состояние не в сети надстройки здесь: [Outlook 2007 примеры Дополнительные справочные кода и распространяемого установщика](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="de833-110">Download the Sample Offline State Add-in here: [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="de833-111">Запустите Visual Studio 2005 с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="de833-111">Run Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="de833-112">Если компьютер работает под управлением Windows XP, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="de833-112">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="de833-113">Если компьютер работает под управлением ОС Windows Vista, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="de833-113">If your computer is running Windows Vista, you must be logged in as an Administrator.</span></span> <span data-ttu-id="de833-114">Щелкните правой кнопкой мыши значок Visual Studio 2005 и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="de833-114">Right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
3. <span data-ttu-id="de833-115">В Visual Studio 2005 откройте меню **файл**, выберите команду **Открыть**и щелкните **Проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="de833-115">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
4. <span data-ttu-id="de833-116">Перейдите к папке, в которой вы сохранили примера **ConnectionStateAddin**и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="de833-116">Browse to the location where you saved the sample, click **ConnectionStateAddin**, and then click **Open**.</span></span>
    
5. <span data-ttu-id="de833-117">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="de833-117">On the **Build** menu, click **Build Solution**.</span></span>
    
6. <span data-ttu-id="de833-118">В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="de833-118">In the **Save File As** dialog box, click **Save**.</span></span>
    
7. <span data-ttu-id="de833-119">Нажмите кнопку **Пуск** , последовательно выберите пункты **Все программы**, **Стандартные**, щелкните правой кнопкой мыши **Командная строка**и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="de833-119">Click the **Start** menu, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="de833-120">При запуске Windows XP, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="de833-120">If you are running Windows XP, you must be logged in as an Administrator.</span></span> 
  
8. <span data-ttu-id="de833-121">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="de833-121">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
9. <span data-ttu-id="de833-122">В окне **командной строки** перейдите в папку Отладка, которой вы сохранили примера.</span><span class="sxs-lookup"><span data-stu-id="de833-122">In the **Command Prompt** window, change directories to the Debug folder where you saved the sample.</span></span> <span data-ttu-id="de833-123">Например если примера сохранен на диск C:\, вы введите **cd «C:\ConnectionStateAddin\Debug»** и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="de833-123">For example, if you saved the sample on your C:\ drive, you would type **cd "C:\ConnectionStateAddin\Debug"** and then press **ENTER**.</span></span> 
    
10. <span data-ttu-id="de833-124">Введите **regsvr32 OfflineStateAddin.dll** и нажмите клавишу **Ввод**.</span><span class="sxs-lookup"><span data-stu-id="de833-124">Type **regsvr32 OfflineStateAddin.dll** and press **ENTER**.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="de833-125">Чтобы удалить надстройку пример состояние не в сети, введите **regsvr32 -u OfflineStateAddin.dll**</span><span class="sxs-lookup"><span data-stu-id="de833-125">To uninstall the Sample Offline State Add-in, type **regsvr32 -u OfflineStateAddin.dll**</span></span>
  
11. <span data-ttu-id="de833-126">В диалоговом окне **RegSrv32** нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="de833-126">In the **RegSrv32** dialog box, click **OK**.</span></span>
    
12. <span data-ttu-id="de833-127">Перезапустите Outlook, чтобы просмотреть меню **Состояния не в сети** .</span><span class="sxs-lookup"><span data-stu-id="de833-127">Restart Outlook to see the **Offline State** menu.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="de833-128">См. также</span><span class="sxs-lookup"><span data-stu-id="de833-128">See also</span></span>



[<span data-ttu-id="de833-129">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="de833-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="de833-130">Установка примера надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="de833-130">Installing the Sample Offline State Add-in</span></span>](installing-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="de833-131">Сведения о примере надстройки с автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="de833-131">About the Sample Offline State Add-in</span></span>](about-the-sample-offline-state-add-in.md)
  
[<span data-ttu-id="de833-132">Конфигурация надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="de833-132">Setting Up an Offline State Add-in</span></span>](setting-up-an-offline-state-add-in.md)
  
[<span data-ttu-id="de833-133">Отслеживание изменений состояния подключения с помощью надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="de833-133">Monitoring Connection State Changes Using an Offline State Add-in</span></span>](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[<span data-ttu-id="de833-134">Отсоединение надстройки, позволяющей управлять автономным состоянием</span><span class="sxs-lookup"><span data-stu-id="de833-134">Disconnecting an Offline State Add-in</span></span>](disconnecting-an-offline-state-add-in.md)

