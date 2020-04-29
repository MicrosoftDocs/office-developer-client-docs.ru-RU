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
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="34e72-103">Централизация получения отчетов о недоставке</span><span class="sxs-lookup"><span data-stu-id="34e72-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="34e72-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34e72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34e72-105">**Получение отчетов о недоставке (NDR) в центральном расположении, когда несколько экземпляров клиента одновременно работают.**</span><span class="sxs-lookup"><span data-stu-id="34e72-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="34e72-106">Установите **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) и **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) в соответствующие значения для учетной записи, которая должна получать отчеты.</span><span class="sxs-lookup"><span data-stu-id="34e72-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="34e72-107">Создайте идентификатор записи, вызвав [IAddrBook:: креатеонеофф](iaddrbook-createoneoff.md) при необходимости.</span><span class="sxs-lookup"><span data-stu-id="34e72-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="34e72-108">Узнайте, что существуют системы обмена сообщениями, которые будут игнорировать учетную запись, запрошенную для отчетов, и отправить их инициатору.</span><span class="sxs-lookup"><span data-stu-id="34e72-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="34e72-109">Уменьшите влияние, которое повлияет на администраторов, которым потребуется переместить отчеты, выполнив следующие действия:</span><span class="sxs-lookup"><span data-stu-id="34e72-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="34e72-110">Предоставление исходному сообщению уникального класса сообщений, например IPM. Note. Мснневс.</span><span class="sxs-lookup"><span data-stu-id="34e72-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="34e72-111">Искать входящие сообщения с помощью класса Report. IPM. Note. Мснневс. NDR и пересылать их в учетную запись, к которой вы предслали отчеты.</span><span class="sxs-lookup"><span data-stu-id="34e72-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="34e72-112">В то же время отправьте сообщение электронной почты в систему обмена сообщениями, которое проигнорировало учетную запись отчета о недоставке, чтобы сообщить, что он должен учитывать свойство **PR_REPORT_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="34e72-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="34e72-113">Большинство систем обмена сообщениями, которые не поддерживают **PR_REPORT_ENTRYID** , не учитывают соглашения о классе сообщений MAPI либо.</span><span class="sxs-lookup"><span data-stu-id="34e72-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="34e72-114">Таким образом, вы получите нечто вроде заметки.</span><span class="sxs-lookup"><span data-stu-id="34e72-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="34e72-115">Это немного сложнее, так как входные данные — это такая переменная.</span><span class="sxs-lookup"><span data-stu-id="34e72-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="34e72-116">Взгляните на тему и перешлите ее, если вы нашли что-либо из списка слов, означающих "не удается доставить", или что-либо из исходной темы.</span><span class="sxs-lookup"><span data-stu-id="34e72-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="34e72-117">Будьте готовы к настройке этих списков с течением времени.</span><span class="sxs-lookup"><span data-stu-id="34e72-117">Be prepared to tune these lists over time.</span></span> 
    

