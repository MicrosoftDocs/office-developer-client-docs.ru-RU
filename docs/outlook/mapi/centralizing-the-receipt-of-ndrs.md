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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332664"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="6937c-103">Централизация получения отчетов о недоставке</span><span class="sxs-lookup"><span data-stu-id="6937c-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="6937c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6937c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6937c-105">**Получение отчетов о недоставке (NDR) в центральном расположении, когда несколько экземпляров клиента одновременно работают.**</span><span class="sxs-lookup"><span data-stu-id="6937c-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="6937c-106">Set **пр_репорт_ентрид** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **Пр_репорт_наме** ([PidTagReportName](pidtagreportname-canonical-property.md)) и **пр_репорт_сеарч_кэй** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) в соответствующие значения для учетной записи, которая должна быть получена отчеты.</span><span class="sxs-lookup"><span data-stu-id="6937c-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="6937c-107">Создайте идентификатор записи, вызвав [IAddrBook:: креатеонеофф](iaddrbook-createoneoff.md) при необходимости.</span><span class="sxs-lookup"><span data-stu-id="6937c-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="6937c-108">Узнайте, что существуют системы обмена сообщениями, которые будут игнорировать учетную запись, запрошенную для отчетов, и отправить их инициатору.</span><span class="sxs-lookup"><span data-stu-id="6937c-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="6937c-109">Уменьшите влияние, которое повлияет на администраторов, которым потребуется переместить отчеты, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6937c-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="6937c-110">Предоставление исходному сообщению уникального класса сообщений, например IPM. Note. Мснневс.</span><span class="sxs-lookup"><span data-stu-id="6937c-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="6937c-111">Искать входящие сообщения с помощью класса Report. IPM. Note. Мснневс. NDR и пересылать их в учетную запись, к которой вы предслали отчеты.</span><span class="sxs-lookup"><span data-stu-id="6937c-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="6937c-112">В то же время отправьте сообщение электронной почты в систему обмена сообщениями, которое проигнорировало учетную запись отчета о недоставке, чтобы сообщить, что он должен учитывать свойство **пр_репорт_ентрид** .</span><span class="sxs-lookup"><span data-stu-id="6937c-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="6937c-113">Большинство систем обмена сообщениями, в которых не учитывается **пр_репорт_ентрид** , не соблюдается соглашение о классе сообщений MAPI либо.</span><span class="sxs-lookup"><span data-stu-id="6937c-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="6937c-114">Таким образом, вы получите нечто вроде заметки.</span><span class="sxs-lookup"><span data-stu-id="6937c-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="6937c-115">Это немного сложнее, так как входные данные — это такая переменная.</span><span class="sxs-lookup"><span data-stu-id="6937c-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="6937c-116">ВзГляните на тему и перешлите ее, если вы нашли что-либо из списка слов, означающих "не удается доставить", или что-либо из исходной темы.</span><span class="sxs-lookup"><span data-stu-id="6937c-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="6937c-117">Будьте готовы к настройке этих списков с течением времени.</span><span class="sxs-lookup"><span data-stu-id="6937c-117">Be prepared to tune these lists over time.</span></span> 
    

