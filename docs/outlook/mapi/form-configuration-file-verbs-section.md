---
title: Раздел Конфигурация формы [Глаголы]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417786"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="d769f-103">Раздел Конфигурация формы [Глаголы]</span><span class="sxs-lookup"><span data-stu-id="d769f-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="d769f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d769f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d769f-105">В **разделе [Verbs]** перечислены полные наборы глаголов, поддерживаемых формой.</span><span class="sxs-lookup"><span data-stu-id="d769f-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="d769f-106">Формат раздела **[Глаголы]:**</span><span class="sxs-lookup"><span data-stu-id="d769f-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="d769f-107">**[Глаголы]**</span><span class="sxs-lookup"><span data-stu-id="d769f-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="d769f-108">**Verb1**  =   _строка_</span><span class="sxs-lookup"><span data-stu-id="d769f-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="d769f-109">Ниже приводится пример **раздела [Verbs].**</span><span class="sxs-lookup"><span data-stu-id="d769f-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="d769f-110">Каждый глагол определяется в **отдельном [Verb.**</span><span class="sxs-lookup"><span data-stu-id="d769f-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="d769f-111">_строка_ **]** раздела.</span><span class="sxs-lookup"><span data-stu-id="d769f-111">_string_ **]** section.</span></span> <span data-ttu-id="d769f-112">**[Глагол.**</span><span class="sxs-lookup"><span data-stu-id="d769f-112">A **[Verb.**</span></span> <span data-ttu-id="d769f-113">_строка_ **]** в разделе описывается один глагол, предлагаемый формой.</span><span class="sxs-lookup"><span data-stu-id="d769f-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="d769f-114">Запись **DisplayName** в **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="d769f-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="d769f-115">_в_ разделе string **]** указывается имя команды, отображаемая в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="d769f-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="d769f-116">Запись **Кода** соответствует числу глаголов, переданным методом [IMAPIForm::D oVerb.](imapiform-doverb.md)</span><span class="sxs-lookup"><span data-stu-id="d769f-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="d769f-117">Синтаксис **для [Verb.**</span><span class="sxs-lookup"><span data-stu-id="d769f-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="d769f-118">_строка_ **]** раздел:</span><span class="sxs-lookup"><span data-stu-id="d769f-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="d769f-119">**[Глагол.**</span><span class="sxs-lookup"><span data-stu-id="d769f-119">**[Verb.**</span></span> <span data-ttu-id="d769f-120">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="d769f-120">_string_ **]**</span></span>
  
 <span data-ttu-id="d769f-121">**DisplayName**  =   _отображаемая строка_</span><span class="sxs-lookup"><span data-stu-id="d769f-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="d769f-122">**Код**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="d769f-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="d769f-123">**Флаги**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="d769f-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="d769f-124">**Attribs**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="d769f-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="d769f-125">Ниже приводится пример **[Verb.**</span><span class="sxs-lookup"><span data-stu-id="d769f-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="d769f-126">_строка_ **]** раздела.</span><span class="sxs-lookup"><span data-stu-id="d769f-126">_string_ **]** section.</span></span> 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

<span data-ttu-id="d769f-127">Глаголы, перечисленные в этом разделе, извлекаются клиентом с помощью [метода IMAPIFormInfo::CalcVerbSet.](imapiforminfo-calcverbset.md)</span><span class="sxs-lookup"><span data-stu-id="d769f-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="d769f-128">Глаголы активируются, вызывая метод [IMAPIForm::D oVerb](imapiform-doverb.md) формы и передав ему кодовое число выполняемого глагола.</span><span class="sxs-lookup"><span data-stu-id="d769f-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

