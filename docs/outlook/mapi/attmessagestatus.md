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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318216"
---
# <a name="attmessagestatus"></a><span data-ttu-id="d0e28-103">attMessageStatus</span><span class="sxs-lookup"><span data-stu-id="d0e28-103">attMessageStatus</span></span>

  
  
<span data-ttu-id="d0e28-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0e28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0e28-105">Флаги сообщений MAPI сопоставляются с флагами TNEF для сохранения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="d0e28-105">MAPI message flags are mapped to TNEF flags to preserve backward compatibility.</span></span> <span data-ttu-id="d0e28-106">Все флаги группируются и кодируются в одном байте.</span><span class="sxs-lookup"><span data-stu-id="d0e28-106">All the flags are grouped together and encoded in a single byte.</span></span> <span data-ttu-id="d0e28-107">Используются следующие сопоставления:</span><span class="sxs-lookup"><span data-stu-id="d0e28-107">The mappings are as follows:</span></span>
  
|<span data-ttu-id="d0e28-108">**Флаги сообщений MAPI**</span><span class="sxs-lookup"><span data-stu-id="d0e28-108">**MAPI message flags**</span></span>|<span data-ttu-id="d0e28-109">**Флаги TNEF**</span><span class="sxs-lookup"><span data-stu-id="d0e28-109">**TNEF flags**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0e28-110">МСГФЛАГ_РЕАД</span><span class="sxs-lookup"><span data-stu-id="d0e28-110">MSGFLAG_READ</span></span>  <br/> |<span data-ttu-id="d0e28-111">Фмсреад</span><span class="sxs-lookup"><span data-stu-id="d0e28-111">fmsRead</span></span>  <br/> |
|<span data-ttu-id="d0e28-112">МСГФЛАГ_УНМОДИФЕД</span><span class="sxs-lookup"><span data-stu-id="d0e28-112">MSGFLAG_UNMODIFED</span></span>  <br/> |<span data-ttu-id="d0e28-113">~ Фмсмодифиед</span><span class="sxs-lookup"><span data-stu-id="d0e28-113">~fmsModified</span></span>  <br/> |
|<span data-ttu-id="d0e28-114">МСГФЛАГ_СУБМИТ</span><span class="sxs-lookup"><span data-stu-id="d0e28-114">MSGFLAG_SUBMIT</span></span>  <br/> |<span data-ttu-id="d0e28-115">Фмссубмиттед</span><span class="sxs-lookup"><span data-stu-id="d0e28-115">fmsSubmitted</span></span>  <br/> |
|<span data-ttu-id="d0e28-116">МСГФЛАГ_ХАСАТТАЧ</span><span class="sxs-lookup"><span data-stu-id="d0e28-116">MSGFLAG_HASATTACH</span></span>  <br/> |<span data-ttu-id="d0e28-117">Фмшасаттач</span><span class="sxs-lookup"><span data-stu-id="d0e28-117">fmsHasAttach</span></span>  <br/> |
|<span data-ttu-id="d0e28-118">МСГФЛАГ_УНСЕНТ</span><span class="sxs-lookup"><span data-stu-id="d0e28-118">MSGFLAG_UNSENT</span></span>  <br/> |<span data-ttu-id="d0e28-119">Фмслокал</span><span class="sxs-lookup"><span data-stu-id="d0e28-119">fmsLocal</span></span>  <br/> |
   
<span data-ttu-id="d0e28-120">Эти флаги определены в формате TNEF. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="d0e28-120">These flags are defined in the TNEF.H header file.</span></span>
  

