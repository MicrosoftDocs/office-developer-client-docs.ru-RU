---
title: attMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8f55470a-65b3-4210-a7d2-9031cb17ca80
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 158e4db4b0f80b80385e85c8afa16fa515dc61b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808098"
---
# <a name="attmessagestatus"></a><span data-ttu-id="54381-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="54381-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="54381-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="54381-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="54381-105">Отметки сообщений MAPI, сопоставляются с флаги TNEF для поддержки обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="54381-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="54381-106">Все флаги объединять и кодируются в один байт.</span><span class="sxs-lookup"><span data-stu-id="54381-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="54381-107">Сопоставления, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="54381-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="54381-108">**Отметки сообщений MAPI**</span><span class="sxs-lookup"><span data-stu-id="54381-108">**MAPI message flags**</span></span>|<span data-ttu-id="54381-109">**Флаги TNEF**</span><span class="sxs-lookup"><span data-stu-id="54381-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54381-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="54381-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="54381-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="54381-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="54381-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="54381-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="54381-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="54381-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="54381-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="54381-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="54381-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="54381-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="54381-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="54381-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="54381-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="54381-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="54381-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="54381-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="54381-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="54381-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="54381-120">Эти параметры определены в формате TNEF. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="54381-120">These flags are defined in the TNEF.H header file.</span></span>
  

