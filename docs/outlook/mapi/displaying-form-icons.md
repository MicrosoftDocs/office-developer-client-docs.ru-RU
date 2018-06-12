---
title: Отображение значков формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 197e72ab-f9d6-4889-a677-0ce4c27b1aad
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: b2e79e5568de38bee9a97c9df2598b30f1ba1bdf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808317"
---
# <a name="displaying-form-icons"></a><span data-ttu-id="4f128-103">Отображение значков формы</span><span class="sxs-lookup"><span data-stu-id="4f128-103">Displaying Form Icons</span></span>

  
  
<span data-ttu-id="4f128-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f128-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f128-105">При отображении списка сообщений в папке, полезно для пользователей различать сообщения с помощью пользовательских классов сообщений из стандартных IPM. Обратите внимание, сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f128-105">When displaying a list of messages in a folder, it is helpful to your users if you distinguish messages with custom message classes from the standard IPM.Note messages.</span></span> <span data-ttu-id="4f128-106">Настраиваемые классы сообщения соответствуют формы серверы и серверы формы предоставляют значки будет представлять собой.</span><span class="sxs-lookup"><span data-stu-id="4f128-106">Custom message classes correspond to form servers, and form servers provide icons to represent themselves.</span></span> <span data-ttu-id="4f128-107">В списке сообщений для оповещения пользователей для каждого сообщения класс сообщения можно отобразить эти значки, прежде чем пользователь открывает сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f128-107">You can display these icons in the list of messages to alert users to each message's message class before the user opens the messages.</span></span> <span data-ttu-id="4f128-108">Как правило значок в свойстве **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) формы, то, которое должно отображаться в списке сообщений.</span><span class="sxs-lookup"><span data-stu-id="4f128-108">Typically, the icon in the form's **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)) property is the one that should be displayed in the list of messages.</span></span> <span data-ttu-id="4f128-109">Формы также имеют свойство **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)), которые могут отображаться, когда форма свернута в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="4f128-109">Forms also have a **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) property that can be displayed when the form is minimized in a property sheet.</span></span>
  
 <span data-ttu-id="4f128-110">**Чтобы получить значок для класса сообщения без активации сервера форм для этого класса сообщений**</span><span class="sxs-lookup"><span data-stu-id="4f128-110">**To get an icon for a message class without activating the form server for that message class**</span></span>
  
1. <span data-ttu-id="4f128-111">Вызовите метод [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) для получения указателя на [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4f128-111">Call the [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method to get a pointer to an [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
2. <span data-ttu-id="4f128-112">Вызовите метод [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) для получения указателя на [IMAPIFormInfo: IMAPIProp](imapiforminfoimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4f128-112">Call the [IMAPIFormContainer::ResolveMessageClass](imapiformcontainer-resolvemessageclass.md) method to get a pointer to an [IMAPIFormInfo : IMAPIProp](imapiforminfoimapiprop.md) interface.</span></span> 
    
3. <span data-ttu-id="4f128-113">Вызовите метод [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) для получения дескриптор значка.</span><span class="sxs-lookup"><span data-stu-id="4f128-113">Call the [IMAPIFormInfo::MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) method to get an icon handle.</span></span> 
    
<span data-ttu-id="4f128-114">Значок могут отображаться с помощью стандартных Win32 API.</span><span class="sxs-lookup"><span data-stu-id="4f128-114">The icon can then be displayed using standard Win32 APIs.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4f128-115">При наличии значок класс сообщения, внесите все усилия для кэширования этот значок.</span><span class="sxs-lookup"><span data-stu-id="4f128-115">Once you have the icon for a message class, make every effort to cache that icon.</span></span> <span data-ttu-id="4f128-116">Не кэширование значки серьезно влияет на производительность клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="4f128-116">Not caching icons severely affects the performance of client applications.</span></span> <span data-ttu-id="4f128-117">При кэшировании значки, следует избегать отношений между классы сообщений и их подклассов.</span><span class="sxs-lookup"><span data-stu-id="4f128-117">When caching icons, be careful of the relationships between message classes and their subclasses.</span></span> <span data-ttu-id="4f128-118">Например если IPM. Класс сообщения Note.Meeting.Cancel происходит для разрешения IPM. Обратите внимание на то, не предполагается, что все подклассов IPM. Примечание следует использовать значок IPM. Примечание.</span><span class="sxs-lookup"><span data-stu-id="4f128-118">For example, if the IPM.Note.Meeting.Cancel message class happens to resolve back to IPM.Note, do not assume that all subclasses of IPM.Note should use the icon for IPM.Note.</span></span> 
  

