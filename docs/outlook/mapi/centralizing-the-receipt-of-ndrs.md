---
title: Централизация получения отчетов о недоставке
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405858"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="a90c6-103">Централизация получения отчетов о недоставке</span><span class="sxs-lookup"><span data-stu-id="a90c6-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="a90c6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a90c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a90c6-105">**Чтобы отчеты о несделательности (NDRs) прибыли в центральное расположение при одновременном запуске нескольких экземпляров клиента**</span><span class="sxs-lookup"><span data-stu-id="a90c6-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="a90c6-106">Установите **PR_REPORT_ENTRYID** [(PidTagReportEntryId),](pidtagreportentryid-canonical-property.md) **PR_REPORT_NAME** [(PidTagReportName)](pidtagreportname-canonical-property.md)и **PR_REPORT_SEARCH_KEY** [(PidTagReportSearchKey)](pidtagreportsearchkey-canonical-property.md)к соответствующим значениям для учетной записи, которая будет получать отчеты.</span><span class="sxs-lookup"><span data-stu-id="a90c6-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="a90c6-107">Создайте идентификатор входа, позвонив [в IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a90c6-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="a90c6-108">Поймите, что существуют системы обмена сообщениями, которые будут игнорировать запрашиваемую учетную запись для отчетов и отправлять их в отправитель.</span><span class="sxs-lookup"><span data-stu-id="a90c6-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="a90c6-109">Уменьшите влияние, которое это будет иметь на администраторов, которые должны будут перемещать отчеты по:</span><span class="sxs-lookup"><span data-stu-id="a90c6-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="a90c6-110">Предоставление исходного сообщения определенного класса сообщений, например IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="a90c6-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="a90c6-111">Найди входящие сообщения с классом Report.IPM.Note.MSNNews.NDR и переадектуй их в учетную запись, в которая должны прийти отчеты.</span><span class="sxs-lookup"><span data-stu-id="a90c6-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="a90c6-112">В то же время отправьте сообщение электронной почты в систему обмена сообщениями, которая  проигнорировала вашу учетную запись отчета о неделивстве, чтобы сообщить, что она должна соблюдать PR_REPORT_ENTRYID.</span><span class="sxs-lookup"><span data-stu-id="a90c6-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="a90c6-113">Большинство систем обмена сообщениями, которые не **PR_REPORT_ENTRYID,** также не будут соблюдать конвенции класса сообщений MAPI.</span><span class="sxs-lookup"><span data-stu-id="a90c6-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="a90c6-114">Поэтому вы получите что-то похожее на заметку.</span><span class="sxs-lookup"><span data-stu-id="a90c6-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="a90c6-115">С этим немного сложнее, так как вход настолько переменная.</span><span class="sxs-lookup"><span data-stu-id="a90c6-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="a90c6-116">Посмотрите на объект и переадектуйте его, если вы найдете что-то из списка слов, которые означают "недостижимый", или что-то из исходного субъекта.</span><span class="sxs-lookup"><span data-stu-id="a90c6-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="a90c6-117">Будьте готовы со временем настроить эти списки.</span><span class="sxs-lookup"><span data-stu-id="a90c6-117">Be prepared to tune these lists over time.</span></span> 
    

