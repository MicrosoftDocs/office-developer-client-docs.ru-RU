---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c00c2fa04ae7e89f8c23c085ba021a935748ad4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809900"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="e593e-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="e593e-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="e593e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e593e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e593e-105">Возвращает указатель интерфейса библиотеку локального формы.</span><span class="sxs-lookup"><span data-stu-id="e593e-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e593e-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e593e-106">Header file:</span></span>  <br/> |<span data-ttu-id="e593e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="e593e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e593e-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="e593e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e593e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e593e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e593e-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="e593e-110">Called by:</span></span>  <br/> |<span data-ttu-id="e593e-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="e593e-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="e593e-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="e593e-112">Parameters</span></span>

 <span data-ttu-id="e593e-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="e593e-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="e593e-114">[out] Указатель на указатель на интерфейс библиотеки локального формы.</span><span class="sxs-lookup"><span data-stu-id="e593e-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e593e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e593e-115">Return value</span></span>

<span data-ttu-id="e593e-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="e593e-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e593e-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="e593e-117">Remarks</span></span>

<span data-ttu-id="e593e-118">Интерфейс, для которого возвращается указатель можно использовать с помощью программ сторонних производителей установки для установки отдельных приложений форм в библиотеку без программа предварительного войдите в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="e593e-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e593e-119">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="e593e-119">MFCMAPI reference</span></span>

<span data-ttu-id="e593e-120">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="e593e-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e593e-121">**����**</span><span class="sxs-lookup"><span data-stu-id="e593e-121">**File**</span></span>|<span data-ttu-id="e593e-122">**�������**</span><span class="sxs-lookup"><span data-stu-id="e593e-122">**Function**</span></span>|<span data-ttu-id="e593e-123">**�����������**</span><span class="sxs-lookup"><span data-stu-id="e593e-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e593e-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="e593e-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="e593e-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="e593e-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="e593e-126">Mfcmapi (en) использует метод **MAPIOpenLocalFormContainer** для открытия контейнера локального формы для отображения в новом окне.</span><span class="sxs-lookup"><span data-stu-id="e593e-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e593e-127">См. также</span><span class="sxs-lookup"><span data-stu-id="e593e-127">See also</span></span>



[<span data-ttu-id="e593e-128">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="e593e-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

