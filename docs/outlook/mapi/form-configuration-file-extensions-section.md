---
title: Раздел "файл конфигурации формы [расширения]"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 96682dd2bdfedc42ea13c6985cb834f0adffd4df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327302"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="ae7f9-103">Раздел "файл конфигурации формы [расширения]"</span><span class="sxs-lookup"><span data-stu-id="ae7f9-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="ae7f9-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae7f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae7f9-105">В разделе **[Extensions]** перечисляются расширенные атрибуты формы, обычно это именованный набор свойств, который содержит все атрибуты за пределами базовых, перечисленных в разделе **[Description]** файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="ae7f9-106">Расширенные атрибуты — это свойства, возвращаемые из \*\*\*\* вызовов метода PROPS объекта **имапиформинфо** с набором High bit в теге Property.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="ae7f9-107">Клиентские приложения могут определять дополнительные атрибуты формы, если они есть, путем извлечения этих тегов.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="ae7f9-108">Для этого клиенты вызывают метод [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , передавая имена свойств формы и вызывайте метод [IMAPIProp:: Prop](imapiprop-getprops.md) для получения свойств.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="ae7f9-109">**Разрешений**</span><span class="sxs-lookup"><span data-stu-id="ae7f9-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="ae7f9-110">**Модулей.**</span><span class="sxs-lookup"><span data-stu-id="ae7f9-110">**Extension.**</span></span> <span data-ttu-id="ae7f9-111">_строка1_ =  _строка2_</span><span class="sxs-lookup"><span data-stu-id="ae7f9-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="ae7f9-112">Каждый раздел свойства расширения определяет один атрибут расширения с помощью синтаксиса именованного свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="ae7f9-113">Свойство должно иметь тип ПТ_ЛОНГ или PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="ae7f9-114">Наборы свойств, содержащие именованные строки, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="ae7f9-115">Формат раздела **[Extension]** :</span><span class="sxs-lookup"><span data-stu-id="ae7f9-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="ae7f9-116">**Модулей.**</span><span class="sxs-lookup"><span data-stu-id="ae7f9-116">**[Extension.**</span></span> <span data-ttu-id="ae7f9-117">_строка2_ **]**</span><span class="sxs-lookup"><span data-stu-id="ae7f9-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="ae7f9-118">**Тип** =  _Integer_</span><span class="sxs-lookup"><span data-stu-id="ae7f9-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="ae7f9-119">\*\*\*\* =  _GUID_ нмидпропсет</span><span class="sxs-lookup"><span data-stu-id="ae7f9-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="ae7f9-120">\*\*\*\* =  _Целое число_ нмидинтежер</span><span class="sxs-lookup"><span data-stu-id="ae7f9-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="ae7f9-121">\*\*\*\* =  __ Строка |  значения_Integer_</span><span class="sxs-lookup"><span data-stu-id="ae7f9-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="ae7f9-122">Ниже приведен пример раздела **[Extensions]** и последующих связанных разделов.</span><span class="sxs-lookup"><span data-stu-id="ae7f9-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


