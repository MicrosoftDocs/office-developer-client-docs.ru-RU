---
title: Индикаторы хода выполнения MAPI
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
# <a name="mapi-progress-indicators"></a><span data-ttu-id="c7446-103">Индикаторы хода выполнения MAPI</span><span class="sxs-lookup"><span data-stu-id="c7446-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="c7446-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7446-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7446-105">Многие операции, выполняемые для клиентов, могут занимать много времени.</span><span class="sxs-lookup"><span data-stu-id="c7446-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="c7446-106">Чтобы уведомить клиентов о ходе выполнения длительной операции, можно отобразить индикатор, отображающий законченную часть операции в любой заданную точку от начала операции до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="c7446-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="c7446-107">Индикатор выполнения показывает процент от общей операции, которую необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="c7446-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="c7446-108">Следующие методы поддерживают длительные операции и отображают индикатор хода выполнения:</span><span class="sxs-lookup"><span data-stu-id="c7446-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="c7446-109">[IMAPIFolder:: копимессажес](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Елетемессажес](imapifolder-deletemessages.md), [IMAPIFolder::D Елетефолдер](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)и [IMAPIFolder:: сетреадфлагс](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="c7446-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="c7446-110">[IMAPIProp:: копипропс](imapiprop-copyprops.md) и [IMAPIProp:: CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="c7446-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="c7446-111">[Имаписуппорт::D окопипропс](imapisupport-docopyprops.md), [Имаписуппорт::D окопито](imapisupport-docopyto.md), [Имаписуппорт:: CopyFolder](imapisupport-copyfolder.md)и [имаписуппорт:: копимессажес](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="c7446-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="c7446-112">[IMessage::D елетеаттач](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="c7446-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="c7446-113">[Иабконтаинер:: копентриес](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="c7446-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="c7446-114">Чтобы отобразить индикатор хода выполнения, MAPI определяет объект хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="c7446-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="c7446-115">Объекты хода выполнения реализуют интерфейс [IMAPIProgress: IUnknown](imapiprogressiunknown.md) , интерфейс, который включает методы для установки диапазона индикатора и создания отображения.</span><span class="sxs-lookup"><span data-stu-id="c7446-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="c7446-116">MAPI предоставляет реализацию объекта Progress, как и некоторые клиенты.</span><span class="sxs-lookup"><span data-stu-id="c7446-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="c7446-117">Следует использовать реализацию клиента, если она предоставляется в качестве входного параметра для метода, выполняющего операцию.</span><span class="sxs-lookup"><span data-stu-id="c7446-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="c7446-118">Если клиент передает значение NULL, а не указатель на объект Progress, используйте реализацию MAPI, вызвав метод [имаписуппорт::D опрогрессдиалог](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="c7446-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c7446-119">См. также</span><span class="sxs-lookup"><span data-stu-id="c7446-119">See also</span></span>



[<span data-ttu-id="c7446-120">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="c7446-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

