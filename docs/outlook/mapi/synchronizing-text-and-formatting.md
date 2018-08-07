---
title: Синхронизация текста и форматирования
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 40d7a45ab97e0d2f8e9d3db1e1d38eb3bdb75158
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812464"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="4f9a4-103">Синхронизация текста и форматирования</span><span class="sxs-lookup"><span data-stu-id="4f9a4-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="4f9a4-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4f9a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4f9a4-105">Основная проблема при отправке сообщения форматированный текст (RTF) — это поддержание синхронизации с форматирования текста.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="4f9a4-106">Для обеспечения при получении сообщения в место назначения они их авторства предназначен и форматирование текста и синхронизируются, MAPI предоставляет функцию [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="4f9a4-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="4f9a4-107">**RTFSync** обычно вызывается с поддержкой RTF клиентов перед отображением входящих сообщений и диспетчером очереди MAPI, когда загружает сообщения поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="4f9a4-108">Вызывающие задать область возможных несоответствие, передав одним или двумя флаги **RTFSync**:</span><span class="sxs-lookup"><span data-stu-id="4f9a4-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="4f9a4-109">RTF_SYNC_BODY_CHANGED для указания изменения в текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="4f9a4-110">RTF_SYNC_RTF_CHANGED для указания изменения в обычный текст.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="4f9a4-111">Процесс синхронизации, что происходит в **RTFSync** — проверка сложных циклической (контрольной СУММЫ) текста сообщения, игнорирует некоторые символы и преобразовывает другим пользователям.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="4f9a4-112">Символы, вероятнее всего, добавленные поставщиками транспорта игнорируются.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="4f9a4-113">MAPI определяет несколько свойств для работы с RTF, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="4f9a4-114">**Свойство RTF**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-114">**RTF property**</span></span>|<span data-ttu-id="4f9a4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4f9a4-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4f9a4-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f9a4-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4f9a4-117">Указывает начало текста настоящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="4f9a4-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f9a4-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4f9a4-119">Содержит результат проверки циклической текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="4f9a4-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f9a4-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4f9a4-121">Содержит число знаков в **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="4f9a4-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f9a4-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4f9a4-123">Задайте значение TRUE, когда сообщение синхронизированные текста и форматирования.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="4f9a4-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f9a4-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4f9a4-125">Содержит число знаков nonwhitespace, следует ставить перед ним текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="4f9a4-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="4f9a4-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="4f9a4-127">Содержит число знаков nonwhitespace, аудита текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="4f9a4-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

