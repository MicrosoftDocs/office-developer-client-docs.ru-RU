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
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435105"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="530d4-103">Синхронизация текста и форматирования</span><span class="sxs-lookup"><span data-stu-id="530d4-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="530d4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="530d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="530d4-105">Основной задачей при отправке сообщений в формате RTF является синхронизация текста с форматированием.</span><span class="sxs-lookup"><span data-stu-id="530d4-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="530d4-106">Чтобы убедиться, что сообщения, поступающие по адресу назначения, являются их источниками, а также для синхронизации текста и форматирования, MAPI предоставляет функцию [ртфсинк](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="530d4-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="530d4-107">**Ртфсинк** обычно вызывается клиентами, ПОДДЕРЖИВАЮЩими RTF, перед отображением входящих сообщений и диспетчером очереди MAPI при загрузке сообщений в поставщик транспорта.</span><span class="sxs-lookup"><span data-stu-id="530d4-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="530d4-108">Вызывающие абоненты указывают область возможных расхождений путем передачи одного или двух флагов в **ртфсинк**:</span><span class="sxs-lookup"><span data-stu-id="530d4-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="530d4-109">RTF_SYNC_BODY_CHANGED, чтобы указать изменение текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="530d4-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="530d4-110">RTF_SYNC_RTF_CHANGED, чтобы указать изменение форматирования сообщения.</span><span class="sxs-lookup"><span data-stu-id="530d4-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="530d4-111">Процесс синхронизации, выполняемый в **ртфсинк** , это сложная циклическая контрольная проверка (CRC) текста сообщения, которая игнорирует некоторые символы и преобразует другие.</span><span class="sxs-lookup"><span data-stu-id="530d4-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="530d4-112">Символы, которые скорее всего были добавлены поставщиками транспорта, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="530d4-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="530d4-113">MAPI определяет несколько свойств для работы с RTF, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="530d4-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="530d4-114">**Свойство RTF**</span><span class="sxs-lookup"><span data-stu-id="530d4-114">**RTF property**</span></span>|<span data-ttu-id="530d4-115">**Описание**</span><span class="sxs-lookup"><span data-stu-id="530d4-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="530d4-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="530d4-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="530d4-117">Указывает начало реального текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="530d4-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="530d4-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="530d4-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="530d4-119">Содержит результат циклической проверки избыточности текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="530d4-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="530d4-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="530d4-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="530d4-121">Содержит число символов в **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="530d4-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="530d4-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="530d4-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="530d4-123">Установите значение TRUE при синхронизации текста сообщения и форматирования.</span><span class="sxs-lookup"><span data-stu-id="530d4-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="530d4-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="530d4-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="530d4-125">Содержит количество непустых символов, прецеед текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="530d4-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="530d4-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="530d4-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="530d4-127">Содержит количество непустых символов, заканчивающихся текстом сообщения.</span><span class="sxs-lookup"><span data-stu-id="530d4-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

