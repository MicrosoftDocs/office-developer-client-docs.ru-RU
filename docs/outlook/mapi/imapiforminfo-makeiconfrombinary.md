---
title: IMAPIFormInfoMakeIconFromBinary
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.MakeIconFromBinary
api_type:
- COM
ms.assetid: 4daeddd7-3f0c-4178-ae8d-f74814090d40
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 418056f7222d5ab05f43a3661c1811bf2ae15be8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405116"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="46117-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="46117-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="46117-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46117-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46117-105">Создает значок из одного из свойств значка формы.</span><span class="sxs-lookup"><span data-stu-id="46117-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="46117-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="46117-106">Parameters</span></span>

 <span data-ttu-id="46117-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="46117-107">_nPropID_</span></span>
  
> <span data-ttu-id="46117-108">[in] Идентификатор свойства для свойства значок.</span><span class="sxs-lookup"><span data-stu-id="46117-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="46117-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="46117-109">_phicon_</span></span>
  
> <span data-ttu-id="46117-110">[вышел] Указатель на возвращенный значок.</span><span class="sxs-lookup"><span data-stu-id="46117-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46117-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46117-111">Return value</span></span>

<span data-ttu-id="46117-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="46117-112">S_OK</span></span> 
  
> <span data-ttu-id="46117-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="46117-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46117-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="46117-114">Remarks</span></span>

<span data-ttu-id="46117-115">Клиентские приложения называют **метод IMAPIFormInfo::MakeIconFromBinary** для создания значка из одного из свойств значка формы.</span><span class="sxs-lookup"><span data-stu-id="46117-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="46117-116">В  _параметре nPropID_ **MakeIconFromBinary** принимает идентификатор свойства одного из свойств значка формы.</span><span class="sxs-lookup"><span data-stu-id="46117-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="46117-117">С помощью этого идентификатора свойства создается значок, который может отображаться в представлениях таблиц, включая столбцы свойств для значков.</span><span class="sxs-lookup"><span data-stu-id="46117-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46117-118">См. также</span><span class="sxs-lookup"><span data-stu-id="46117-118">See also</span></span>



[<span data-ttu-id="46117-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="46117-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

