---
title: Файл конфигурации формы — раздел [Verbs]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327498"
---
# <a name="form-configuration-file-verbs-section"></a><span data-ttu-id="3e1cb-103">Файл конфигурации формы — раздел [Verbs]</span><span class="sxs-lookup"><span data-stu-id="3e1cb-103">Form Configuration File [Verbs] Section</span></span>

  
  
<span data-ttu-id="3e1cb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e1cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e1cb-105">В разделе **[Verbs]** приводится полный набор команд, поддерживаемых формой.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-105">The **[Verbs]** section lists the complete set of verbs supported by the form.</span></span> <span data-ttu-id="3e1cb-106">Формат раздела **[Verbs]** :</span><span class="sxs-lookup"><span data-stu-id="3e1cb-106">The format of the **[Verbs]** section is:</span></span> 
  
 <span data-ttu-id="3e1cb-107">**Команд**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-107">**[Verbs]**</span></span>
  
 <span data-ttu-id="3e1cb-108">\*\*\*\* =  _Строка_ Verb1</span><span class="sxs-lookup"><span data-stu-id="3e1cb-108">**Verb1** =  _string_</span></span>
  
<span data-ttu-id="3e1cb-109">Ниже приведен пример раздела **[Verbs]** .</span><span class="sxs-lookup"><span data-stu-id="3e1cb-109">Following is an example of a **[Verbs]** section.</span></span> 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

<span data-ttu-id="3e1cb-110">Каждая команда определена в отдельной **[verb.**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-110">Each verb is defined in a separate **[Verb.**</span></span> <span data-ttu-id="3e1cb-111">_строка_ **]** раздел.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-111">_string_ **]** section.</span></span> <span data-ttu-id="3e1cb-112">**[Verb.**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-112">A **[Verb.**</span></span> <span data-ttu-id="3e1cb-113">_строка_ **]** в разделе описывается одна команда, предлагаемая формой.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-113">_string_ **]** section describes a single verb offered by the form.</span></span> <span data-ttu-id="3e1cb-114">Запись **DisplayName** в **[verb.**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-114">The **DisplayName** entry in a **[Verb.**</span></span> <span data-ttu-id="3e1cb-115">_строка_ **]** раздел указывает имя команды, отображаемое в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-115">_string_ **]** section specifies the command name displayed in the user interface.</span></span> <span data-ttu-id="3e1cb-116">Запись **кода** соответствует номеру команды, переданному в методе [Имапиформ::D оверб](imapiform-doverb.md) .</span><span class="sxs-lookup"><span data-stu-id="3e1cb-116">The **Code** entry corresponds to the verb number passed in the [IMAPIForm::DoVerb](imapiform-doverb.md) method.</span></span> <span data-ttu-id="3e1cb-117">Синтаксис **[verb.**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-117">The syntax for the **[Verb.**</span></span> <span data-ttu-id="3e1cb-118">_строка_ **]** раздел:</span><span class="sxs-lookup"><span data-stu-id="3e1cb-118">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="3e1cb-119">**Команд.**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-119">**[Verb.**</span></span> <span data-ttu-id="3e1cb-120">_строка_ **]**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-120">_string_ **]**</span></span>
  
 <span data-ttu-id="3e1cb-121">\*\*\*\* =  _Отображаемая строка_ DisplayName</span><span class="sxs-lookup"><span data-stu-id="3e1cb-121">**DisplayName** =  _displayed string_</span></span>
  
 <span data-ttu-id="3e1cb-122">\*\*\*\* =  _Целое число_ кода</span><span class="sxs-lookup"><span data-stu-id="3e1cb-122">**Code** =  _integer_</span></span>
  
 <span data-ttu-id="3e1cb-123">\*\*\*\* =  _Целое число_ флагов</span><span class="sxs-lookup"><span data-stu-id="3e1cb-123">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="3e1cb-124">\*\*\*\* =  _Целое число_ аттрибс</span><span class="sxs-lookup"><span data-stu-id="3e1cb-124">**Attribs** =  _integer_</span></span>
  
<span data-ttu-id="3e1cb-125">Ниже приведен пример **[verb.**</span><span class="sxs-lookup"><span data-stu-id="3e1cb-125">Following is an example of a **[Verb.**</span></span> <span data-ttu-id="3e1cb-126">_строка_ **]** раздел.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-126">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="3e1cb-127">Команды, перечисленные в этом разделе, извлекаются клиентом с помощью [метода имапиформинфо:: калквербсет](imapiforminfo-calcverbset.md).</span><span class="sxs-lookup"><span data-stu-id="3e1cb-127">Verbs listed in this section are retrieved by a client using the [IMAPIFormInfo::CalcVerbSet method](imapiforminfo-calcverbset.md).</span></span> <span data-ttu-id="3e1cb-128">Команды активируются, вызывая метод формы [имапиформ::D оверб](imapiform-doverb.md) и передавая ему номер кода выполняемой команды.</span><span class="sxs-lookup"><span data-stu-id="3e1cb-128">Verbs are activated by calling the form's [IMAPIForm::DoVerb](imapiform-doverb.md) method and passing it the code number of the verb to be performed.</span></span> 
  

