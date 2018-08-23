---
title: 'Файл конфигурации формы: раздел [Команды]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6a06283e3eb072e1f502d0b1bd303ce9f0733578
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583976"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="4bcf0-103">Файл конфигурации формы: раздел [Команды]</span><span class="sxs-lookup"><span data-stu-id="4bcf0-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="4bcf0-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4bcf0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4bcf0-105">**[]** Разделе перечислены полный набор команд, поддерживаемых формы.</span><span class="sxs-lookup"><span data-stu-id="4bcf0-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="4bcf0-106">Имеет формат **[]** разделе:</span><span class="sxs-lookup"><span data-stu-id="4bcf0-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="4bcf0-107">**[Команд]**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="4bcf0-108">**Verb1** =  _строки_</span><span class="sxs-lookup"><span data-stu-id="4bcf0-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="4bcf0-109">Ниже приведен пример раздела **[команд]** .</span><span class="sxs-lookup"><span data-stu-id="4bcf0-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="4bcf0-110">Команд определяется в отдельном **[глаголов.**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="4bcf0-111">_строка_ раздел **]** .</span><span class="sxs-lookup"><span data-stu-id="4bcf0-111">_string_ **]** section.</span></span> <span data-ttu-id="4bcf0-112">A **[глаголов.**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-112">A **[Verb.**</span></span> <span data-ttu-id="4bcf0-113">_строка_ **]** разделе описываются в виде одной команды.</span><span class="sxs-lookup"><span data-stu-id="4bcf0-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="4bcf0-114">Запись **DisplayName** в **[глаголов.**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="4bcf0-115">_строка_ раздел **]** указывает имя команды, отображаемые в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="4bcf0-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="4bcf0-116">Запись **кода** соответствует номер команды, переданной в метод [IMAPIForm::DoVerb](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="4bcf0-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="4bcf0-117">Синтаксис для **[глаголов.**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="4bcf0-118">_строка_ раздел **]** :</span><span class="sxs-lookup"><span data-stu-id="4bcf0-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="4bcf0-119">**[Команда.**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-119">**[Verb.**</span></span> <span data-ttu-id="4bcf0-120">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-120">_string_ **]**</span></span>
  
 <span data-ttu-id="4bcf0-121">**Отображаемое имя** =  _отображается строка_</span><span class="sxs-lookup"><span data-stu-id="4bcf0-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="4bcf0-122">**Код** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="4bcf0-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="4bcf0-123">**Флаги** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="4bcf0-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="4bcf0-124">**Атрибутов** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="4bcf0-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="4bcf0-125">Ниже приведен пример **[глаголов.**</span><span class="sxs-lookup"><span data-stu-id="4bcf0-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="4bcf0-126">_строка_ раздел **]** .</span><span class="sxs-lookup"><span data-stu-id="4bcf0-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="4bcf0-127">Команды, приведенные в этом разделе извлекаются с помощью [метода IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md)клиентом.</span><span class="sxs-lookup"><span data-stu-id="4bcf0-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="4bcf0-128">Команды, активируются путем вызова метода [IMAPIForm::DoVerb](imapiform-doverb.md) формы и передав номер кода команды нужно выполнить.</span><span class="sxs-lookup"><span data-stu-id="4bcf0-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

