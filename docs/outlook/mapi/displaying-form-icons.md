---
title: Отображение значков форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c93912d19f0ad3c3231092c82f27cec9e3f15b3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438633"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="92ccf-103">Отображение значков форм</span><span class="sxs-lookup"><span data-stu-id="92ccf-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="92ccf-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92ccf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92ccf-105">При отображении списка сообщений в папке пользователи могут быть полезны, если вы отличает сообщения с пользовательскими классами сообщений от стандартного IPM. Обратите внимание на сообщения.</span><span class="sxs-lookup"><span data-stu-id="92ccf-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="92ccf-106">Пользовательские классы сообщений соответствуют серверам форм, а серверы форм предоставляют значки для самостоятельного представления.</span><span class="sxs-lookup"><span data-stu-id="92ccf-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="92ccf-107">Вы можете отображать эти значки в списке сообщений, чтобы оповещать пользователей о каждом классе сообщений каждого сообщения, прежде чем пользователь откроет эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="92ccf-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="92ccf-108">Как правило, значок в свойстве **PR_MINI_ICON** формы ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) должен отображаться в списке сообщений.</span><span class="sxs-lookup"><span data-stu-id="92ccf-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="92ccf-109">Формы также имеют свойство **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)), которое может отображаться, если форма свернута в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="92ccf-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="92ccf-110">**Получение значка для класса сообщений без активации сервера форм для этого класса сообщений**</span><span class="sxs-lookup"><span data-stu-id="92ccf-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="92ccf-111">Вызовите метод [имапиформмгр:: опенформконтаинер](imapiformmgr-openformcontainer.md) , чтобы получить указатель на интерфейс [имапиформконтаинер: IUnknown](imapiformcontaineriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="92ccf-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="92ccf-112">Вызовите метод [имапиформконтаинер:: ресолвемессажекласс](imapiformcontainer-resolvemessageclass.md) , чтобы получить указатель на интерфейс [имапиформинфо: IMAPIProp](imapiforminfoimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="92ccf-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="92ccf-113">Вызовите метод [имапиформинфо:: макеиконфромбинари](imapiforminfo-makeiconfrombinary.md) , чтобы получить маркер значка.</span><span class="sxs-lookup"><span data-stu-id="92ccf-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="92ccf-114">Затем значок можно отобразить с помощью стандартных интерфейсов API Win32.</span><span class="sxs-lookup"><span data-stu-id="92ccf-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="92ccf-115">Получив значок для класса сообщений, сделайте все усилия для кэширования этого значка.</span><span class="sxs-lookup"><span data-stu-id="92ccf-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="92ccf-116">Не кэширование значков серьезно влияет на производительность клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="92ccf-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="92ccf-117">При кэшировании значков следует следить за связями между классами сообщений и их подклассами.</span><span class="sxs-lookup"><span data-stu-id="92ccf-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="92ccf-118">Например, если элемент IPM. Note. Meeting. Cancel Message, чтобы разрешить обратное разрешение в IPM. Обратите внимание, что не следует предполагать, что все подклассы IPM. Обратите внимание, что следует использовать значок IPM. Ноте.</span><span class="sxs-lookup"><span data-stu-id="92ccf-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

