---
title: Регистрация служб и поставщиков служб в MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Последнее изменение: 18 июля 2013 г.'
ms.openlocfilehash: 2eb7f1b496e0732b157ea4f9105a0e067329c52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812113"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="5a3c1-103">Регистрация служб и поставщиков служб в MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="5a3c1-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="5a3c1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5a3c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5a3c1-105">Для установки нового поставщика в системе требуется обновление файла MapiSvc.inf для указания на новый поставщик.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="5a3c1-106">Стандартные свойства, установленные во время настройки, которые включают следующие информирование MAPI расположение библиотеки поставщика динамической компоновки (DLL):</span><span class="sxs-lookup"><span data-stu-id="5a3c1-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="5a3c1-107">**PR_SERVICE_DLL_NAME** , указанного в разделе **[Службы сообщений]** .</span><span class="sxs-lookup"><span data-stu-id="5a3c1-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="5a3c1-108">**PR_PROVIDER_DLL_NAME** , указанного в разделе **[Поставщика услуг]** .</span><span class="sxs-lookup"><span data-stu-id="5a3c1-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="5a3c1-109">Ожидается, что значение имя вашего поставщика .dll (без суффикс «32»).</span><span class="sxs-lookup"><span data-stu-id="5a3c1-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="5a3c1-110">MAPI загружает ваш поставщик, выполнив поиск по пути.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="5a3c1-111">Выравнивание пути в MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="5a3c1-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="5a3c1-112">В папке Program Files, обновления в переменную path, чтобы разрешить поставщики MAPI для работы требует установки большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="5a3c1-113">С некоторыми ограничениями Microsoft Outlook 2010 и Outlook 2013 позволяет разместить полные пути к поставщики MAPI.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="5a3c1-114">При регистрации у поставщика в MapiSvc.inf, можно поместить полный путь к поставщику в разделе свойства MAPI, **PR_SERVICE_DLL_NAME** и **PR_PROVIDER_DLL_NAME**.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="5a3c1-115">В любом свойство полный путь должен быть без суффикса «32», так как MAPI по-прежнему производится, добавьте к имени файла перед нужны для файла.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="5a3c1-116">Это означает, что при регистрации путь «c:\mypath\myprovider.dll» MAPI попытается загрузить «c:\mypath\myprovider32.dll».</span><span class="sxs-lookup"><span data-stu-id="5a3c1-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="5a3c1-117">Поскольку Outlook MAPI изначально не предназначен для учета полные пути, выполнив поиск первого периода, в строке, которая означает, что пути, содержащие другие периоды не могут работать, поэтому нельзя использовать пути, такие как выполнить этот вставки суффикс «32» «c:\my.path\myprovider.dll» или «c:\mypath\my.provider.dll».</span><span class="sxs-lookup"><span data-stu-id="5a3c1-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="5a3c1-118">В некоторых случаях в хранилище поставщика будет создана идентификаторы записей с помощью функции **WrapStoreEntryID** , который принимает в качестве параметра имя вашего поставщика.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5a3c1-119">При использовании полные пути в MapiSvc.inf необходимо использовать тот же путь в вызове **WrapStoreEntryID**.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="5a3c1-120">Кроме того пути, который использован может быть преобразован в Юникод с использованием кодовой страницы, предоставленные функции [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) и обратно.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="5a3c1-121">При выборе пути, который содержит символы, которые не могут выдержать обмен через функции [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) и [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) могут возникнуть сбой.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="5a3c1-122">Для демонстрации эту функцию был обновлен [Пример оболочку PST -файлов](http://ol2010mapisamples.codeplex.com/) на сайте CodePlex - соответствующие функциональные возможности в **MergeWithMapiSvc** и **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="5a3c1-122">For a demonstration of this functionality, the [Wrapped PST sample](http://ol2010mapisamples.codeplex.com/) on CodePlex has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

