---
title: Регистрация служб и поставщиков услуг в MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Last modified: July 18, 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328373"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="1afbc-103">Регистрация служб и поставщиков услуг в MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="1afbc-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="1afbc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1afbc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1afbc-105">Чтобы установить нового поставщика в системе, необходимо обновить файл MapiSvc.inf, чтобы он был указать на нового поставщика.</span><span class="sxs-lookup"><span data-stu-id="1afbc-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="1afbc-106">Стандартные свойства, заданная во время настройки, в том числе следующие, сообщают MAPI, где найти библиотеку динамической компоновки поставщика (DLL):</span><span class="sxs-lookup"><span data-stu-id="1afbc-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="1afbc-107">Этот **PR_SERVICE_DLL_NAME** указан в разделе **[Служба сообщений].**</span><span class="sxs-lookup"><span data-stu-id="1afbc-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="1afbc-108">Этот **PR_PROVIDER_DLL_NAME** указан в разделе **[Поставщик услуг].**</span><span class="sxs-lookup"><span data-stu-id="1afbc-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1afbc-109">Ожидается, что вы установите имя DLL поставщика (без суффикса "32").</span><span class="sxs-lookup"><span data-stu-id="1afbc-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="1afbc-110">Затем MAPI загружает поставщика, ищет его по пути.</span><span class="sxs-lookup"><span data-stu-id="1afbc-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="1afbc-111">Размещение пути в mapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="1afbc-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="1afbc-112">Большинство приложений устанавливаются в папке Program Files, что требует обновления переменной пути, чтобы разрешить работу поставщиков MAPI.</span><span class="sxs-lookup"><span data-stu-id="1afbc-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="1afbc-113">С помощью нескольких ограничений Microsoft Outlook 2010, русская версия Outlook 2013 могут использовать полные пути к поставщикам MAPI.</span><span class="sxs-lookup"><span data-stu-id="1afbc-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="1afbc-114">При регистрации поставщика в MapiSvc.inf можно уложить полный путь к поставщику в свойствах MAPI PR_SERVICE_DLL_NAME и **PR_PROVIDER_DLL_NAME.** </span><span class="sxs-lookup"><span data-stu-id="1afbc-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="1afbc-115">В обоих свойствах полный путь должен быть без суффикса "32", так как MAPI продолжает прикрепить его к имени файла перед поиском файла.</span><span class="sxs-lookup"><span data-stu-id="1afbc-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="1afbc-116">Это означает, что если вы зарегистрируете путь "c:\mypath\myprovider.dll", MAPI попытается загрузить "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="1afbc-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="1afbc-117">Так как MAPI Outlook изначально не был разработан для размещения полных путей, для этого вставляется суффикс "32", который ищет первый период в строке, что означает, что пути, содержащие другие точки, не могут работать, поэтому нельзя использовать такие пути, как "c:\my.path\myprovider.dll" или "c:\mypath\my.provider.dll".</span><span class="sxs-lookup"><span data-stu-id="1afbc-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="1afbc-118">Иногда в поставщике магазина идентификаторы записей создаются с помощью функции **WrapStoreEntryID,** которая принимает в качестве параметра имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="1afbc-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="1afbc-119">При использовании полных путей в MapiSvc.inf необходимо использовать тот же путь во всех вызовах **WrapStoreEntryID.**</span><span class="sxs-lookup"><span data-stu-id="1afbc-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="1afbc-120">Кроме того, путь, который вы используете, может быть преобразован в Юникод и из него, используя кодовую страницу, предоставленную функцией [GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)</span><span class="sxs-lookup"><span data-stu-id="1afbc-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="1afbc-121">Если выбрать путь, содержащий символы, которые не могут выдержать такую прокрутку с помощью функций [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) и [WideCharToMultiByte,](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) будет сбой.</span><span class="sxs-lookup"><span data-stu-id="1afbc-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="1afbc-122">Для демонстрации этой функциональности был изменен пример упакованного [PST-сайта](https://github.com/stephenegriffin/Outlook2010CodeSamples) на GitHub. Эта функциональная возможность находится в **MergeWithMapiSvc** и **GenerateProviderPath.**</span><span class="sxs-lookup"><span data-stu-id="1afbc-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

