---
title: Установка поставщика пакетных пакетов PST
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309634"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="e8a35-103">Установка поставщика пакетных пакетов PST</span><span class="sxs-lookup"><span data-stu-id="e8a35-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="e8a35-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8a35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8a35-105">В этом разделе вы сможете скачать и установить поставщика магазина PST Sample Wrapped.</span><span class="sxs-lookup"><span data-stu-id="e8a35-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="e8a35-106">Поставщик магазина упаковки образца PST WrapPST реализует поставщика магазинов PST, который предназначен для использования в сочетании с API репликации.</span><span class="sxs-lookup"><span data-stu-id="e8a35-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="e8a35-107">Дополнительные сведения об API репликации см. в [иллюстрации API репликации.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="e8a35-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="e8a35-108">Установка поставщика магазина PST с завернутой выборочной упаковкой</span><span class="sxs-lookup"><span data-stu-id="e8a35-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="e8a35-109">Чтобы скачать пример поставщика пакетов PST Store, см. в Outlook [2007](https://www.microsoft.com/en-us/download/details.aspx?id=24102)примеры вспомогательного справочного кода и перераспределяемого установщика.</span><span class="sxs-lookup"><span data-stu-id="e8a35-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="e8a35-110">Откройте **папку SampleWrappedPSTStoreProvider** и нажмите кнопку **Извлечение всех файлов.**</span><span class="sxs-lookup"><span data-stu-id="e8a35-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="e8a35-111">Щелкните **Обзор,** выберите расположение, в котором необходимо сохранить образец, и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="e8a35-112">Нажмите кнопку **Извлечь**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-112">Click **Extract**.</span></span> <span data-ttu-id="e8a35-113">Выбранная папка отображается и содержит извлеченные файлы.</span><span class="sxs-lookup"><span data-stu-id="e8a35-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="e8a35-114">Откройте Visual Studio 2005 в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="e8a35-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="e8a35-115">Если компьютер работает Windows XP, необходимо войти в систему в качестве администратора.</span><span class="sxs-lookup"><span data-stu-id="e8a35-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="e8a35-116">Если компьютер работает Windows Vista, необходимо войти в систему в качестве администратора, а затем щелкнуть правой кнопкой мыши значок Visual Studio 2005 года и нажмите кнопку Выполнить в качестве **администратора**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="e8a35-117">В Visual Studio 2005 нажмите **кнопку Файл**, выберите **Открыть**, а затем **нажмите кнопку Project/ решение**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="e8a35-118">Просмотрите расположение, в котором сохранен пример, щелкните **WrapPST** и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="e8a35-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="e8a35-120">В **диалоговом окне Сохранить файл как** диалоговое окно нажмите **кнопку Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="e8a35-121">В папке, в которой сохранен пример,  щелкните правой кнопкой мыши файлInstall.batи нажмите **кнопку Выполнить в качестве администратора**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="e8a35-122">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="e8a35-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8a35-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e8a35-123">See also</span></span>



[<span data-ttu-id="e8a35-124">О поставщике пакетных пакетов PST Store</span><span class="sxs-lookup"><span data-stu-id="e8a35-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="e8a35-125">Инициализация поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="e8a35-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="e8a35-126">Ведение журнала в поставщике упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="e8a35-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="e8a35-127">Использование поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="e8a35-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="e8a35-128">Отключение поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="e8a35-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

