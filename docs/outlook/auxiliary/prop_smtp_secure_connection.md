---
title: PROP_SMTP_SECURE_CONNECTION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: e316a424-d789-4ce5-bcc6-263049f3659e
description: Указывает тип зашифрованного подключения, используемого для учетной записи SMTP.
ms.openlocfilehash: 67eae5c9c5ca1b7f664ceaac0463ef3f3c9a291a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421286"
---
# <a name="prop_smtp_secure_connection"></a><span data-ttu-id="bc197-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="bc197-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="bc197-104">Указывает тип зашифрованного подключения, используемого для учетной записи SMTP.</span><span class="sxs-lookup"><span data-stu-id="bc197-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="bc197-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bc197-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bc197-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bc197-106">Identifier:</span></span>  <br/> |<span data-ttu-id="bc197-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="bc197-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="bc197-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="bc197-108">Property type:</span></span>  <br/> |<span data-ttu-id="bc197-109">PT_DWORD</span><span class="sxs-lookup"><span data-stu-id="bc197-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="bc197-110">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="bc197-110">Property tag:</span></span>  <br/> |<span data-ttu-id="bc197-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="bc197-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="bc197-112">Обращения</span><span class="sxs-lookup"><span data-stu-id="bc197-112">Access:</span></span>  <br/> |<span data-ttu-id="bc197-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bc197-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc197-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="bc197-114">Remarks</span></span>

<span data-ttu-id="bc197-115">Значение может быть одной из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="bc197-115">The value can be one of the following constants.</span></span> <span data-ttu-id="bc197-116">В этом разделе приведены [константы (API управления учетными записями)](constants-account-management-api.md) для их значений.</span><span class="sxs-lookup"><span data-stu-id="bc197-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="bc197-117">**Константы**</span><span class="sxs-lookup"><span data-stu-id="bc197-117">**Constants**</span></span>|<span data-ttu-id="bc197-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bc197-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc197-119">**ENCRYPT_CONN_NO_SECURITY**</span><span class="sxs-lookup"><span data-stu-id="bc197-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="bc197-120">Не используйте шифрование.</span><span class="sxs-lookup"><span data-stu-id="bc197-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="bc197-121">**ENCRYPT_CONN_SSL**</span><span class="sxs-lookup"><span data-stu-id="bc197-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="bc197-122">Используйте шифрование SSL.</span><span class="sxs-lookup"><span data-stu-id="bc197-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="bc197-123">**ENCRYPT_CONN_TLS**</span><span class="sxs-lookup"><span data-stu-id="bc197-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="bc197-124">Используйте шифрование TLS и протокол проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="bc197-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="bc197-125">**ENCRYPT_CONN_AUTO**</span><span class="sxs-lookup"><span data-stu-id="bc197-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="bc197-126">Автоматически определять и использовать метод шифрования, поддерживаемый почтовым сервером.</span><span class="sxs-lookup"><span data-stu-id="bc197-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc197-127">См. также</span><span class="sxs-lookup"><span data-stu-id="bc197-127">See also</span></span>

- [<span data-ttu-id="bc197-128">Управление скачиванием сообщений для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="bc197-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="bc197-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="bc197-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

