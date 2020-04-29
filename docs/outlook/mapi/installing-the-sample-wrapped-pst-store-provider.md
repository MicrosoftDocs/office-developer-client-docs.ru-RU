---
title: Установка примера поставщика упакованного PST-хранилища
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
# <a name="installing-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="12a4e-103">Установка примера поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="12a4e-103">Installing the Sample Wrapped PST Store Provider</span></span>

  
  
<span data-ttu-id="12a4e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12a4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12a4e-105">В этом разделе описано, как скачать и установить пример поставщика упакованного PST-хранилища с упакованным PST-данным.</span><span class="sxs-lookup"><span data-stu-id="12a4e-105">This topic takes you through the steps to download and install the Sample Wrapped PST Store Provider.</span></span> <span data-ttu-id="12a4e-106">В примере поставщика упакованного PST-хранилища Враппст реализуется поставщик упакованного PST-хранилища, предназначенный для использования вместе с API репликации.</span><span class="sxs-lookup"><span data-stu-id="12a4e-106">The Sample Wrapped PST Store Provider, WrapPST, implements a wrapped PST store provider that is intended to be used in conjunction with the Replication API.</span></span> <span data-ttu-id="12a4e-107">Более подробную информацию об API репликации можно узнать [в статье о API репликации](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="12a4e-107">For more information about the Replication API, see [About the Replication API](about-the-replication-api.md).</span></span>
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a><span data-ttu-id="12a4e-108">Установка примера поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="12a4e-108">Install the Sample Wrapped PST Store Provider</span></span>

1. <span data-ttu-id="12a4e-109">Загрузить поставщик примера упакованного PST-хранилища можно в статье [примеры кода вспомогательного справочника Outlook 2007 и распространяемый установщик](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span><span class="sxs-lookup"><span data-stu-id="12a4e-109">To download the Sample Wrapped PST Store Provider, see [Outlook 2007 Auxiliary Reference Code Samples and Redistributable Installer](https://www.microsoft.com/en-us/download/details.aspx?id=24102).</span></span>
    
2. <span data-ttu-id="12a4e-110">Откройте папку **самплевраппедпстсторепровидер** и выберите пункт **извлечь все файлы**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-110">Open the **SampleWrappedPSTStoreProvider** folder and click **Extract All Files**.</span></span>
    
3. <span data-ttu-id="12a4e-111">Нажмите кнопку **Обзор**, выберите расположение, в котором нужно сохранить пример, и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-111">Click **Browse**, select the location where you want to save the sample, and click **OK**.</span></span>
    
4. <span data-ttu-id="12a4e-112">Нажмите кнопку **Извлечь**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-112">Click **Extract**.</span></span> <span data-ttu-id="12a4e-113">Откроется выбранная папка, содержащая извлеченные файлы.</span><span class="sxs-lookup"><span data-stu-id="12a4e-113">The folder you selected appears and contains the extracted files.</span></span>
    
5. <span data-ttu-id="12a4e-114">Откройте Visual Studio 2005 от имени администратора.</span><span class="sxs-lookup"><span data-stu-id="12a4e-114">Open Visual Studio 2005 as an administrator.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="12a4e-115">Если компьютер работает под управлением Windows XP, необходимо войти в систему с учетной записью администратора.</span><span class="sxs-lookup"><span data-stu-id="12a4e-115">If your computer is running Windows XP, you must be logged in as an Administrator.</span></span> <span data-ttu-id="12a4e-116">Если компьютер работает под управлением Windows Vista, необходимо войти в систему с учетной записью администратора и щелкнуть правой кнопкой мыши значок Visual Studio 2005 и выбрать пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-116">If your computer is running Windows Vista, you must be logged in as an Administrator and you must right-click the Visual Studio 2005 icon and click **Run as administrator**.</span></span> 
  
6. <span data-ttu-id="12a4e-117">В Visual Studio 2005 откройте меню **файл**, выберите пункт **Открыть**, а затем выберите **проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-117">In Visual Studio 2005, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
7. <span data-ttu-id="12a4e-118">Перейдите к папке, в которой был сохранен пример, нажмите кнопку **враппст**, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-118">Browse to the location where you saved the sample, click **WrapPST**, and then click **Open**.</span></span>
    
8. <span data-ttu-id="12a4e-119">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-119">On the **Build** menu, click **Build Solution**.</span></span>
    
9. <span data-ttu-id="12a4e-120">В диалоговом окне **сохранить файл как** нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-120">In the **Save File As** dialog box, click **Save**.</span></span>
    
10. <span data-ttu-id="12a4e-121">В папке, в которой сохранен пример, щелкните файл **install. bat** правой кнопкой мыши и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-121">In the folder where you saved the sample, right-click the **Install.bat** file and click **Run as administrator**.</span></span>
    
11. <span data-ttu-id="12a4e-122">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="12a4e-122">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12a4e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="12a4e-123">See also</span></span>



[<span data-ttu-id="12a4e-124">О примере поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="12a4e-124">About the Sample Wrapped PST Store Provider</span></span>](about-the-sample-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="12a4e-125">Инициализация поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="12a4e-125">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="12a4e-126">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="12a4e-126">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="12a4e-127">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="12a4e-127">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
  
[<span data-ttu-id="12a4e-128">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="12a4e-128">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)

