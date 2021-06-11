---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Указывает метод проверки подлинности для учетной записи SMTP.
ms.openlocfilehash: bb5adeb1fe73ed8b7ab69ca584215b44e1a9e4b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434643"
---
# <a name="prop_smtp_auth_method"></a><span data-ttu-id="e7ed2-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="e7ed2-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="e7ed2-104">Указывает метод проверки подлинности для учетной записи SMTP.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e7ed2-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="e7ed2-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e7ed2-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e7ed2-106">Identifier:</span></span>  <br/> |<span data-ttu-id="e7ed2-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="e7ed2-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="e7ed2-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="e7ed2-108">Property type:</span></span>  <br/> |<span data-ttu-id="e7ed2-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="e7ed2-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="e7ed2-110">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="e7ed2-110">Property tag:</span></span>  <br/> |<span data-ttu-id="e7ed2-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="e7ed2-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="e7ed2-112">Доступ:</span><span class="sxs-lookup"><span data-stu-id="e7ed2-112">Access:</span></span>  <br/> |<span data-ttu-id="e7ed2-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e7ed2-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7ed2-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e7ed2-114">Remarks</span></span>

<span data-ttu-id="e7ed2-115">Значение — битмаска следующих констант.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="e7ed2-116">См. [константы (API управления](constants-account-management-api.md) учетной записью) для их значений.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="e7ed2-117">**SMTP_AUTH_SAME_AS_POP** означает использование тех же учетных данных, что и [](prop_inet_user.md) мой входящий почтовый сервер, как PROP_INET_USER [и PROP_INET_PASSWORD.](prop_inet_password.md)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="e7ed2-118">**SMTP_AUTH_USER_PASS** означает использование учетных данных, предоставляемых [PROP_SMTP_USER](prop_smtp_user.md) и [PROP_SMTP_PASSWORD.](prop_smtp_password.md)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="e7ed2-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** означает, что перед отправкой почты пользователь должен войти на входящий почтовый сервер.</span><span class="sxs-lookup"><span data-stu-id="e7ed2-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e7ed2-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e7ed2-120">See also</span></span>

- [<span data-ttu-id="e7ed2-121">Управление скачиванием сообщений для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="e7ed2-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="e7ed2-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="e7ed2-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

