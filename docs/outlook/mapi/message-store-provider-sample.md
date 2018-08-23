---
title: Пример поставщика хранилища сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 25c606531aa9a7436306a1b87c32aab49fd975db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593916"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="0c83d-103">Пример поставщика хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="0c83d-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="0c83d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c83d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c83d-105">Оболочку PST поставщик хранилища использует поставщика личных папок (PST) файла как серверные компоненты для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="0c83d-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="0c83d-106">Оболочку поставщика хранилища PST-файлов можно использовать интерфейс API репликации.</span><span class="sxs-lookup"><span data-stu-id="0c83d-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="0c83d-107">API репликации можно реплицировать элементов из хранилища данных в Microsoft Outlook PST-хранилище.</span><span class="sxs-lookup"><span data-stu-id="0c83d-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="0c83d-108">Использование API репликации для репликации данных в выделенном PST-хранилище и отслеживание состояния синхронизации.</span><span class="sxs-lookup"><span data-stu-id="0c83d-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="0c83d-109">Дополнительные сведения [О репликации API](about-the-replication-api.md)см.</span><span class="sxs-lookup"><span data-stu-id="0c83d-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="0c83d-110">Большая часть функций в оболочку PST поставщик хранилища передать свои аргументы непосредственно к базовым поставщиком PST-файлов.</span><span class="sxs-lookup"><span data-stu-id="0c83d-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="0c83d-111">Некоторые функции требуют специальных реализаций и описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="0c83d-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c83d-112">Исполняемый файл:</span><span class="sxs-lookup"><span data-stu-id="0c83d-112">Executable:</span></span>  <br/> |<span data-ttu-id="0c83d-113">WrpPST32.dll</span><span class="sxs-lookup"><span data-stu-id="0c83d-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="0c83d-114">Каталог исходного кода:</span><span class="sxs-lookup"><span data-stu-id="0c83d-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="0c83d-115">SampleWrappedPSTStoreProvider\WrapPST</span><span class="sxs-lookup"><span data-stu-id="0c83d-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="0c83d-116">Язык:</span><span class="sxs-lookup"><span data-stu-id="0c83d-116">Language:</span></span>  <br/> |<span data-ttu-id="0c83d-117">C++</span><span class="sxs-lookup"><span data-stu-id="0c83d-117">C++</span></span>  <br/> |
|<span data-ttu-id="0c83d-118">Платформы:</span><span class="sxs-lookup"><span data-stu-id="0c83d-118">Platforms:</span></span>  <br/> |<span data-ttu-id="0c83d-119">Microsoft Visual Studio 2008 для компиляции для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="0c83d-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="0c83d-120">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="0c83d-120">Supported Features</span></span>

<span data-ttu-id="0c83d-121">В этом примере поддерживает Microsoft Outlook 2010, 64-разрядная версия и теперь обновлен для Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="0c83d-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="0c83d-122">В следующих разделах для получения дополнительных сведений:</span><span class="sxs-lookup"><span data-stu-id="0c83d-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="0c83d-123">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="0c83d-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="0c83d-124">Инициализация поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="0c83d-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="0c83d-125">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="0c83d-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="0c83d-126">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="0c83d-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="0c83d-127">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="0c83d-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="0c83d-128">**Чтобы установить оболочку PST поставщик хранилища**</span><span class="sxs-lookup"><span data-stu-id="0c83d-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="0c83d-129">Чтобы загрузить поставщик оболочку PST-файлов, обратитесь к разделу [Загрузка примеров Outlook MAPI](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="0c83d-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="0c83d-130">Найдите папку, в которой вы сохранили примеры Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="0c83d-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="0c83d-131">Щелкните правой кнопкой мыши **OutlookMAPISamples -\<номер версии\> ** ZIP-папку и выберите команду **Извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="0c83d-132">Нажмите кнопку **Обзор**, выберите расположение, где требуется сохранить образца и нажмите кнопку **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="0c83d-133">Запустите Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="0c83d-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="0c83d-134">В Microsoft Visual Studio 2008 откройте меню **файл**, выберите команду **Открыть**и выберите **Проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="0c83d-135">Перейдите к папке, в которой вы сохранили примера **WrapPST.vcproj**и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="0c83d-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="0c83d-137">В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="0c83d-138">В папке, где был сохранен примера щелкните правой кнопкой мыши файл **install.bat** и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="0c83d-139">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="0c83d-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

