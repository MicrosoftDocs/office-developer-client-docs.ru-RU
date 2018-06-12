---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Указывает тип шифрованного подключения для учетной записи SMTP.
ms.openlocfilehash: e1c8c8dacf953407d4cbb114aa5ee0a4cdb6acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807956"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="60f71-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="60f71-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="60f71-104">Указывает тип шифрованного подключения для учетной записи SMTP.</span><span class="sxs-lookup"><span data-stu-id="60f71-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="60f71-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="60f71-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="60f71-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="60f71-106">Identifier:</span></span>  <br/> |<span data-ttu-id="60f71-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="60f71-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="60f71-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="60f71-108">Property type:</span></span>  <br/> |<span data-ttu-id="60f71-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="60f71-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="60f71-110">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="60f71-110">Property tag:</span></span>  <br/> |<span data-ttu-id="60f71-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="60f71-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="60f71-112">Access:</span><span class="sxs-lookup"><span data-stu-id="60f71-112">Access:</span></span>  <br/> |<span data-ttu-id="60f71-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="60f71-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60f71-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="60f71-114">Remarks</span></span>

<span data-ttu-id="60f71-115">Значение может быть одна из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="60f71-115">The value can be one of the following constants.</span></span> <span data-ttu-id="60f71-116">В разделе [константы (Управление учетными записями API)](constants-account-management-api.md) их значения.</span><span class="sxs-lookup"><span data-stu-id="60f71-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="60f71-117">**Константы**</span><span class="sxs-lookup"><span data-stu-id="60f71-117">**Constants**</span></span>|<span data-ttu-id="60f71-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="60f71-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="60f71-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="60f71-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="60f71-120">Не используйте любой шифрования.</span><span class="sxs-lookup"><span data-stu-id="60f71-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="60f71-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="60f71-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="60f71-122">Используйте шифрование Secure сокетов (SSL).</span><span class="sxs-lookup"><span data-stu-id="60f71-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="60f71-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="60f71-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="60f71-124">Используйте протокол проверки подлинности и шифрования безопасности TLS (Transport Layer).</span><span class="sxs-lookup"><span data-stu-id="60f71-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="60f71-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="60f71-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="60f71-126">Автоматическое определение и использование метода шифрования, поддерживаемые почтовым сервером.</span><span class="sxs-lookup"><span data-stu-id="60f71-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="60f71-127">См. также</span><span class="sxs-lookup"><span data-stu-id="60f71-127">See also</span></span>

- [<span data-ttu-id="60f71-128">Загружаемые файлы для управления сообщения для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="60f71-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="60f71-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="60f71-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

