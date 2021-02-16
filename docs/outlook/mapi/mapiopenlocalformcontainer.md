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
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427740"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="46bd7-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="46bd7-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="46bd7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46bd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46bd7-105">Возвращает указатель интерфейса на локализованную библиотеку форм.</span><span class="sxs-lookup"><span data-stu-id="46bd7-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46bd7-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="46bd7-106">Header file:</span></span>  <br/> |<span data-ttu-id="46bd7-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="46bd7-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="46bd7-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="46bd7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="46bd7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="46bd7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="46bd7-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="46bd7-110">Called by:</span></span>  <br/> |<span data-ttu-id="46bd7-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="46bd7-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="46bd7-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="46bd7-112">Parameters</span></span>

 <span data-ttu-id="46bd7-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="46bd7-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="46bd7-114">[out] Указатель на указатель на интерфейс локальной библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="46bd7-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="46bd7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46bd7-115">Return value</span></span>

<span data-ttu-id="46bd7-116">Нет.</span><span class="sxs-lookup"><span data-stu-id="46bd7-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46bd7-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="46bd7-117">Remarks</span></span>

<span data-ttu-id="46bd7-118">Интерфейс, в который возвращается указатель, может использоваться программами установки сторонних приложений для установки форм, характерных для приложений, в библиотеку без необходимости входа в MAPI.</span><span class="sxs-lookup"><span data-stu-id="46bd7-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="46bd7-119">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="46bd7-119">MFCMAPI reference</span></span>

<span data-ttu-id="46bd7-120">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="46bd7-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="46bd7-121">**Файл**</span><span class="sxs-lookup"><span data-stu-id="46bd7-121">**File**</span></span>|<span data-ttu-id="46bd7-122">**Функция**</span><span class="sxs-lookup"><span data-stu-id="46bd7-122">**Function**</span></span>|<span data-ttu-id="46bd7-123">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="46bd7-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="46bd7-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="46bd7-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="46bd7-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="46bd7-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="46bd7-126">MFCMAPI использует метод **MAPIOpenLocalFormContainer** для открытия локального контейнера формы для отрисовки в новом окне.</span><span class="sxs-lookup"><span data-stu-id="46bd7-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46bd7-127">См. также</span><span class="sxs-lookup"><span data-stu-id="46bd7-127">See also</span></span>



[<span data-ttu-id="46bd7-128">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="46bd7-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

