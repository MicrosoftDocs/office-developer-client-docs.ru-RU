---
title: 'Файл конфигурации формы: раздел [Расширения]'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4817e446-982d-491c-abcf-cc888a771afa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7c26b86ad4d6c7fd565abddbfc76f50ac3dccaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808457"
---
# <a name="form-configuration-file-extensions-section"></a><span data-ttu-id="07336-103">Файл конфигурации формы: раздел [Расширения]</span><span class="sxs-lookup"><span data-stu-id="07336-103">Form Configuration File [Extensions] Section</span></span>

  
  
<span data-ttu-id="07336-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07336-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07336-105">В разделе **[расширения]** приведены дополнительные атрибуты формы, обычно набор именованных свойств, которые являются какие-либо атрибуты за пределы основные из них, перечисленные в разделе **[Описание]** файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="07336-105">The **[Extensions]** section lists the extended attributes of the form, typically a named property set, which are any attributes beyond the basic ones listed in the **[Description]** section of the form configuration file.</span></span> <span data-ttu-id="07336-106">Дополнительные атрибуты, возвращаемые из вызовы метода **GetProps** объекта **IMAPIFormInfo** с высокой бит в тег свойства свойства.</span><span class="sxs-lookup"><span data-stu-id="07336-106">Extended attributes are properties returned from calls to the **GetProps** method of the **IMAPIFormInfo** object with the high bit set in the property tag.</span></span> <span data-ttu-id="07336-107">Клиентские приложения можно определить дополнительные атрибуты формы, путем получения этих тегов.</span><span class="sxs-lookup"><span data-stu-id="07336-107">Client applications can determine a form's extended attributes, if any, by retrieving these tags.</span></span> <span data-ttu-id="07336-108">Для этого клиенты вызовите метод [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) , передав в именах свойств формы и вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) для получения свойства.</span><span class="sxs-lookup"><span data-stu-id="07336-108">To do so, clients call the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method, passing in the names of the form's properties and call the [IMAPIProp::GetProps](imapiprop-getprops.md) method to get the properties.</span></span> 
  
 <span data-ttu-id="07336-109">**[Расширения]**</span><span class="sxs-lookup"><span data-stu-id="07336-109">**[Extensions]**</span></span>
  
 <span data-ttu-id="07336-110">**Расширение.**</span><span class="sxs-lookup"><span data-stu-id="07336-110">**Extension.**</span></span> <span data-ttu-id="07336-111">_string1_ =  _string2_</span><span class="sxs-lookup"><span data-stu-id="07336-111">_string1_ =  _string2_</span></span>
  
<span data-ttu-id="07336-112">Каждый раздел свойства extension определяет один атрибут расширения, с помощью интерфейса MAPI, с именем синтаксис свойства.</span><span class="sxs-lookup"><span data-stu-id="07336-112">Each extension property section defines one extension attribute using the MAPI named property syntax.</span></span> <span data-ttu-id="07336-113">Тип свойства должен быть PT_LONG или PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="07336-113">The property type must be either PT_LONG or PT_STRING8.</span></span> <span data-ttu-id="07336-114">Наборы свойств, которые содержит именованные строки не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="07336-114">Property sets that contains named strings are not supported.</span></span> <span data-ttu-id="07336-115">Имеет формат в раздел **[расширения]** :</span><span class="sxs-lookup"><span data-stu-id="07336-115">The format of the **[Extension]** section is:</span></span> 
  
 <span data-ttu-id="07336-116">**[Расширение.**</span><span class="sxs-lookup"><span data-stu-id="07336-116">**[Extension.**</span></span> <span data-ttu-id="07336-117">_строка string2_ **]**</span><span class="sxs-lookup"><span data-stu-id="07336-117">_string2_ **]**</span></span>
  
 <span data-ttu-id="07336-118">**Тип** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="07336-118">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="07336-119">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="07336-119">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="07336-120">**NmidInteger** =  _целое число_</span><span class="sxs-lookup"><span data-stu-id="07336-120">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="07336-121">**Значение** =  _строка_ |  _целое число_</span><span class="sxs-lookup"><span data-stu-id="07336-121">**Value** =  _string_ |  _integer_</span></span>
  
<span data-ttu-id="07336-122">Показан пример **[расширения]** и последующих связанных с ними разделов подписки.</span><span class="sxs-lookup"><span data-stu-id="07336-122">An example of an **[Extensions]** section and a subsequent related section is shown following.</span></span> 
  
```
[Extensions]
Extension.A = 1
[Extension.1]
Type = 30
NmidPropset = {00020D0C-0000-0000-C000-000000000046}
NmidInteger = 1
Value = 11220000

```


