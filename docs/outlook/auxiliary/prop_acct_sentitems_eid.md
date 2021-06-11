---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Представляет ID записи папки по умолчанию для отправленных элементов для учетной записи.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431843"
---
# <a name="prop_acct_sentitems_eid"></a><span data-ttu-id="bb7a0-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="bb7a0-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="bb7a0-104">Представляет ID записи папки по умолчанию для отправленных элементов для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="bb7a0-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bb7a0-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bb7a0-105">Quick info</span></span>

<span data-ttu-id="bb7a0-106">См. [iOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="bb7a0-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb7a0-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="bb7a0-107">Identifier:</span></span>  <br/> |<span data-ttu-id="bb7a0-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="bb7a0-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="bb7a0-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="bb7a0-109">Property type:</span></span>  <br/> |<span data-ttu-id="bb7a0-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="bb7a0-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="bb7a0-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="bb7a0-111">Property tag:</span></span>  <br/> |<span data-ttu-id="bb7a0-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="bb7a0-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="bb7a0-113">Доступ:</span><span class="sxs-lookup"><span data-stu-id="bb7a0-113">Access:</span></span>  <br/> |<span data-ttu-id="bb7a0-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="bb7a0-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb7a0-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="bb7a0-115">Remarks</span></span>

<span data-ttu-id="bb7a0-116">Получите это свойство с помощью [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="bb7a0-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="bb7a0-117">Папка по умолчанию для отправленных элементов — **отправленные элементы.**</span><span class="sxs-lookup"><span data-stu-id="bb7a0-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="bb7a0-118">Это свойство только для чтения для учетных записей POP3 и IMAP.</span><span class="sxs-lookup"><span data-stu-id="bb7a0-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="bb7a0-119">Попытка установить это свойство для этих типов учетных записей возвращает **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="bb7a0-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

