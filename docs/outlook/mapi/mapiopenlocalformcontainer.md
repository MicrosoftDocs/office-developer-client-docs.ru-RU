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
ms.openlocfilehash: 87696ceea96bd2f51bfe5a0b062499946179c8b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582562"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="56751-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="56751-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="56751-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56751-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56751-105">Возвращает указатель интерфейса библиотеку локального формы.</span><span class="sxs-lookup"><span data-stu-id="56751-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56751-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="56751-106">Header file:</span></span>  <br/> |<span data-ttu-id="56751-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="56751-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="56751-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="56751-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="56751-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="56751-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="56751-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="56751-110">Called by:</span></span>  <br/> |<span data-ttu-id="56751-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="56751-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="56751-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="56751-112">Parameters</span></span>

 <span data-ttu-id="56751-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="56751-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="56751-114">[out] Указатель на указатель на интерфейс библиотеки локального формы.</span><span class="sxs-lookup"><span data-stu-id="56751-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56751-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56751-115">Return value</span></span>

<span data-ttu-id="56751-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="56751-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56751-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="56751-117">Remarks</span></span>

<span data-ttu-id="56751-118">Интерфейс, для которого возвращается указатель можно использовать с помощью программ сторонних производителей установки для установки отдельных приложений форм в библиотеку без программа предварительного войдите в систему MAPI.</span><span class="sxs-lookup"><span data-stu-id="56751-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="56751-119">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="56751-119">MFCMAPI reference</span></span>

<span data-ttu-id="56751-120">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="56751-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="56751-121">**Файл**</span><span class="sxs-lookup"><span data-stu-id="56751-121">**File**</span></span>|<span data-ttu-id="56751-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="56751-122">**Function**</span></span>|<span data-ttu-id="56751-123">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="56751-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56751-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="56751-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="56751-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="56751-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="56751-126">Mfcmapi (en) использует метод **MAPIOpenLocalFormContainer** для открытия контейнера локального формы для отображения в новом окне.</span><span class="sxs-lookup"><span data-stu-id="56751-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56751-127">См. также</span><span class="sxs-lookup"><span data-stu-id="56751-127">See also</span></span>



[<span data-ttu-id="56751-128">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="56751-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

