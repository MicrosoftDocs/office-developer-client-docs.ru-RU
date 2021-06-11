---
title: Пример поставщика магазина сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436869"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="5bc1b-103">Пример поставщика магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="5bc1b-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="5bc1b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bc1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bc1b-105">Поставщик личных папок (PST) в качестве заднего конца для хранения данных использует поставщика файлов персональных папок ( PST).</span><span class="sxs-lookup"><span data-stu-id="5bc1b-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="5bc1b-106">Поставщик магазина PST, завернутый в пакет, должен использоваться вместе с API репликации.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="5bc1b-107">API репликации позволяет реплицировать элементы из заднего хранилища данных в хранилище Outlook PST.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="5bc1b-108">API репликации используется для репликации данных в специальный хранилище PST и отслеживания состояния синхронизации.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="5bc1b-109">Дополнительные сведения см. [в aPI репликации.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="5bc1b-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="5bc1b-110">Большинство функций в поставщике магазина PST с пакетом образца передают свои аргументы непосредственно основному поставщику PST.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="5bc1b-111">Некоторые функции требуют особой реализации и описаны в следующих темах.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5bc1b-112">Исполняемый:</span><span class="sxs-lookup"><span data-stu-id="5bc1b-112">Executable:</span></span>  <br/> |<span data-ttu-id="5bc1b-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="5bc1b-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="5bc1b-114">Каталог исходных кодов:</span><span class="sxs-lookup"><span data-stu-id="5bc1b-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="5bc1b-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="5bc1b-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="5bc1b-116">Язык:</span><span class="sxs-lookup"><span data-stu-id="5bc1b-116">Language:</span></span>  <br/> |<span data-ttu-id="5bc1b-117">C++</span><span class="sxs-lookup"><span data-stu-id="5bc1b-117">C++</span></span>  <br/> |
|<span data-ttu-id="5bc1b-118">Платформы:</span><span class="sxs-lookup"><span data-stu-id="5bc1b-118">Platforms:</span></span>  <br/> |<span data-ttu-id="5bc1b-119">Microsoft Visual Studio 2008 для Windows Vista, Windows Server 2008, Windows XP SP2 и Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="5bc1b-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="5bc1b-120">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="5bc1b-120">Supported Features</span></span>

<span data-ttu-id="5bc1b-121">Этот пример поддерживает Microsoft Outlook 2010, русская версия 64-битный и в настоящее время пересмотрен для Outlook 2013 г.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="5bc1b-122">Дополнительные сведения см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="5bc1b-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="5bc1b-123">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="5bc1b-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="5bc1b-124">Инициализация поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="5bc1b-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="5bc1b-125">Ведение журнала в поставщике упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="5bc1b-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="5bc1b-126">Использование поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="5bc1b-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="5bc1b-127">Отключение поставщика упакованных магазинов PST</span><span class="sxs-lookup"><span data-stu-id="5bc1b-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="5bc1b-128">**Установка поставщика магазинов PST Sample Wrapped**</span><span class="sxs-lookup"><span data-stu-id="5bc1b-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="5bc1b-129">Чтобы скачать поставщик пакетов PST sample, см. в примере Загрузка Outlook [MAPI Samples](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="5bc1b-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="5bc1b-130">Найдите папку, в которой сохранены Outlook MAPI Samples.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="5bc1b-131">Щелкните правой кнопкой **мыши папку OutlookMAPISamples-version \< \> number** zip и нажмите кнопку **Извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="5bc1b-132">Щелкните **Обзор,** выберите расположение, в котором необходимо сохранить образец, а затем нажмите кнопку **Извлечение**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="5bc1b-133">Запуск Microsoft Visual Studio 2008 г.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="5bc1b-134">В Microsoft Visual Studio 2008 нажмите **кнопку Файл**, выберите **Открыть**, а затем **нажмите кнопку Project/Решение**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="5bc1b-135">Просмотрите расположение, в котором сохранен пример, щелкните **WrapPST.vcproj** и нажмите **кнопку Открыть**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="5bc1b-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="5bc1b-137">В **диалоговом окне Сохранить файл как** диалоговое окно нажмите **кнопку Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="5bc1b-138">В папке, в которой сохранен пример,  щелкните правой кнопкой мыши файлinstall.batи нажмите **кнопку Выполнить в качестве администратора**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="5bc1b-139">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="5bc1b-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

