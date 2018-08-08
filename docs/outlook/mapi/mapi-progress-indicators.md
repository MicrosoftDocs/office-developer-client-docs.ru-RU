---
title: Индикаторы выполнения MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8af2ba3067dabe759056313eb278b9901510980
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809797"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="86fcd-103">Индикаторы выполнения MAPI</span><span class="sxs-lookup"><span data-stu-id="86fcd-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="86fcd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="86fcd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="86fcd-105">Многие из операций, выполняемых для клиентов, может занять много времени.</span><span class="sxs-lookup"><span data-stu-id="86fcd-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="86fcd-106">Информирование клиентов о ходе выполнения длительной операции, можно отобразить индикатор, который отображает графическое по завершении работы часть операции в данный момент от начала операции до его завершения.</span><span class="sxs-lookup"><span data-stu-id="86fcd-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="86fcd-107">Индикатор показывает процент завершения общее операции.</span><span class="sxs-lookup"><span data-stu-id="86fcd-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="86fcd-108">Следующие методы поддерживают длительных операций и отображение индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="86fcd-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="86fcd-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)и [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="86fcd-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="86fcd-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) и [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="86fcd-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="86fcd-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)и [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="86fcd-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="86fcd-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="86fcd-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="86fcd-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="86fcd-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="86fcd-114">Чтобы отобразить индикатор выполнения, MAPI определяет объект хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="86fcd-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="86fcd-115">Объекты хода выполнения реализовать [IMAPIProgress: IUnknown](imapiprogressiunknown.md) интерфейса, интерфейс, который содержит методы для создания диапазона индикатора и создание отображения.</span><span class="sxs-lookup"><span data-stu-id="86fcd-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="86fcd-116">MAPI предоставляет реализацию объекта о ходе выполнения, как и некоторыми клиентами.</span><span class="sxs-lookup"><span data-stu-id="86fcd-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="86fcd-117">Реализация клиента, следует использовать, если оно предоставлено, как входного параметра для метода для выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="86fcd-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="86fcd-118">Если клиент передает значение NULL вместо указателя на объект ход выполнения, описание использования реализации интерфейса MAPI путем вызова метода [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="86fcd-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="86fcd-119">См. также</span><span class="sxs-lookup"><span data-stu-id="86fcd-119">See also</span></span>



[<span data-ttu-id="86fcd-120">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="86fcd-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

