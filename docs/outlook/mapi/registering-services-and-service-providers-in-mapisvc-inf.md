---
title: Регистрация служб и поставщиков услуг в MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Последнее изменение: 18 июля 2013 г.'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328373"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="9adc5-103">Регистрация служб и поставщиков услуг в MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="9adc5-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="9adc5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9adc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9adc5-105">Установка нового поставщика в системе требует обновления файла MapiSvc.inf, чтобы указать на нового поставщика.</span><span class="sxs-lookup"><span data-stu-id="9adc5-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="9adc5-106">Стандартные свойства, заданная во время настройки, включая следующие, информируют MAPI, где найти библиотеку динамических ссылок поставщика (.dll):</span><span class="sxs-lookup"><span data-stu-id="9adc5-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="9adc5-107">Этот **PR_SERVICE_DLL_NAME** указан в разделе **[Служба сообщений].**</span><span class="sxs-lookup"><span data-stu-id="9adc5-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="9adc5-108">Этот **PR_PROVIDER_DLL_NAME** указан в разделе **[Поставщик услуг].**</span><span class="sxs-lookup"><span data-stu-id="9adc5-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="9adc5-109">Ожидается, что вы установите имя .dll поставщика (без суффикса "32").</span><span class="sxs-lookup"><span data-stu-id="9adc5-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="9adc5-110">ПОСЛЕ этого MAPI загружает поставщика, ищем его на пути.</span><span class="sxs-lookup"><span data-stu-id="9adc5-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="9adc5-111">Ввод пути в MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="9adc5-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="9adc5-112">Большинство приложений устанавливаются в программных файлах, что требует обновления переменной пути, чтобы разрешить работу поставщиков MAPI.</span><span class="sxs-lookup"><span data-stu-id="9adc5-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="9adc5-113">С несколькими ограничениями Microsoft Outlook 2010, русская версия и Outlook 2013 может вместить полные пути к поставщикам MAPI.</span><span class="sxs-lookup"><span data-stu-id="9adc5-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="9adc5-114">При регистрации поставщика в MapiSvc.inf можно ввести полный путь к поставщику в свойствах MAPI PR_SERVICE_DLL_NAME **и PR_PROVIDER_DLL_NAME**. </span><span class="sxs-lookup"><span data-stu-id="9adc5-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="9adc5-115">В любом свойстве полный путь должен быть без суффикса "32", так как MAPI продолжает прикрепить его к имени файла перед поиском файла.</span><span class="sxs-lookup"><span data-stu-id="9adc5-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="9adc5-116">Это означает, что если вы зарегистрируете путь "c:\mypath\myprovider.dll", MAPI попытается загрузить "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="9adc5-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="9adc5-117">Поскольку mapI Outlook изначально не был разработан для размещения полных путей, он выполняет эту вставку суффикса "32", ища первый период в строке, что означает, что пути, содержащие другие периоды, не могут работать, поэтому вы не можете использовать пути, такие как "c:\my.path\myprovider.dll" или "c:\mypath\my.provider.dll".</span><span class="sxs-lookup"><span data-stu-id="9adc5-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="9adc5-118">Иногда в поставщике магазинов вы создаете идентификаторы записей с помощью функции **WrapStoreEntryID,** которая принимает в качестве параметра имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="9adc5-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="9adc5-119">Если вы используете полные пути в MapiSvc.inf, необходимо использовать тот же путь в любых вызовах **в WrapStoreEntryID.**</span><span class="sxs-lookup"><span data-stu-id="9adc5-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="9adc5-120">Кроме того, путь, который вы используете, может быть преобразован в Юникод и из него с помощью страницы кода, предоставленной функцией [GetACP.](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/)</span><span class="sxs-lookup"><span data-stu-id="9adc5-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="9adc5-121">При выборе пути, который содержит символы, которые не могут выдержать такой кругооборот с помощью функций [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) и [WideCharToMultiByte,](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) вы испытаете сбой.</span><span class="sxs-lookup"><span data-stu-id="9adc5-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="9adc5-122">Для демонстрации этой функции был пересмотрен пример упакованного [PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) на GitHub - в **MergeWithMapiSvc** и **GenerateProviderPath**.</span><span class="sxs-lookup"><span data-stu-id="9adc5-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

