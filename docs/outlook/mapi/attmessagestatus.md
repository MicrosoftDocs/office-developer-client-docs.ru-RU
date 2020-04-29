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
ms.openlocfilehash: d4dc72309ff090317b2353cab0b4fc2c5be41181
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430317"
---
# <a name="attmessagestatus"></a><span data-ttu-id="2c511-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="2c511-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="2c511-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c511-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c511-105">Флаги сообщений MAPI сопоставляются с флагами TNEF для сохранения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="2c511-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="2c511-106">Все флаги группируются и кодируются в одном байте.</span><span class="sxs-lookup"><span data-stu-id="2c511-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="2c511-107">Используются следующие сопоставления:</span><span class="sxs-lookup"><span data-stu-id="2c511-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="2c511-108">**Флаги сообщений MAPI**</span><span class="sxs-lookup"><span data-stu-id="2c511-108">**MAPI message flags**</span></span>|<span data-ttu-id="2c511-109">**Флаги TNEF**</span><span class="sxs-lookup"><span data-stu-id="2c511-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2c511-110">MSGFLAG_READ</span><span class="sxs-lookup"><span data-stu-id="2c511-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="2c511-111">фмсреад</span><span class="sxs-lookup"><span data-stu-id="2c511-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="2c511-112">MSGFLAG_UNMODIFED</span><span class="sxs-lookup"><span data-stu-id="2c511-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="2c511-113">~ Фмсмодифиед</span><span class="sxs-lookup"><span data-stu-id="2c511-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="2c511-114">MSGFLAG_SUBMIT</span><span class="sxs-lookup"><span data-stu-id="2c511-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="2c511-115">фмссубмиттед</span><span class="sxs-lookup"><span data-stu-id="2c511-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="2c511-116">MSGFLAG_HASATTACH</span><span class="sxs-lookup"><span data-stu-id="2c511-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="2c511-117">фмшасаттач</span><span class="sxs-lookup"><span data-stu-id="2c511-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="2c511-118">MSGFLAG_UNSENT</span><span class="sxs-lookup"><span data-stu-id="2c511-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="2c511-119">фмслокал</span><span class="sxs-lookup"><span data-stu-id="2c511-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="2c511-120">Эти флаги определены в формате TNEF. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="2c511-120">These flags are defined in the TNEF.H header file.</span></span>
  

