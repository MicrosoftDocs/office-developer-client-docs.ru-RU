---
title: Справочник разработчика OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Здесь представлены обзоры и справочники программирования, которыми можно руководствоваться при разработке решений для классических клиентских приложений OneNote 2013.
localization_priority: Priority
ms.openlocfilehash: d2b401a768e62c4b9712b1590bfaf499c2b022ab
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725926"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="f476a-103">Справочник разработчика OneNote</span><span class="sxs-lookup"><span data-stu-id="f476a-103">OneNote developer reference</span></span>

<span data-ttu-id="f476a-104">Здесь представлены обзоры и справочники программирования, которыми можно руководствоваться при разработке решений для классических клиентских приложений OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="f476a-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="f476a-105">Он включает все дополнения и изменения API-интерфейса для OneNote 2013 и содержит примеры кода на языке C#, демонстрирующие способы выполнения некоторых задач в OneNote.</span><span class="sxs-lookup"><span data-stu-id="f476a-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="f476a-106">API OneNote 2013 позволяет пользователям программным путем получать доступ к содержимому OneNote и изменять его.</span><span class="sxs-lookup"><span data-stu-id="f476a-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="f476a-107">Пользователи также могут вносить изменения в представление окон OneNote.</span><span class="sxs-lookup"><span data-stu-id="f476a-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="f476a-108">Эта документация включает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="f476a-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="f476a-109">[Интерфейсы окон](window-interfaces-onenote.md). Описаны интерфейсы **Window** и **Windows**, позволяющие пользователям просматривать набор окон OneNote и изменять некоторые свойства окон.</span><span class="sxs-lookup"><span data-stu-id="f476a-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="f476a-110">[Интерфейсы с диалоговым окном для удобной систематизации](quick-filing-dialog-box-interfaces-onenote.md). Описаны интерфейсы, которые можно использовать для программной настройки диалогового окна **Быстрая подготовка файлов** в OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="f476a-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="f476a-111">[Интерфейс приложения](application-interface-onenote.md). Описаны методы, свойства и события, помогающие получать и обновлять сведения и содержимое OneNote 2013, а также выполнять с ними операции.</span><span class="sxs-lookup"><span data-stu-id="f476a-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="f476a-112">[Перечисления](enumerations-onenote-developer-reference.md). Описаны перечисления в объектной модели OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="f476a-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="f476a-113">[Коды ошибок](error-codes-onenote.md). Перечислены коды ошибок в объектной модели OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="f476a-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="f476a-114">Описанные в этой документации API предназначены только для классических приложений OneNote Win32 в сценариях без подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="f476a-114">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios.</span></span> <span data-ttu-id="f476a-115">В сценариях с подключением к сети используйте рекомендуемые API службы OneNote.</span><span class="sxs-lookup"><span data-stu-id="f476a-115">For connected scenarios, use the recommended OneNote service APIs.</span></span> <span data-ttu-id="f476a-116">Дополнительные сведения см. на сайте [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="f476a-116">To learn more, visit [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f476a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f476a-117">See also</span></span>

- [<span data-ttu-id="f476a-118">OneNote для разработчиков</span><span class="sxs-lookup"><span data-stu-id="f476a-118">OneNote for developers</span></span>](https://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="f476a-119">[Примеры на портале GitHub](https://github.com/OneNoteDev/) (API службы OneNote)</span><span class="sxs-lookup"><span data-stu-id="f476a-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="f476a-120">Специальные возможности в продуктах Майкрософт</span><span class="sxs-lookup"><span data-stu-id="f476a-120">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="f476a-121">Обозначения в документации</span><span class="sxs-lookup"><span data-stu-id="f476a-121">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)    
- [<span data-ttu-id="f476a-122">Авторские права на справочник разработчика OneNote</span><span class="sxs-lookup"><span data-stu-id="f476a-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/library/office/jj680116.aspx)
    
    

