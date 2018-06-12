---
title: Реализация команд стандартной формы
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f89f7c58-6358-4523-9788-676f189b5e69
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 8135af7947f30ac600b8d9af364b2a79a3443ab6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809331"
---
# <a name="implementing-standard-form-verbs"></a><span data-ttu-id="0a188-103">Реализация команд стандартной формы</span><span class="sxs-lookup"><span data-stu-id="0a188-103">Implementing Standard Form Verbs</span></span>

  
  
<span data-ttu-id="0a188-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a188-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a188-105">MAPI определяет набор стандартных команд или действия в случае, если пользователь выбирает элемент меню или нажатии кнопки, поддерживающая всем пользователям формы.</span><span class="sxs-lookup"><span data-stu-id="0a188-105">MAPI defines a set of standard verbs, or actions taken when a user makes a menu selection or clicks a button, that all form viewers should support.</span></span> <span data-ttu-id="0a188-106">Каждый имеет константа, связанные с ним для идентификации, определенных в EXCHFORM. Файл заголовка.</span><span class="sxs-lookup"><span data-stu-id="0a188-106">Each verb has a constant associated with it for identification, defined in the EXCHFORM.H header file.</span></span> <span data-ttu-id="0a188-107">В следующей таблице приведены команды стандартной формы и их связанных констант:</span><span class="sxs-lookup"><span data-stu-id="0a188-107">The following table lists the standard form verbs and their associated constants:</span></span>
  
|<span data-ttu-id="0a188-108">**Команда**</span><span class="sxs-lookup"><span data-stu-id="0a188-108">**Verb**</span></span>|<span data-ttu-id="0a188-109">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0a188-109">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0a188-110">открытие;</span><span class="sxs-lookup"><span data-stu-id="0a188-110">Open</span></span>  <br/> |<span data-ttu-id="0a188-111">EXCHIVERB_OPEN</span><span class="sxs-lookup"><span data-stu-id="0a188-111">EXCHIVERB_OPEN</span></span>  <br/> |
|<span data-ttu-id="0a188-112">Ответить</span><span class="sxs-lookup"><span data-stu-id="0a188-112">Reply</span></span>  <br/> |<span data-ttu-id="0a188-113">EXCHIVERB_REPLYTOSENDER</span><span class="sxs-lookup"><span data-stu-id="0a188-113">EXCHIVERB_REPLYTOSENDER</span></span>  <br/> |
|<span data-ttu-id="0a188-114">Ответить всем</span><span class="sxs-lookup"><span data-stu-id="0a188-114">Reply to All</span></span>  <br/> |<span data-ttu-id="0a188-115">EXCHIVERB_REPLYTOALL</span><span class="sxs-lookup"><span data-stu-id="0a188-115">EXCHIVERB_REPLYTOALL</span></span>  <br/> |
|<span data-ttu-id="0a188-116">Переслать</span><span class="sxs-lookup"><span data-stu-id="0a188-116">Forward</span></span>  <br/> |<span data-ttu-id="0a188-117">EXCHIVERB_FORWARD</span><span class="sxs-lookup"><span data-stu-id="0a188-117">EXCHIVERB_FORWARD</span></span>  <br/> |
|<span data-ttu-id="0a188-118">Print</span><span class="sxs-lookup"><span data-stu-id="0a188-118">Print</span></span>  <br/> |<span data-ttu-id="0a188-119">EXCHIVERB_PRINT</span><span class="sxs-lookup"><span data-stu-id="0a188-119">EXCHIVERB_PRINT</span></span>  <br/> |
|<span data-ttu-id="0a188-120">Сохранить как</span><span class="sxs-lookup"><span data-stu-id="0a188-120">Save As</span></span>  <br/> |<span data-ttu-id="0a188-121">EXCHIVERB_SAVEAS</span><span class="sxs-lookup"><span data-stu-id="0a188-121">EXCHIVERB_SAVEAS</span></span>  <br/> |
|<span data-ttu-id="0a188-122">Ответ в папку</span><span class="sxs-lookup"><span data-stu-id="0a188-122">Reply to Folder</span></span>  <br/> |<span data-ttu-id="0a188-123">EXCHIVERB_REPLYTOFOLDER</span><span class="sxs-lookup"><span data-stu-id="0a188-123">EXCHIVERB_REPLYTOFOLDER</span></span>  <br/> |
   
<span data-ttu-id="0a188-124">Если пользователь выбирает команду, передайте его константу вызов метода [IMAPIForm::DoVerb](imapiform-doverb.md) формы для его соответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="0a188-124">When a user chooses a verb, pass its constant in a call to the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method to perform its corresponding action.</span></span> 
  
<span data-ttu-id="0a188-125">В дополнение к доступ к команд с помощью средства просмотра вашей формы, в некоторых случаях пользователям глаголов непосредственно из формы.</span><span class="sxs-lookup"><span data-stu-id="0a188-125">In addition to accessing verbs through your form viewer, users can sometimes access verbs directly from the form.</span></span> <span data-ttu-id="0a188-126">К примеру некоторые объекты формы пользователь может вызвать глаголов **Print** , щелкнув правой кнопкой мыши на форме и выберите команду **Печать** контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="0a188-126">For example, some form objects allow the user to invoke the **Print** verb by right-clicking on the form and choosing **Print** from a context-sensitive menu.</span></span> 
  

