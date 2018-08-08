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
ms.openlocfilehash: a230e8b69a64646dffb23147345d5960fdd38581
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808919"
---
# <a name="imapiforminfomakeiconfrombinary"></a><span data-ttu-id="bee61-103">IMAPIFormInfo::MakeIconFromBinary</span><span class="sxs-lookup"><span data-stu-id="bee61-103">IMAPIFormInfo::MakeIconFromBinary</span></span>

  
  
<span data-ttu-id="bee61-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bee61-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bee61-105">Создает значок из одного из свойств значок формы.</span><span class="sxs-lookup"><span data-stu-id="bee61-105">Builds an icon from one of the icon properties of a form.</span></span>
  
```cpp
HRESULT MakeIconFromBinary(
  ULONG nPropID,
  HICON FAR * phicon
);
```

## <a name="parameters"></a><span data-ttu-id="bee61-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bee61-106">Parameters</span></span>

 <span data-ttu-id="bee61-107">_nPropID_</span><span class="sxs-lookup"><span data-stu-id="bee61-107">_nPropID_</span></span>
  
> <span data-ttu-id="bee61-108">[in] Идентификатор свойства для значка свойства.</span><span class="sxs-lookup"><span data-stu-id="bee61-108">[in] A property identifier for an icon property.</span></span>
    
 <span data-ttu-id="bee61-109">_phicon_</span><span class="sxs-lookup"><span data-stu-id="bee61-109">_phicon_</span></span>
  
> <span data-ttu-id="bee61-110">[out] Указатель на возвращаемый значок.</span><span class="sxs-lookup"><span data-stu-id="bee61-110">[out] A pointer to the returned icon.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bee61-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="bee61-111">Return value</span></span>

<span data-ttu-id="bee61-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="bee61-112">S_OK</span></span> 
  
> <span data-ttu-id="bee61-113">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bee61-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bee61-114">���������</span><span class="sxs-lookup"><span data-stu-id="bee61-114">Remarks</span></span>

<span data-ttu-id="bee61-115">Клиентские приложения вызовите метод **IMAPIFormInfo::MakeIconFromBinary** для создания значка из одного из свойств значок формы.</span><span class="sxs-lookup"><span data-stu-id="bee61-115">Client applications call the **IMAPIFormInfo::MakeIconFromBinary** method to build an icon from one of the icon properties of a form.</span></span> <span data-ttu-id="bee61-116">В параметре _nPropID_ **MakeIconFromBinary** принимает идентификатор свойства одного из свойств значок формы.</span><span class="sxs-lookup"><span data-stu-id="bee61-116">In the  _nPropID_ parameter, **MakeIconFromBinary** takes the property identifier of one of the icon properties of a form.</span></span> <span data-ttu-id="bee61-117">Использование этого свойства идентификатора, построение выполнено значок, который может отображаться в табличном представлении, включая столбцы свойств для значков.</span><span class="sxs-lookup"><span data-stu-id="bee61-117">Using this property identifier, it builds an icon that can be displayed in table views that include property columns for icons.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bee61-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bee61-118">See also</span></span>



[<span data-ttu-id="bee61-119">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="bee61-119">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

