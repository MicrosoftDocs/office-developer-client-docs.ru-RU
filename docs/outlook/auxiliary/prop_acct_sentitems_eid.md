---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Представляет идентификатор папки по умолчанию для отправленных элементов для учетной записи.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431843"
---
# <a name="prop_acct_sentitems_eid"></a><span data-ttu-id="78720-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="78720-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="78720-104">Представляет идентификатор папки по умолчанию для отправленных элементов для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="78720-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="78720-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="78720-105">Quick info</span></span>

<span data-ttu-id="78720-106">Обратитесь к разделу [иолкаккаунт](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="78720-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78720-107">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="78720-107">Identifier:</span></span>  <br/> |<span data-ttu-id="78720-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="78720-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="78720-109">Тип свойства:</span><span class="sxs-lookup"><span data-stu-id="78720-109">Property type:</span></span>  <br/> |<span data-ttu-id="78720-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="78720-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="78720-111">Тег свойства:</span><span class="sxs-lookup"><span data-stu-id="78720-111">Property tag:</span></span>  <br/> |<span data-ttu-id="78720-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="78720-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="78720-113">Обращения</span><span class="sxs-lookup"><span data-stu-id="78720-113">Access:</span></span>  <br/> |<span data-ttu-id="78720-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="78720-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78720-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="78720-115">Remarks</span></span>

<span data-ttu-id="78720-116">Получить это свойство можно с помощью [иолкаккаунт::/Prop](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="78720-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="78720-117">Папкой по умолчанию для отправленных элементов **отправляются элементы**.</span><span class="sxs-lookup"><span data-stu-id="78720-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="78720-118">Это свойство доступно только для чтения для учетных записей POP3 и IMAP.</span><span class="sxs-lookup"><span data-stu-id="78720-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="78720-119">При попытке задать это свойство для этих типов учетных записей возвращается **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="78720-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

