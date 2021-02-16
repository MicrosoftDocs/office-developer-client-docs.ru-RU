---
title: Реализация стандартных глаголов форм
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
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="79cb1-103">Реализация стандартных глаголов форм</span><span class="sxs-lookup"><span data-stu-id="79cb1-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="79cb1-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79cb1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79cb1-105">MAPI определяет набор стандартных глаголов или действий, которые должны поддерживаться всеми пользователями, которые должны поддерживаться при выборе меню или нажатии кнопки.</span><span class="sxs-lookup"><span data-stu-id="79cb1-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="79cb1-106">С каждым глаголом связана константа для идентификации, определяемая в EXCHFORM. Файл h-загона.</span><span class="sxs-lookup"><span data-stu-id="79cb1-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="79cb1-107">В следующей таблице перечислены стандартные команды формы и связанные с ними константы:</span><span class="sxs-lookup"><span data-stu-id="79cb1-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="79cb1-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="79cb1-108">**Verb**</span></span>|<span data-ttu-id="79cb1-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="79cb1-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79cb1-110">Открыть</span><span class="sxs-lookup"><span data-stu-id="79cb1-110">Open</span></span>  <br/> |<span data-ttu-id="79cb1-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="79cb1-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="79cb1-112">Ответить</span><span class="sxs-lookup"><span data-stu-id="79cb1-112">Reply</span></span>  <br/> |<span data-ttu-id="79cb1-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="79cb1-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="79cb1-114">Ответ всем</span><span class="sxs-lookup"><span data-stu-id="79cb1-114">Reply to All</span></span>  <br/> |<span data-ttu-id="79cb1-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="79cb1-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="79cb1-116">Перенаправление</span><span class="sxs-lookup"><span data-stu-id="79cb1-116">Forward</span></span>  <br/> |<span data-ttu-id="79cb1-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="79cb1-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="79cb1-118">Печать</span><span class="sxs-lookup"><span data-stu-id="79cb1-118">Print</span></span>  <br/> |<span data-ttu-id="79cb1-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="79cb1-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="79cb1-120">Сохранить как</span><span class="sxs-lookup"><span data-stu-id="79cb1-120">Save As</span></span>  <br/> |<span data-ttu-id="79cb1-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="79cb1-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="79cb1-122">Ответ папке</span><span class="sxs-lookup"><span data-stu-id="79cb1-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="79cb1-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="79cb1-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="79cb1-124">Когда пользователь выбирает глагол, передав его константы в вызове метода [IMAPIForm::D oVerb](imapiform-doverb.md) формы, чтобы выполнить соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="79cb1-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="79cb1-125">Помимо доступа к глаголам с помощью просмотра формы, пользователи иногда могут получать доступ к глаголам непосредственно из формы.</span><span class="sxs-lookup"><span data-stu-id="79cb1-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="79cb1-126">Например, некоторые объекты формы позволяют  пользователю вызвать глагол "Печать", щелкнув правой кнопкой мыши форму и выбрав пункт **"Печать"** в контекстном меню.</span><span class="sxs-lookup"><span data-stu-id="79cb1-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

