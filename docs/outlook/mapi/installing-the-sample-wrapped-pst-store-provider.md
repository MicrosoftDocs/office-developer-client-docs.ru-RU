---
title: Установка примера оболочку поставщика хранилища PST-файлов
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '���� ���������� ���������: 5 ���� 2012 �.'
ms.openlocfilehash: 29aabc7a2e8513bf24bd3b56ff3e4a126e3d7437
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809450"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="1ff96-103">Установка примера оболочку поставщика хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="1ff96-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="1ff96-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ff96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ff96-105">В этом разделе описываются действия, чтобы загрузить и установить оболочку PST поставщик хранилища.</span><span class="sxs-lookup"><span data-stu-id="1ff96-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="1ff96-106">Пример оболочку PST хранения поставщик, WrapPST, реализует оболочку поставщика хранилища PST-файлов, который предназначен для использования совместно с использованием интерфейса API репликации.</span><span class="sxs-lookup"><span data-stu-id="1ff96-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="1ff96-107">Дополнительные сведения об API репликации можно [О репликации API](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="1ff96-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="1ff96-108">Установка примера поставщика хранилища оболочку PST-файлов</span><span class="sxs-lookup"><span data-stu-id="1ff96-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="1ff96-109">Чтобы загрузить оболочку PST поставщик хранилища, обратитесь к разделу [Outlook 2007 примеры Дополнительные справочные кода и распространяемого установщика](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="1ff96-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](http://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="1ff96-110">Откройте папку **SampleWrappedPSTStoreProvider** и выберите команду **Извлечь все файлы**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="1ff96-111">Нажмите кнопку **Обзор**, выберите расположение, где требуется сохранить образца и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="1ff96-112">Нажмите кнопку **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-112">Click **Extract**.</span></span> <span data-ttu-id="1ff96-113">Выбранная папка появляется и содержит извлеченные файлы.</span><span class="sxs-lookup"><span data-stu-id="1ff96-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="1ff96-114">Откройте Visual Studio 2005 с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="1ff96-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="1ff96-115">Если компьютер работает под управлением Windows XP, вы должны войти в систему с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="1ff96-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="1ff96-116">Если компьютер работает под управлением ОС Windows Vista, вы должны войти в систему как администратор и щелкните правой кнопкой мыши значок Visual Studio 2005 и щелкните **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="1ff96-117">В Visual Studio 2005 откройте меню **файл**, выберите команду **Открыть**и щелкните **Проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="1ff96-118">Перейдите к папке, в которой вы сохранили примера **WrapPST**и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="1ff96-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="1ff96-120">В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="1ff96-121">В папке, где был сохранен примера щелкните правой кнопкой мыши файл **Install.bat** и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="1ff96-122">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="1ff96-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ff96-123">См. также</span><span class="sxs-lookup"><span data-stu-id="1ff96-123">See also</span></span>



[<span data-ttu-id="1ff96-124">О примере оболочку поставщика хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="1ff96-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="1ff96-125">Инициализация поставщика оболочку хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="1ff96-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="1ff96-126">Выполнив вход поставщик оболочку хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="1ff96-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="1ff96-127">С помощью поставщика оболочку хранилища PST-файлов</span><span class="sxs-lookup"><span data-stu-id="1ff96-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="1ff96-128">Завершение работы поставщика оболочку хранения PST-файлов</span><span class="sxs-lookup"><span data-stu-id="1ff96-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

