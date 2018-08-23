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
ms.openlocfilehash: 704707b34fb4532f0e60636df31edbae1a939f35
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565748"
---
# <a name="attmessagestatus"></a><span data-ttu-id="70f3e-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="70f3e-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="70f3e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70f3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70f3e-105">Отметки сообщений MAPI, сопоставляются с флаги TNEF для поддержки обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="70f3e-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="70f3e-106">Все флаги объединять и кодируются в один байт.</span><span class="sxs-lookup"><span data-stu-id="70f3e-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="70f3e-107">Сопоставления, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="70f3e-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="70f3e-108">**Отметки сообщений MAPI**</span><span class="sxs-lookup"><span data-stu-id="70f3e-108">**MAPI message flags**</span></span>|<span data-ttu-id="70f3e-109">**Флаги TNEF**</span><span class="sxs-lookup"><span data-stu-id="70f3e-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="70f3e-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="70f3e-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="70f3e-111">fmsRead</span><span class="sxs-lookup"><span data-stu-id="70f3e-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="70f3e-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="70f3e-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="70f3e-113">~ fmsModified</span><span class="sxs-lookup"><span data-stu-id="70f3e-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="70f3e-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="70f3e-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="70f3e-115">fmsSubmitted</span><span class="sxs-lookup"><span data-stu-id="70f3e-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="70f3e-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="70f3e-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="70f3e-117">fmsHasAttach</span><span class="sxs-lookup"><span data-stu-id="70f3e-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="70f3e-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="70f3e-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="70f3e-119">fmsLocal</span><span class="sxs-lookup"><span data-stu-id="70f3e-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="70f3e-120">Эти параметры определены в формате TNEF. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="70f3e-120">These flags are defined in the TNEF.H header file.</span></span>
  

