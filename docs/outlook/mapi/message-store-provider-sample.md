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
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436869"
---
# <a name="message-store-provider-sample"></a><span data-ttu-id="851b0-103">Пример поставщика хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="851b0-103">Message Store Provider Sample</span></span>

  
  
<span data-ttu-id="851b0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="851b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="851b0-105">Поставщик примера упакованного PST-хранилища использует поставщика файла личных папок (PST) в качестве фонового сервера для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="851b0-105">The Sample Wrapped PST Store Provider uses a Personal Folders file (PST) provider as the back end for storing data.</span></span> <span data-ttu-id="851b0-106">Поставщик упакованного PST-хранилища должен использоваться вместе с API репликации.</span><span class="sxs-lookup"><span data-stu-id="851b0-106">The wrapped PST store provider should be used together with the Replication API.</span></span> 
  
<span data-ttu-id="851b0-107">API репликации позволяет реплицировать элементы из внутреннего репозитория данных в хранилище PST Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="851b0-107">The Replication API enables you to replicate items from a back-end data repository into a Microsoft Outlook PST store.</span></span> <span data-ttu-id="851b0-108">Используйте API репликации для репликации данных в выделенное хранилище PST и отслеживания состояния синхронизации.</span><span class="sxs-lookup"><span data-stu-id="851b0-108">You use the Replication API to replicate the data into a dedicated PST store and keep track of the synchronization state.</span></span> <span data-ttu-id="851b0-109">Более подробную информацию можно узнать [в статье о API репликации](about-the-replication-api.md).</span><span class="sxs-lookup"><span data-stu-id="851b0-109">For more information, see [About the Replication API](about-the-replication-api.md).</span></span>
  
<span data-ttu-id="851b0-110">Большинство функций в примере поставщика упакованного PST-хранилища передают свои аргументы непосредственно базовому поставщику PST.</span><span class="sxs-lookup"><span data-stu-id="851b0-110">Most of the functions in the Sample Wrapped PST Store Provider pass their arguments directly to the underlying PST provider.</span></span> <span data-ttu-id="851b0-111">Для некоторых функций требуется специальная реализация, описанная в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="851b0-111">Certain functions require special implementation and are described in the following topics.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="851b0-112">Выполним</span><span class="sxs-lookup"><span data-stu-id="851b0-112">Executable:</span></span>  <br/> |<span data-ttu-id="851b0-113">WrpPST32. dll</span><span class="sxs-lookup"><span data-stu-id="851b0-113">WrpPST32.dll</span></span>  <br/> |
|<span data-ttu-id="851b0-114">Каталог исходного кода:</span><span class="sxs-lookup"><span data-stu-id="851b0-114">Source code directory:</span></span>  <br/> |<span data-ttu-id="851b0-115">самплевраппедпстсторепровидер\враппст</span><span class="sxs-lookup"><span data-stu-id="851b0-115">SampleWrappedPSTStoreProvider\WrapPST</span></span>  <br/> |
|<span data-ttu-id="851b0-116">Языки</span><span class="sxs-lookup"><span data-stu-id="851b0-116">Language:</span></span>  <br/> |<span data-ttu-id="851b0-117">Языка</span><span class="sxs-lookup"><span data-stu-id="851b0-117">C++</span></span>  <br/> |
|<span data-ttu-id="851b0-118">Embedded</span><span class="sxs-lookup"><span data-stu-id="851b0-118">Platforms:</span></span>  <br/> |<span data-ttu-id="851b0-119">Microsoft Visual Studio 2008 для компиляции для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="851b0-119">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="851b0-120">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="851b0-120">Supported Features</span></span>

<span data-ttu-id="851b0-121">В этом примере поддерживается Microsoft Outlook 2010 64 — бит, который теперь пересмотрен для Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="851b0-121">This sample supports Microsoft Outlook 2010 64-bit and has now been revised for Outlook 2013.</span></span> <span data-ttu-id="851b0-122">Дополнительные сведения можно найти в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="851b0-122">See the following topics for additional information:</span></span>
  
- [<span data-ttu-id="851b0-123">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="851b0-123">About the Replication API</span></span>](about-the-replication-api.md)
    
- [<span data-ttu-id="851b0-124">Инициализация поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="851b0-124">Initializing a Wrapped PST Store Provider</span></span>](initializing-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="851b0-125">Вход в систему поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="851b0-125">Logging On to a Wrapped PST Store Provider</span></span>](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="851b0-126">Использование поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="851b0-126">Using a Wrapped PST Store Provider</span></span>](using-a-wrapped-pst-store-provider.md)
    
- [<span data-ttu-id="851b0-127">Завершение работы поставщика упакованного PST-хранилища</span><span class="sxs-lookup"><span data-stu-id="851b0-127">Shutting Down a Wrapped PST Store Provider</span></span>](shutting-down-a-wrapped-pst-store-provider.md)
    
 <span data-ttu-id="851b0-128">**Установка примера поставщика упакованного PST-хранилища**</span><span class="sxs-lookup"><span data-stu-id="851b0-128">**To install the Sample Wrapped PST Store Provider**</span></span>
  
1. <span data-ttu-id="851b0-129">Загрузить пример поставщика упакованных PST-файлов можно в статье [Загрузка примеров для Outlook MAPI](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="851b0-129">To download the Sample Wrapped PST Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="851b0-130">Откройте папку, в которую были сохранены примеры Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="851b0-130">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="851b0-131">Щелкните правой кнопкой мыши папку Zip **\<аутлукмаписамплес-\> Version Number** и выберите пункт **извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="851b0-131">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and then click **Extract All**.</span></span>
    
3. <span data-ttu-id="851b0-132">Нажмите кнопку **Обзор**, выберите расположение, в котором нужно сохранить пример, а затем нажмите кнопку **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="851b0-132">Click **Browse**, select the location where you want to save the sample, and then click **Extract**.</span></span>
    
4. <span data-ttu-id="851b0-133">Запустите Microsoft Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="851b0-133">Run Microsoft Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="851b0-134">В Microsoft Visual Studio 2008 в меню **файл**выберите пункт **Открыть**, а затем выберите **проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="851b0-134">In Microsoft Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="851b0-135">Перейдите к папке, в которой сохранен пример, выберите **враппст. vcproj**, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="851b0-135">Browse to the location where you saved the sample, click **WrapPST.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="851b0-136">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="851b0-136">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="851b0-137">В диалоговом окне **сохранить файл как** нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="851b0-137">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="851b0-138">В папке, в которой сохранен пример, щелкните файл **install. bat** правой кнопкой мыши и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="851b0-138">In the folder where you saved the sample, right-click the **install.bat** file and then click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="851b0-139">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="851b0-139">In the **User Account Control** dialog box, click **Continue**.</span></span>
    

