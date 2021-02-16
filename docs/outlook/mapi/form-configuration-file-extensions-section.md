---
title: Файл конфигурации формы [расширения] Раздел
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423757"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="d694f-103">Файл конфигурации формы [расширения] Раздел</span><span class="sxs-lookup"><span data-stu-id="d694f-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="d694f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d694f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d694f-105">В разделе **[Extensions]** перечислены расширенные атрибуты формы, как правило, именоватый набор свойств, которые являются атрибутами, которые выходят за пределы базовых атрибутов, перечисленных в разделе **[Описание]** файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="d694f-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="d694f-106">Расширенные атрибуты — это свойства, возвращаемые при вызовах метода **GetProps** объекта **IMAPIFormInfo** с высоким битом в теге свойства.</span><span class="sxs-lookup"><span data-stu-id="d694f-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="d694f-107">Клиентские приложения могут определять расширенные атрибуты формы (если они есть) с помощью этих тегов.</span><span class="sxs-lookup"><span data-stu-id="d694f-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="d694f-108">Для этого клиенты вызовите метод [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) передав имена свойств формы и вызовите метод [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить свойства.</span><span class="sxs-lookup"><span data-stu-id="d694f-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="d694f-109">**[Расширения]**</span><span class="sxs-lookup"><span data-stu-id="d694f-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="d694f-110">**Расширение.**</span><span class="sxs-lookup"><span data-stu-id="d694f-110">**Extension.**</span></span> <span data-ttu-id="d694f-111">_string1_  =   _string2_</span><span class="sxs-lookup"><span data-stu-id="d694f-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="d694f-112">В каждом разделе свойств расширения определяется один атрибут расширения с использованием синтаксиса именуемой свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="d694f-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="d694f-113">Тип свойства должен быть PT_LONG или PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="d694f-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="d694f-114">Наборы свойств, которые содержат именуемую строку, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d694f-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="d694f-115">Формат раздела **[Расширение]:**</span><span class="sxs-lookup"><span data-stu-id="d694f-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="d694f-116">**[Расширение.**</span><span class="sxs-lookup"><span data-stu-id="d694f-116">**[Extension.**</span></span> <span data-ttu-id="d694f-117">_string2_ **]**</span><span class="sxs-lookup"><span data-stu-id="d694f-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="d694f-118">**Тип**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="d694f-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="d694f-119">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="d694f-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="d694f-120">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="d694f-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="d694f-121">**Значение**  =   _string_  |   _integer_</span><span class="sxs-lookup"><span data-stu-id="d694f-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="d694f-122">Ниже показан пример **раздела [Расширения]** и последующего связанного раздела.</span><span class="sxs-lookup"><span data-stu-id="d694f-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


