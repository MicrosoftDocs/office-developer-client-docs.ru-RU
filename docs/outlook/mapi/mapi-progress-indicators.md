---
title: Индикаторы прогресса MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410709"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="ce4e5-103">Индикаторы прогресса MAPI</span><span class="sxs-lookup"><span data-stu-id="ce4e5-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="ce4e5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ce4e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ce4e5-105">Выполнение многих операций для клиентов может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="ce4e5-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="ce4e5-106">Чтобы информировать клиентов о ходе длительной операции, можно показать индикатор, который графически отображает готовую часть операции в любой момент от начала операции до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="ce4e5-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="ce4e5-107">Индикатор прогресса показывает процент от общей операции, которая должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="ce4e5-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="ce4e5-108">Следующие методы поддерживают длительные операции и отображение индикатора прогресса:</span><span class="sxs-lookup"><span data-stu-id="ce4e5-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="ce4e5-109">[IMAPIFolder::CopyMessages,](imapifolder-copymessages.md) [IMAPIFolder::CopyFolder,](imapifolder-copyfolder.md) [IMAPIFolder::D eleteMessages,](imapifolder-deletemessages.md) [IMAPIFolder::D eleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="ce4e5-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="ce4e5-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="ce4e5-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="ce4e5-111">[IMAPISupport::D oCopyProps,](imapisupport-docopyprops.md) [IMAPISupport::D oCopyTo,](imapisupport-docopyto.md) [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)и [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="ce4e5-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="ce4e5-112">[IMessage::D eleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="ce4e5-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="ce4e5-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="ce4e5-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="ce4e5-114">Чтобы отобразить индикатор прогресса, MAPI определяет объект прогресса.</span><span class="sxs-lookup"><span data-stu-id="ce4e5-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="ce4e5-115">Объекты progress реализуют [интерфейс IMAPIProgress : IUnknown,](imapiprogressiunknown.md) интерфейс, который включает методы для установления диапазона индикатора и создания дисплея.</span><span class="sxs-lookup"><span data-stu-id="ce4e5-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="ce4e5-116">MAPI обеспечивает реализацию объекта progress, как и некоторые клиенты.</span><span class="sxs-lookup"><span data-stu-id="ce4e5-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="ce4e5-117">При его поставке необходимо использовать реализацию клиента в качестве параметра ввода метода выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ce4e5-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="ce4e5-118">Если клиент передает NULL вместо указателя на объект прогресса, используйте реализацию MAPI, позвонив [методу IMAPISupport::D oProgressDialog.](imapisupport-doprogressdialog.md)</span><span class="sxs-lookup"><span data-stu-id="ce4e5-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ce4e5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="ce4e5-119">See also</span></span>



[<span data-ttu-id="ce4e5-120">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="ce4e5-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

