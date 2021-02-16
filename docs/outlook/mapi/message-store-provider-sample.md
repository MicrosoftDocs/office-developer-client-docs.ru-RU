---
title: Пример поставщика store сообщений
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
# <a name="message-store-provider-sample"></a><span data-ttu-id="b6a84-103">Пример поставщика store сообщений</span><span class="sxs-lookup"><span data-stu-id="b6a84-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="b6a84-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6a84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6a84-105">Образец поставщика упакованного PST-файла использует поставщика файлов личных папок (PST) в качестве тыловый части для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="b6a84-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="b6a84-106">Поставщик упакованного PST-хранения должен использоваться вместе с API репликации.</span><span class="sxs-lookup"><span data-stu-id="b6a84-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="b6a84-107">API репликации позволяет реплицировать элементы из тылового репозитория данных в PST-хранилище Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="b6a84-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="b6a84-108">API репликации используется для репликации данных в выделенное хранилище PST и отслеживания состояния синхронизации.</span><span class="sxs-lookup"><span data-stu-id="b6a84-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="b6a84-109">Дополнительные сведения [см. в сведениях об API репликации.](about-the-replication-api.md)</span><span class="sxs-lookup"><span data-stu-id="b6a84-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="b6a84-110">Большинство функций в примере поставщика упакованного PST-магазина передают свои аргументы непосредственно основному поставщику PST.</span><span class="sxs-lookup"><span data-stu-id="b6a84-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="b6a84-111">Некоторые функции требуют особой реализации и описаны в следующих темах.</span><span class="sxs-lookup"><span data-stu-id="b6a84-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6a84-112">Исполняемый исполня</span><span class="sxs-lookup"><span data-stu-id="b6a84-112">Executable:</span></span>  <br/> |<span data-ttu-id="b6a84-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="b6a84-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="b6a84-114">Каталог с исходным кодом:</span><span class="sxs-lookup"><span data-stu-id="b6a84-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="b6a84-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="b6a84-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="b6a84-116">Язык:</span><span class="sxs-lookup"><span data-stu-id="b6a84-116">Language:</span></span>  <br/> |<span data-ttu-id="b6a84-117">C++</span><span class="sxs-lookup"><span data-stu-id="b6a84-117">C++</span></span>  <br/> |
|<span data-ttu-id="b6a84-118">Платформы:</span><span class="sxs-lookup"><span data-stu-id="b6a84-118">Platforms:</span></span>  <br/> |<span data-ttu-id="b6a84-119">Microsoft Visual Studio 2008 для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="b6a84-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="b6a84-120">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="b6a84-120">Supported Features</span></span>

<span data-ttu-id="b6a84-121">Этот пример поддерживает Microsoft Outlook 2010, русская версия 64-битную и был изменен для Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="b6a84-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="b6a84-122">Дополнительные сведения см. в следующих темах:</span><span class="sxs-lookup"><span data-stu-id="b6a84-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="b6a84-123">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="b6a84-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="b6a84-124">Инициализация поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="b6a84-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="b6a84-125">Вход в систему для поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="b6a84-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="b6a84-126">Использование поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="b6a84-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="b6a84-127">Завершение работы поставщика упакованного PST-магазина</span><span class="sxs-lookup"><span data-stu-id="b6a84-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="b6a84-128">**Установка примера поставщика упакованного PST-магазина**</span><span class="sxs-lookup"><span data-stu-id="b6a84-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="b6a84-129">Чтобы скачать пример поставщика упакованных PST-данных, скачайте примеры [MAPI для Outlook.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="b6a84-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="b6a84-130">Найдите папку, в которой сохранены примеры MAPI для Outlook.</span><span class="sxs-lookup"><span data-stu-id="b6a84-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="b6a84-131">Щелкните правой кнопкой **мыши ZIP-папку OutlookMAPISamples версии \< \>** и выберите **"Извлечь все".**</span><span class="sxs-lookup"><span data-stu-id="b6a84-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="b6a84-132">Нажмите **кнопку**"Обзор", выберите расположение, в котором вы хотите сохранить пример, а затем нажмите кнопку **"Извлечь".**</span><span class="sxs-lookup"><span data-stu-id="b6a84-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="b6a84-133">Запустите Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b6a84-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="b6a84-134">В Microsoft Visual Studio 2008 нажмите **кнопку "Файл",** выберите **"Открыть"** и выберите **"Проект/решение".**</span><span class="sxs-lookup"><span data-stu-id="b6a84-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="b6a84-135">Перейдите в расположение, в котором сохранен пример, щелкните **WrapPST.vcproj** и нажмите кнопку **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="b6a84-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="b6a84-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="b6a84-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="b6a84-137">В **диалоговом окне** "Сохранить файл как" нажмите кнопку **"Сохранить".**</span><span class="sxs-lookup"><span data-stu-id="b6a84-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="b6a84-138">В папке, в которой сохранен пример,  щелкните правой кнопкой мыши файлinstall.batи выберите "Запуск от прав **администратора".**</span><span class="sxs-lookup"><span data-stu-id="b6a84-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="b6a84-139">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="b6a84-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

