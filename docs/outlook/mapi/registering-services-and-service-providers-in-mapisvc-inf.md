---
title: Регистрация служб и поставщиков служб в MapiSvc. INF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Дата последнего изменения: 18 июля 2013 г.'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328373"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a><span data-ttu-id="6eb2f-103">Регистрация служб и поставщиков служб в MapiSvc. INF</span><span class="sxs-lookup"><span data-stu-id="6eb2f-103">Registering Services and Service Providers in MapiSvc.inf</span></span>

 
  
<span data-ttu-id="6eb2f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6eb2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6eb2f-105">Для установки нового поставщика в системе необходимо обновить файл MapiSvc. INF, указав нового поставщика.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-105">Installing a new provider on a system requires updating the MapiSvc.inf file to point to the new provider.</span></span> <span data-ttu-id="6eb2f-106">Стандартные свойства, заданные во время настройки, включая следующие, информируют MAPI, где найти библиотеку динамической компоновки поставщика (DLL):</span><span class="sxs-lookup"><span data-stu-id="6eb2f-106">Standard properties set during configuration, which include the following, inform MAPI where to find the provider's dynamic-link library (.dll):</span></span>
  
- <span data-ttu-id="6eb2f-107">**Пр_сервице_длл_наме** задается в разделе **[Message Service]** .</span><span class="sxs-lookup"><span data-stu-id="6eb2f-107">The **PR_SERVICE_DLL_NAME** is specified in the **[Message Service]** section.</span></span> 
    
- <span data-ttu-id="6eb2f-108">**Пр_провидер_длл_наме** задается в разделе **[Provider Service]** .</span><span class="sxs-lookup"><span data-stu-id="6eb2f-108">The **PR_PROVIDER_DLL_NAME** is specified in the **[Service Provider]** section.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6eb2f-109">Ожидается, что вы задаете имя DLL поставщика (без суффикса "32").</span><span class="sxs-lookup"><span data-stu-id="6eb2f-109">The expectation is that you set the name of your provider's .dll (without the suffix "32").</span></span> <span data-ttu-id="6eb2f-110">После этого MAPI загружает поставщик, выполняя поиск по пути.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-110">MAPI then loads your provider by looking for it on the path.</span></span> 
  
## <a name="putting-a-path-in-mapisvcinf"></a><span data-ttu-id="6eb2f-111">Размещение пути в MapiSvc. INF</span><span class="sxs-lookup"><span data-stu-id="6eb2f-111">Putting a Path in MapiSvc.inf</span></span>

<span data-ttu-id="6eb2f-112">Большинство приложений устанавливаются в разделе Program Files, поэтому необходимо обновить переменную Path, чтобы разрешить поставщикам MAPI работать.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-112">Most applications install under Program Files, requiring an update to the path variable to allow MAPI providers to work.</span></span> <span data-ttu-id="6eb2f-113">С некоторыми ограничениями Microsoft Outlook 2010 и Outlook 2013 могут поддерживать полные пути к поставщикам MAPI.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-113">With a few restrictions Microsoft Outlook 2010 and Outlook 2013 can accommodate full paths to MAPI providers.</span></span>
  
<span data-ttu-id="6eb2f-114">При регистрации поставщика в MapiSvc. inf можно поместить полный путь к поставщику в свойствах MAPI **пр_сервице_длл_наме** и **пр_провидер_длл_наме**.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-114">When registering your provider in MapiSvc.inf, you could put the full path to the provider in the MAPI properties **PR_SERVICE_DLL_NAME** and **PR_PROVIDER_DLL_NAME**.</span></span>
  
<span data-ttu-id="6eb2f-115">В обоих свойствах полный путь должен быть без суффикса "32", так как MAPI продолжает добавлять его в имя файла, прежде чем искать файл.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-115">In either property, the full path must be without the suffix "32", because MAPI continues to append that to the filename before looking for your file.</span></span> <span data-ttu-id="6eb2f-116">Это означает, что если вы зарегистрируете путь "к:\мипас\мипровидер.длл", MAPI предпримет попытку загрузить "c:\mypath\myprovider32.dll".</span><span class="sxs-lookup"><span data-stu-id="6eb2f-116">This means that if you register the path "c:\mypath\myprovider.dll", MAPI will attempt to load "c:\mypath\myprovider32.dll".</span></span>
  
<span data-ttu-id="6eb2f-117">Так как MAPI Outlook изначально не предназначался для размещения полных путей, он выполняет эту вставку суффикса "32", выполняя поиск первого периода в строке, что означает, что пути, содержащие другие точки, не могут работать, поэтому нельзя использовать такие пути, как "к:\ми.пас\мипровидер.длл" или "к:\мипас\ми.провидер.длл".</span><span class="sxs-lookup"><span data-stu-id="6eb2f-117">Because Outlook's MAPI was not originally designed to accommodate full paths, it accomplishes this insertion of the "32" suffix by looking for the first period in the string, which means that paths that contain other periods cannot work, so you cannot use paths such as "c:\my.path\myprovider.dll" or "c:\mypath\my.provider.dll".</span></span>
  
<span data-ttu-id="6eb2f-118">Иногда в поставщике хранилища вы будете создавать идентификаторы записей с помощью функции **врапсторинтрид** , которая принимает в качестве параметра имя поставщика.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-118">Sometimes in a store provider you will generate entry identifiers using the **WrapStoreEntryID** function, which takes as a parameter the name of your provider.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6eb2f-119">При использовании полных путей в MapiSvc. INF необходимо использовать один и тот же путь во всех вызовах **врапсторинтрид**.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-119">If you are using full paths in MapiSvc.inf, you must use the same path in any calls to **WrapStoreEntryID**.</span></span> 
  
<span data-ttu-id="6eb2f-120">Кроме того, используемый путь можно преобразовать в Юникод и из него, используя кодовую страницу, предоставляемую функцией [жетакп](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) .</span><span class="sxs-lookup"><span data-stu-id="6eb2f-120">Additionally, the path you use may be converted to and from Unicode using the code page provided by the [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) function.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="6eb2f-121">Если выбрать путь, который содержит символы, которые не могут быть циклически продерживаться, через функции [мултибитетовидечар](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) и [видечартомултибите](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) будет возникать ошибка.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-121">You will experience failure if you choose a path that contains characters that cannot survive such a roundtrip through the [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) and [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) functions.</span></span> 
  
<span data-ttu-id="6eb2f-122">В качестве демонстрации этой функции вы перестроили [Пример упакованНОГО PST](https://github.com/stephenegriffin/Outlook2010CodeSamples) -файла на сайте GitHub, и у вас есть соответствующие функции в **мержевисмаписвк** и **женератепровидерпас**.</span><span class="sxs-lookup"><span data-stu-id="6eb2f-122">For a demonstration of this functionality, the [Wrapped PST sample](https://github.com/stephenegriffin/Outlook2010CodeSamples) on GitHub has been revised - the pertinent functionality is in **MergeWithMapiSvc** and **GenerateProviderPath**.</span></span>
  

