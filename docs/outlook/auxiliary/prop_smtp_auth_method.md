---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Задает способ проверки подлинности, используемый для учетной записи SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326504"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="3e7c0-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="3e7c0-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="3e7c0-104">Задает способ проверки подлинности, используемый для учетной записи SMTP.</span><span class="sxs-lookup"><span data-stu-id="3e7c0-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3e7c0-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3e7c0-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e7c0-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3e7c0-106">Identifier:</span></span>  <br/> |<span data-ttu-id="3e7c0-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="3e7c0-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="3e7c0-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="3e7c0-108">Property type:</span></span>  <br/> |<span data-ttu-id="3e7c0-109">ПТ_ДВОРД</span><span class="sxs-lookup"><span data-stu-id="3e7c0-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="3e7c0-110">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="3e7c0-110">Property tag:</span></span>  <br/> |<span data-ttu-id="3e7c0-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="3e7c0-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="3e7c0-112">Обращения</span><span class="sxs-lookup"><span data-stu-id="3e7c0-112">Access:</span></span>  <br/> |<span data-ttu-id="3e7c0-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3e7c0-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e7c0-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="3e7c0-114">Remarks</span></span>

<span data-ttu-id="3e7c0-115">Значение представляет собой битовую маску для следующих констант.</span><span class="sxs-lookup"><span data-stu-id="3e7c0-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="3e7c0-116">В этом разделе приведены [константы (API управления учетНыми записями)](constants-account-management-api.md) для их значений.</span><span class="sxs-lookup"><span data-stu-id="3e7c0-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="3e7c0-117">**Смтп_аус_саме_ас_поп** означает использование тех же учетных данных, что и мой сервер входящей почты, что предоставляется [проп_инет_усер](prop_inet_user.md) и [проп_инет_пассворд](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="3e7c0-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="3e7c0-118">**Смтп_аус_усер_пасс** означает использование учетных данных, предоставляемых [проп_смтп_усер](prop_smtp_user.md) и [проп_смтп_пассворд](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="3e7c0-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="3e7c0-119">**Смтп_аус_рецеиве_бефоре_сенд** означает, что пользователь должен войти на сервер входящей почты, прежде чем отправлять почту.</span><span class="sxs-lookup"><span data-stu-id="3e7c0-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3e7c0-120">См. также</span><span class="sxs-lookup"><span data-stu-id="3e7c0-120">See also</span></span>

- [<span data-ttu-id="3e7c0-121">Управление скачиванием сообщений для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="3e7c0-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="3e7c0-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="3e7c0-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

