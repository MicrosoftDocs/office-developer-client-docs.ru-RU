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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328331"
---
# <a name="propsmtpsecureconnection"></a><span data-ttu-id="f8804-103">PROP_SMTP_SECURE_CONNECTION</span><span class="sxs-lookup"><span data-stu-id="f8804-103">PROP_SMTP_SECURE_CONNECTION</span></span>

<span data-ttu-id="f8804-104">Указывает тип зашифрованного подключения, используемого для учетной записи SMTP.</span><span class="sxs-lookup"><span data-stu-id="f8804-104">Specifies the type of encrypted connection to use for an SMTP account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f8804-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f8804-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8804-106">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="f8804-106">Identifier:</span></span>  <br/> |<span data-ttu-id="f8804-107">0x020A</span><span class="sxs-lookup"><span data-stu-id="f8804-107">0x020A</span></span>  <br/> |
|<span data-ttu-id="f8804-108">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="f8804-108">Property type:</span></span>  <br/> |<span data-ttu-id="f8804-109">ПТ_ДВОРД</span><span class="sxs-lookup"><span data-stu-id="f8804-109">PT_DWORD</span></span>  <br/> |
|<span data-ttu-id="f8804-110">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="f8804-110">Property tag:</span></span>  <br/> |<span data-ttu-id="f8804-111">0x020A0003</span><span class="sxs-lookup"><span data-stu-id="f8804-111">0x020A0003</span></span>  <br/> |
|<span data-ttu-id="f8804-112">Обращения</span><span class="sxs-lookup"><span data-stu-id="f8804-112">Access:</span></span>  <br/> |<span data-ttu-id="f8804-113">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8804-113">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8804-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f8804-114">Remarks</span></span>

<span data-ttu-id="f8804-115">Значение может быть одной из следующих констант.</span><span class="sxs-lookup"><span data-stu-id="f8804-115">The value can be one of the following constants.</span></span> <span data-ttu-id="f8804-116">В этом разделе приведены [константы (API управления учетНыми записями)](constants-account-management-api.md) для их значений.</span><span class="sxs-lookup"><span data-stu-id="f8804-116">See [Constants (Account management API)](constants-account-management-api.md) for their values.</span></span> 
  
|<span data-ttu-id="f8804-117">**Константы**</span><span class="sxs-lookup"><span data-stu-id="f8804-117">**Constants**</span></span>|<span data-ttu-id="f8804-118">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f8804-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f8804-119">**ЕНКРИПТ_КОНН_НО_СЕКУРИТИ**</span><span class="sxs-lookup"><span data-stu-id="f8804-119">**ENCRYPT_CONN_NO_SECURITY**</span></span> <br/> |<span data-ttu-id="f8804-120">Не используйте шифрование.</span><span class="sxs-lookup"><span data-stu-id="f8804-120">Do not use any encryption.</span></span>  <br/> |
|<span data-ttu-id="f8804-121">**ЕНКРИПТ_КОНН_ССЛ**</span><span class="sxs-lookup"><span data-stu-id="f8804-121">**ENCRYPT_CONN_SSL**</span></span> <br/> |<span data-ttu-id="f8804-122">Используйте шифрование SSL.</span><span class="sxs-lookup"><span data-stu-id="f8804-122">Use Secure Socket Layer (SSL) encryption.</span></span>  <br/> |
|<span data-ttu-id="f8804-123">**ЕНКРИПТ_КОНН_ТЛС**</span><span class="sxs-lookup"><span data-stu-id="f8804-123">**ENCRYPT_CONN_TLS**</span></span> <br/> |<span data-ttu-id="f8804-124">Используйте шифрование TLS и протокол проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f8804-124">Use Transport Layer Security (TLS) encryption and authentication protocol.</span></span>  <br/> |
|<span data-ttu-id="f8804-125">**ЕНКРИПТ_КОНН_АУТО**</span><span class="sxs-lookup"><span data-stu-id="f8804-125">**ENCRYPT_CONN_AUTO**</span></span> <br/> |<span data-ttu-id="f8804-126">Автоматически определять и использовать метод шифрования, поддерживаемый почтовым сервером.</span><span class="sxs-lookup"><span data-stu-id="f8804-126">Automatically detect and use the encryption method supported by the mail server.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8804-127">См. также</span><span class="sxs-lookup"><span data-stu-id="f8804-127">See also</span></span>

- [<span data-ttu-id="f8804-128">Управление скачиванием сообщений для учетных записей POP3</span><span class="sxs-lookup"><span data-stu-id="f8804-128">Managing message downloads for POP3 accounts</span></span>](managing-message-downloads-for-pop3-accounts.md) 
- [<span data-ttu-id="f8804-129">Constants (Account management API)</span><span class="sxs-lookup"><span data-stu-id="f8804-129">Constants (Account management API)</span></span>](constants-account-management-api.md)

