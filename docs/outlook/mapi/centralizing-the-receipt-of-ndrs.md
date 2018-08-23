---
title: Централизация уведомление о недоставке
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579440"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="044e3-103">Централизация уведомление о недоставке</span><span class="sxs-lookup"><span data-stu-id="044e3-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="044e3-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="044e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="044e3-105">**Чтобы отчет о недоставке (NDR) получения централизованно при одновременном запуске нескольких экземпляров клиента**</span><span class="sxs-lookup"><span data-stu-id="044e3-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="044e3-106">Задайте подходящие значения для учетной записи, которая должна получить **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) и **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) отчеты.</span><span class="sxs-lookup"><span data-stu-id="044e3-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="044e3-107">Создайте идентификатор записи путем вызова [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) , если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="044e3-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="044e3-108">Понимать, что систем обмена сообщениями, которые будет игнорировать учетной записи запросили для отчетов и отправлять их в инициатором.</span><span class="sxs-lookup"><span data-stu-id="044e3-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="044e3-109">Уменьшите влияние это оказывает на администраторов, которые для перемещения отчетов по:</span><span class="sxs-lookup"><span data-stu-id="044e3-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="044e3-110">Давая класс четкие сообщения, такие как IPM исходного сообщения. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="044e3-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="044e3-111">Выполните поиск входящих сообщений с помощью класса Report.IPM.Note.MSNNews.NDR и пересылать их на учетную запись, которая предназначены отчеты будто.</span><span class="sxs-lookup"><span data-stu-id="044e3-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="044e3-112">В то же время отправки электронной почты в систему обмена сообщениями, который обрабатывается свою учетную запись отчет о недоставке сообщать, что его следует принять свойство **PR_REPORT_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="044e3-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="044e3-113">Системы наиболее обмена сообщениями, которые не учитывают **PR_REPORT_ENTRYID** не будет поддерживать условные обозначения класс сообщения MAPI либо.</span><span class="sxs-lookup"><span data-stu-id="044e3-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="044e3-114">Таким образом вы получите выглядеть, как показано Примечание.</span><span class="sxs-lookup"><span data-stu-id="044e3-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="044e3-115">Это немного сложнее для смягчения последствий, так как входные данные поэтому переменной.</span><span class="sxs-lookup"><span data-stu-id="044e3-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="044e3-116">Проверьте тему и пересылать его, если либо что-то из списка слов, значит «Недоставленное» или что-то из исходного темы.</span><span class="sxs-lookup"><span data-stu-id="044e3-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="044e3-117">Будьте готовым для настройки таких списков по времени.</span><span class="sxs-lookup"><span data-stu-id="044e3-117">Be prepared to tune these lists over time.</span></span> 
    

