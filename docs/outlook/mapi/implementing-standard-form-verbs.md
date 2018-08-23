---
title: Реализация стандартных команд для форм
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 46585859e1dde4ecf38262f99cac5e3a9d29e5db
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568751"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="3d8d7-103">Реализация стандартных команд для форм</span><span class="sxs-lookup"><span data-stu-id="3d8d7-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="3d8d7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d8d7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d8d7-105">MAPI определяет набор стандартных команд или действия в случае, если пользователь выбирает элемент меню или нажатии кнопки, поддерживающая всем пользователям формы.</span><span class="sxs-lookup"><span data-stu-id="3d8d7-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="3d8d7-106">Каждый имеет константа, связанные с ним для идентификации, определенных в EXCHFORM. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="3d8d7-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="3d8d7-107">В следующей таблице приведены команды стандартной формы и их связанных констант:</span><span class="sxs-lookup"><span data-stu-id="3d8d7-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="3d8d7-108">**Глагол**</span><span class="sxs-lookup"><span data-stu-id="3d8d7-108">**Verb**</span></span>|<span data-ttu-id="3d8d7-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="3d8d7-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3d8d7-110">Open</span><span class="sxs-lookup"><span data-stu-id="3d8d7-110">Open</span></span>  <br/> |<span data-ttu-id="3d8d7-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="3d8d7-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="3d8d7-112">Ответить</span><span class="sxs-lookup"><span data-stu-id="3d8d7-112">Reply</span></span>  <br/> |<span data-ttu-id="3d8d7-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="3d8d7-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="3d8d7-114">Ответить всем</span><span class="sxs-lookup"><span data-stu-id="3d8d7-114">Reply to All</span></span>  <br/> |<span data-ttu-id="3d8d7-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="3d8d7-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="3d8d7-116">Переслать</span><span class="sxs-lookup"><span data-stu-id="3d8d7-116">Forward</span></span>  <br/> |<span data-ttu-id="3d8d7-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="3d8d7-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="3d8d7-118">Print</span><span class="sxs-lookup"><span data-stu-id="3d8d7-118">Print</span></span>  <br/> |<span data-ttu-id="3d8d7-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="3d8d7-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="3d8d7-120">Сохранить как</span><span class="sxs-lookup"><span data-stu-id="3d8d7-120">Save As</span></span>  <br/> |<span data-ttu-id="3d8d7-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="3d8d7-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="3d8d7-122">Ответ в папку</span><span class="sxs-lookup"><span data-stu-id="3d8d7-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="3d8d7-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="3d8d7-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="3d8d7-124">Если пользователь выбирает команду, передайте его константу вызов метода [IMAPIForm::DoVerb](imapiform-doverb.md) формы для его соответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="3d8d7-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="3d8d7-125">В дополнение к доступ к команд с помощью средства просмотра вашей формы, в некоторых случаях пользователям глаголов непосредственно из формы.</span><span class="sxs-lookup"><span data-stu-id="3d8d7-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="3d8d7-126">К примеру некоторые объекты формы пользователь может вызвать глаголов **Print** , щелкнув правой кнопкой мыши на форме и выберите команду **Печать** контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="3d8d7-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

