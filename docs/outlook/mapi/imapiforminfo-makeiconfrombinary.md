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
ms.openlocfilehash: 30f55044327eecee3ab0d8ee2509d7132ab6e8ee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570130"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="06d1b-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="06d1b-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="06d1b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06d1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06d1b-105">Создает значок из одного из свойств значок формы.</span><span class="sxs-lookup"><span data-stu-id="06d1b-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="06d1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="06d1b-106">Parameters</span></span>

 <span data-ttu-id="06d1b-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="06d1b-107">_nPropID_</span></span>
  
> <span data-ttu-id="06d1b-108">[in] Идентификатор свойства для значка свойства.</span><span class="sxs-lookup"><span data-stu-id="06d1b-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="06d1b-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="06d1b-109">_phicon_</span></span>
  
> <span data-ttu-id="06d1b-110">[out] Указатель на возвращаемый значок.</span><span class="sxs-lookup"><span data-stu-id="06d1b-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="06d1b-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="06d1b-111">Return value</span></span>

<span data-ttu-id="06d1b-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="06d1b-112">S_OK</span></span> 
  
> <span data-ttu-id="06d1b-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="06d1b-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06d1b-114">���������</span><span class="sxs-lookup"><span data-stu-id="06d1b-114">Remarks</span></span>

<span data-ttu-id="06d1b-115">Клиентские приложения вызовите метод **IMAPIFormInfo::MakeIconFromBinary** для создания значка из одного из свойств значок формы.</span><span class="sxs-lookup"><span data-stu-id="06d1b-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="06d1b-116">В параметре _nPropID_ **MakeIconFromBinary** принимает идентификатор свойства одного из свойств значок формы.</span><span class="sxs-lookup"><span data-stu-id="06d1b-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="06d1b-117">Использование этого свойства идентификатора, построение выполнено значок, который может отображаться в табличном представлении, включая столбцы свойств для значков.</span><span class="sxs-lookup"><span data-stu-id="06d1b-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06d1b-118">См. также</span><span class="sxs-lookup"><span data-stu-id="06d1b-118">See also</span></span>



[<span data-ttu-id="06d1b-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="06d1b-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

