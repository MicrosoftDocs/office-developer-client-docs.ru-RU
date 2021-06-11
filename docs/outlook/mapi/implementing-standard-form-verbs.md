---
title: Реализация стандартных глаголов формы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426123"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="a8ce3-103">Реализация стандартных глаголов формы</span><span class="sxs-lookup"><span data-stu-id="a8ce3-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="a8ce3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8ce3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8ce3-105">MAPI определяет набор стандартных глаголов или действий, принятых, когда пользователь делает выбор меню или нажимает кнопку, которую должны поддерживать все зрители форм.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="a8ce3-106">Каждый глагол имеет констант, связанный с ним для идентификации, определенный в EXCHFORM. Файл заглавной папки H.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="a8ce3-107">В следующей таблице перечислены стандартные глаголы формы и связанные с ними константы:</span><span class="sxs-lookup"><span data-stu-id="a8ce3-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="a8ce3-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="a8ce3-108">**Verb**</span></span>|<span data-ttu-id="a8ce3-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a8ce3-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8ce3-110">Открыть</span><span class="sxs-lookup"><span data-stu-id="a8ce3-110">Open</span></span>  <br/> |<span data-ttu-id="a8ce3-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="a8ce3-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="a8ce3-112">Ответить</span><span class="sxs-lookup"><span data-stu-id="a8ce3-112">Reply</span></span>  <br/> |<span data-ttu-id="a8ce3-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="a8ce3-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="a8ce3-114">Ответ на все</span><span class="sxs-lookup"><span data-stu-id="a8ce3-114">Reply to All</span></span>  <br/> |<span data-ttu-id="a8ce3-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="a8ce3-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="a8ce3-116">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="a8ce3-116">Forward</span></span>  <br/> |<span data-ttu-id="a8ce3-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="a8ce3-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="a8ce3-118">Печать</span><span class="sxs-lookup"><span data-stu-id="a8ce3-118">Print</span></span>  <br/> |<span data-ttu-id="a8ce3-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="a8ce3-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="a8ce3-120">Сохранить как</span><span class="sxs-lookup"><span data-stu-id="a8ce3-120">Save As</span></span>  <br/> |<span data-ttu-id="a8ce3-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="a8ce3-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="a8ce3-122">Ответ на папку</span><span class="sxs-lookup"><span data-stu-id="a8ce3-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="a8ce3-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="a8ce3-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="a8ce3-124">Когда пользователь выбирает глагол, передай его константа в вызове методу [IMAPIForm::D oVerb](imapiform-doverb.md) для выполнения соответствующего действия.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="a8ce3-125">В дополнение к доступу к глаголам через вашего просмотра формы, пользователи иногда могут получить доступ к глаголам непосредственно из формы.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="a8ce3-126">Например, некоторые объекты формы позволяют пользователю вызывать глагол **Print,** щелкнув правой кнопкой мыши по форме и выбрав print **из** контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="a8ce3-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

