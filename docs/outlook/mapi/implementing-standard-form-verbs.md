---
title: Реализация стандартных команд форм
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6360b86dc23a5404b818f76cb1c2cd10747ef3cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317446"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="6733a-103">Реализация стандартных команд форм</span><span class="sxs-lookup"><span data-stu-id="6733a-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="6733a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6733a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6733a-105">MAPI определяет набор стандартных глаголов или действий, выполняемых при выборе пользователем кнопки меню или нажатии кнопки, которые должны поддерживаться всеми средствами просмотра формы.</span><span class="sxs-lookup"><span data-stu-id="6733a-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="6733a-106">С каждой командой связана константа, связанная с идентификацией, определенная в ЕКСЧФОРМ. H файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="6733a-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="6733a-107">В следующей таблице перечислены стандартные команды форм и связанные с ними константы.</span><span class="sxs-lookup"><span data-stu-id="6733a-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="6733a-108">**Verb**</span><span class="sxs-lookup"><span data-stu-id="6733a-108">**Verb**</span></span>|<span data-ttu-id="6733a-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="6733a-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6733a-110">Открыть</span><span class="sxs-lookup"><span data-stu-id="6733a-110">Open</span></span>  <br/> |<span data-ttu-id="6733a-111">ЕКСЧИВЕРБ_ОПЕН</span><span class="sxs-lookup"><span data-stu-id="6733a-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="6733a-112">Ответить</span><span class="sxs-lookup"><span data-stu-id="6733a-112">Reply</span></span>  <br/> |<span data-ttu-id="6733a-113">ЕКСЧИВЕРБ_РЕПЛИТОСЕНДЕР</span><span class="sxs-lookup"><span data-stu-id="6733a-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="6733a-114">Ответить всем</span><span class="sxs-lookup"><span data-stu-id="6733a-114">Reply to All</span></span>  <br/> |<span data-ttu-id="6733a-115">ЕКСЧИВЕРБ_РЕПЛИТОАЛЛ</span><span class="sxs-lookup"><span data-stu-id="6733a-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="6733a-116">Переслать</span><span class="sxs-lookup"><span data-stu-id="6733a-116">Forward</span></span>  <br/> |<span data-ttu-id="6733a-117">ЕКСЧИВЕРБ_ФОРВАРД</span><span class="sxs-lookup"><span data-stu-id="6733a-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="6733a-118">Print</span><span class="sxs-lookup"><span data-stu-id="6733a-118">Print</span></span>  <br/> |<span data-ttu-id="6733a-119">ЕКСЧИВЕРБ_ПРИНТ</span><span class="sxs-lookup"><span data-stu-id="6733a-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="6733a-120">Сохранить как</span><span class="sxs-lookup"><span data-stu-id="6733a-120">Save As</span></span>  <br/> |<span data-ttu-id="6733a-121">ЕКСЧИВЕРБ_САВЕАС</span><span class="sxs-lookup"><span data-stu-id="6733a-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="6733a-122">Ответить на папку</span><span class="sxs-lookup"><span data-stu-id="6733a-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="6733a-123">ЕКСЧИВЕРБ_РЕПЛИТОФОЛДЕР</span><span class="sxs-lookup"><span data-stu-id="6733a-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="6733a-124">Когда пользователь выбирает команду, передайте ее константу в вызове метода [имапиформ::D оверб](imapiform-doverb.md) , чтобы выполнить соответствующее действие.</span><span class="sxs-lookup"><span data-stu-id="6733a-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="6733a-125">Помимо доступа к командам в средстве просмотра форм, пользователи могут иногда получать доступ к командам непосредственно из формы.</span><span class="sxs-lookup"><span data-stu-id="6733a-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="6733a-126">Например, некоторые объекты форм позволяют пользователю вызвать команду **печати** , щелкнув форму правой кнопкой мыши и выбрав **Печать** из контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="6733a-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

