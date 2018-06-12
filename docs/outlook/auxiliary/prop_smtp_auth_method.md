---
title: PROP_SMTP_AUTH_METHOD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 4202cafc-9011-406d-90b3-8dabf531c90b
description: Указывает метод проверки подлинности для учетной записи SMTP.
ms.openlocfilehash: 0c52f1eeca8f7ac3e63cccf712dd672c2247be6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807960"
---
# <a name="propsmtpauthmethod"></a><span data-ttu-id="dd6df-103">PROP_SMTP_AUTH_METHOD</span><span class="sxs-lookup"><span data-stu-id="dd6df-103">PROP_SMTP_AUTH_METHOD</span></span>

<span data-ttu-id="dd6df-104">Указывает метод проверки подлинности для учетной записи SMTP.</span><span class="sxs-lookup"><span data-stu-id="dd6df-104">Specifies the authentication method to use for the SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dd6df-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="dd6df-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dd6df-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="dd6df-106">Identifier:</span></span>  <br/> |<span data-ttu-id="dd6df-107">0x0208</span><span class="sxs-lookup"><span data-stu-id="dd6df-107">0x0208</span></span>  <br/> |
|<span data-ttu-id="dd6df-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="dd6df-108">Property type:</span></span>  <br/> |<span data-ttu-id="dd6df-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="dd6df-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="dd6df-110">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="dd6df-110">Property tag:</span></span>  <br/> |<span data-ttu-id="dd6df-111">0x02080003</span><span class="sxs-lookup"><span data-stu-id="dd6df-111">0x02080003</span></span>  <br/> |
|<span data-ttu-id="dd6df-112">Access:</span><span class="sxs-lookup"><span data-stu-id="dd6df-112">Access:</span></span>  <br/> |<span data-ttu-id="dd6df-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="dd6df-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd6df-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="dd6df-114">Remarks</span></span>

<span data-ttu-id="dd6df-115">Значение является битовой маской из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="dd6df-115">The value is a bitmask of the following constants.</span></span> <span data-ttu-id="dd6df-116">В разделе [константы (Управление учетными записями API)](constants-account-management-api.md) их значения.</span><span class="sxs-lookup"><span data-stu-id="dd6df-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
- <span data-ttu-id="dd6df-117">**SMTP_AUTH_SAME_AS_POP** означает, что использование один набор учетных данных в качестве сервера входящих сообщений, предоставляемый [PROP_INET_USER](prop_inet_user.md) и [PROP_INET_PASSWORD](prop_inet_password.md).</span><span class="sxs-lookup"><span data-stu-id="dd6df-117">**SMTP_AUTH_SAME_AS_POP** means using the same credentials as my incoming mail server, as provided by [PROP_INET_USER](prop_inet_user.md) and [PROP_INET_PASSWORD](prop_inet_password.md).</span></span>
    
- <span data-ttu-id="dd6df-118">**SMTP_AUTH_USER_PASS** означает, что с помощью учетных данных, как автор [PROP_SMTP_USER](prop_smtp_user.md) и [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span><span class="sxs-lookup"><span data-stu-id="dd6df-118">**SMTP_AUTH_USER_PASS** means using the credentials as provided by [PROP_SMTP_USER](prop_smtp_user.md) and [PROP_SMTP_PASSWORD](prop_smtp_password.md).</span></span>
    
- <span data-ttu-id="dd6df-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** означает, что разрешения на запрос пользователя для входа на сервер входящей почты перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="dd6df-119">**SMTP_AUTH_RECEIVE_BEFORE_SEND** means requesting the user to log on to the incoming mail server before sending mail.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="dd6df-120">См. также</span><span class="sxs-lookup"><span data-stu-id="dd6df-120">See also</span></span>

- [<span data-ttu-id="dd6df-121">Загружаемые файлы для управления сообщения для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="dd6df-121">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md)  
- [<span data-ttu-id="dd6df-122">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="dd6df-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

