---
title: Справочник разработчика OneNote
manager: soliver
ms.date: 05/16/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4c4ef9e8-6b30-481b-8023-2e1280bcbcc9
description: Эта справка содержит обзоры понятий и программный справочные материалы, которые помогут в разработке решений для настольных систем клиентских приложений, OneNote 2013.
ms.openlocfilehash: b19e9957d1faed1bda150df34f61209d9f40fc5d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395710"
---
# <a name="onenote-developer-reference"></a><span data-ttu-id="1b31f-103">Справочник разработчика OneNote</span><span class="sxs-lookup"><span data-stu-id="1b31f-103">OneNote developer reference</span></span>

<span data-ttu-id="1b31f-104">Эта справка содержит обзоры понятий и программный справочные материалы, которые помогут в разработке решений для настольных систем клиентских приложений, OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="1b31f-104">This reference contains conceptual overviews and programmatic references to guide you in developing solutions for OneNote 2013 desktop client applications.</span></span> <span data-ttu-id="1b31f-105">Включает в себя все дополнения и изменяется на OneNote 2013 программный интерфейс (API) и предоставляет примеры кода на C# показано, как выполнять некоторые задачи в OneNote.</span><span class="sxs-lookup"><span data-stu-id="1b31f-105">It includes all the additions and changes to the OneNote 2013 application programming interface (API), and provides code samples in C# to show how to perform some tasks in OneNote.</span></span> <span data-ttu-id="1b31f-106">API-Интерфейс OneNote 2013 позволяет пользователям программный доступ и редактирование содержимого OneNote.</span><span class="sxs-lookup"><span data-stu-id="1b31f-106">The OneNote 2013 API enables users to programmatically access and edit OneNote content.</span></span> <span data-ttu-id="1b31f-107">Пользователи также могут вносить изменения в представление окон OneNote.</span><span class="sxs-lookup"><span data-stu-id="1b31f-107">Users can also make changes to the view of OneNote windows.</span></span>
  
<span data-ttu-id="1b31f-108">Эта документация включает следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="1b31f-108">This documentation contains the following information:</span></span>
  
- <span data-ttu-id="1b31f-109">[Окно интерфейсы](window-interfaces-onenote.md): описываются интерфейсы **Window** и **Windows** , которые предоставляют пользователям возможность нумерации внутри набора OneNote windows и изменении окно свойств.</span><span class="sxs-lookup"><span data-stu-id="1b31f-109">[Window interfaces](window-interfaces-onenote.md): Describes the **Window** and **Windows** interfaces, which enable users to enumerate through the set of OneNote windows and modify certain window properties.</span></span> 
    
- <span data-ttu-id="1b31f-110">[Интерфейсы поле диалоговое окно быстрого контроля над заполнением записей](quick-filing-dialog-box-interfaces-onenote.md): описываются интерфейсы, которые можно использовать для задания программным путем диалоговое окно **Быстрого контроля над заполнением записей** в OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="1b31f-110">[Quick Filing dialog box interfaces](quick-filing-dialog-box-interfaces-onenote.md): Describes the interfaces that you can use to programmatically customize the **Quick Filing** dialog box in OneNote 2013.</span></span> 
    
- <span data-ttu-id="1b31f-111">[Интерфейс Application](application-interface-onenote.md): описываются методы, свойства и события, которые позволяют получать, работа с элементами управления и обновление данных OneNote 2013 и контента.</span><span class="sxs-lookup"><span data-stu-id="1b31f-111">[Application interface](application-interface-onenote.md): Describes methods, properties, and events that help retrieve, manipulate, and update OneNote 2013 information and content.</span></span>
    
- <span data-ttu-id="1b31f-112">[Перечисления](enumerations-onenote-developer-reference.md): описание перечислений в объектной модели OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="1b31f-112">[Enumerations](enumerations-onenote-developer-reference.md): Describes the enumerations in the OneNote 2013 object model.</span></span>
    
- <span data-ttu-id="1b31f-113">[Коды ошибок](error-codes-onenote.md): перечислены коды ошибок в объектной модели OneNote 2013.</span><span class="sxs-lookup"><span data-stu-id="1b31f-113">[Error codes](error-codes-onenote.md): Lists the error codes in the OneNote 2013 object model.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1b31f-114">Описанные в этой документации API предназначены только для классических приложений OneNote Win32 в сценариях без подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="1b31f-114">The APIs described in this documentation are intended only for OneNote Win32 desktop client solutions in unconnected scenarios.</span></span> <span data-ttu-id="1b31f-115">В сценариях с подключением к сети используйте рекомендуемые API службы OneNote.</span><span class="sxs-lookup"><span data-stu-id="1b31f-115">For connected scenarios, use the recommended OneNote service APIs.</span></span> <span data-ttu-id="1b31f-116">Дополнительные сведения см. на сайте [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span><span class="sxs-lookup"><span data-stu-id="1b31f-116">To learn more, visit [dev.onenote.com](https://go.microsoft.com/fwlink/?LinkID=390615).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b31f-117">См. также</span><span class="sxs-lookup"><span data-stu-id="1b31f-117">See also</span></span>

- [<span data-ttu-id="1b31f-118">OneNote для разработчиков (en)</span><span class="sxs-lookup"><span data-stu-id="1b31f-118">OneNote for developers</span></span>](https://go.microsoft.com/fwlink/?LinkID=390615)   
- <span data-ttu-id="1b31f-119">[Примеры кода на репозиториев](https://github.com/OneNoteDev/) (API службы OneNote)</span><span class="sxs-lookup"><span data-stu-id="1b31f-119">[Samples on GitHub](https://github.com/OneNoteDev/) (OneNote service APIs)</span></span>     
- [<span data-ttu-id="1b31f-120">Специальные возможности в продуктах Майкрософт (Возможно, на английском языке)</span><span class="sxs-lookup"><span data-stu-id="1b31f-120">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)    
- [<span data-ttu-id="1b31f-121">Обозначения в документации</span><span class="sxs-lookup"><span data-stu-id="1b31f-121">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)    
- [<span data-ttu-id="1b31f-122">Сведения об авторских правах Справочник разработчика по OneNote</span><span class="sxs-lookup"><span data-stu-id="1b31f-122">OneNote Developer Reference Copyright Information</span></span>](https://msdn.microsoft.com/library/office/jj680116.aspx)
    
    

