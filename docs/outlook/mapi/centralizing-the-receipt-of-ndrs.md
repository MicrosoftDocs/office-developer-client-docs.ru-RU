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
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="3a46d-103">Централизация получения отчетов о недоставке</span><span class="sxs-lookup"><span data-stu-id="3a46d-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="3a46d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a46d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a46d-105">**Чтобы отчеты о ненастройке (NDRs) поступают в центральное расположение при одновременном запуске нескольких экземпляров клиента**</span><span class="sxs-lookup"><span data-stu-id="3a46d-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="3a46d-106">Установите **PR_REPORT_ENTRYID** ([PidTagReportEntryId),](pidtagreportentryid-canonical-property.md) **PR_REPORT_NAME** ([PidTagReportName)](pidtagreportname-canonical-property.md)и **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey)](pidtagreportsearchkey-canonical-property.md)соответствующими значениями для учетной записи, которая будет получать отчеты.</span><span class="sxs-lookup"><span data-stu-id="3a46d-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="3a46d-107">При необходимости создайте идентификатор записи, вызывая [IAddrBook::CreateOneOff.](iaddrbook-createoneoff.md)</span><span class="sxs-lookup"><span data-stu-id="3a46d-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="3a46d-108">Необходимо понимать, что существуют системы обмена сообщениями, которые будут игнорировать учетную запись, запрашиваемую для отчетов, и отправлять их отправителю.</span><span class="sxs-lookup"><span data-stu-id="3a46d-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="3a46d-109">Уменьшите влияние этого на администраторов, которые должны будут перемещать отчеты, с помощью:</span><span class="sxs-lookup"><span data-stu-id="3a46d-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="3a46d-110">Предоставление исходному сообщению отдельного класса сообщения, например IPM. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="3a46d-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="3a46d-111">Найди входящие сообщения с классом Report.IPM.Note.MSNNews.NDR и переадрейте их в учетную запись, в которая вы собирались отправлять отчеты.</span><span class="sxs-lookup"><span data-stu-id="3a46d-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="3a46d-112">В то же время отправьте сообщение электронной почты в систему обмена сообщениями, которая  проигнорировала вашу учетную запись отчета о ненастройстве, чтобы сообщить о том, что она должна учитывать PR_REPORT_ENTRYID сообщений.</span><span class="sxs-lookup"><span data-stu-id="3a46d-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="3a46d-113">Большинство систем обмена сообщениями, которые не **PR_REPORT_ENTRYID,** также не будут соблюдать соглашения о классах сообщений MAPI.</span><span class="sxs-lookup"><span data-stu-id="3a46d-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="3a46d-114">Таким образом, вы получите что-то, похожее на заметку.</span><span class="sxs-lookup"><span data-stu-id="3a46d-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="3a46d-115">Это немного сложнее, так как входные данные очень переменные.</span><span class="sxs-lookup"><span data-stu-id="3a46d-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="3a46d-116">Посмотрите на тему и переназначите ее, если вы нашли что-то из списка слов, которые означают "неудаваемые" или что-то из исходной темы.</span><span class="sxs-lookup"><span data-stu-id="3a46d-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="3a46d-117">Будьте готовы со временем настраивать эти списки.</span><span class="sxs-lookup"><span data-stu-id="3a46d-117">Be prepared to tune these lists over time.</span></span> 
    

