---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Представляет идентификатор записи папки по умолчанию для отправленных элементов для учетной записи.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807936"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="3b5f8-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="3b5f8-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="3b5f8-104">Представляет идентификатор записи папки по умолчанию для отправленных элементов для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3b5f8-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3b5f8-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3b5f8-105">Quick info</span></span>

<span data-ttu-id="3b5f8-106">В разделе [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="3b5f8-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b5f8-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="3b5f8-107">Identifier:</span></span>  <br/> |<span data-ttu-id="3b5f8-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="3b5f8-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="3b5f8-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="3b5f8-109">Property type:</span></span>  <br/> |<span data-ttu-id="3b5f8-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3b5f8-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3b5f8-111">Свойство tag:</span><span class="sxs-lookup"><span data-stu-id="3b5f8-111">Property tag:</span></span>  <br/> |<span data-ttu-id="3b5f8-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="3b5f8-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="3b5f8-113">Access:</span><span class="sxs-lookup"><span data-stu-id="3b5f8-113">Access:</span></span>  <br/> |<span data-ttu-id="3b5f8-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3b5f8-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b5f8-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="3b5f8-115">Remarks</span></span>

<span data-ttu-id="3b5f8-116">Получение этого свойства с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="3b5f8-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="3b5f8-117">Папка по умолчанию для отправленных элементов — **Отправленные**.</span><span class="sxs-lookup"><span data-stu-id="3b5f8-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="3b5f8-118">Это свойство доступно только для чтения учетных записей POP3 и IMAP.</span><span class="sxs-lookup"><span data-stu-id="3b5f8-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="3b5f8-119">При попытке установить это свойство для следующих типов учетных записей возвращает **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="3b5f8-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

