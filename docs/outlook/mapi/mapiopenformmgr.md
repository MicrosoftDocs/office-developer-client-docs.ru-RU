---
title: MAPIOpenFormMgr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenFormMgr
api_type:
- COM
ms.assetid: 5b624954-d975-4d5e-84d7-74e096ac30af
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2ed71b5eef0c25a78d7c8ec695a756a02e796dbf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586034"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="00b74-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="00b74-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="00b74-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00b74-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00b74-105">Откроется интерфейс [IMAPIFormMgr](imapiformmgriunknown.md) на объект поставщика библиотеки форм в контексте существующего сеанса.</span><span class="sxs-lookup"><span data-stu-id="00b74-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00b74-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="00b74-106">Header file:</span></span>  <br/> |<span data-ttu-id="00b74-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="00b74-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="00b74-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="00b74-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="00b74-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="00b74-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="00b74-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="00b74-110">Called by:</span></span>  <br/> |<span data-ttu-id="00b74-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="00b74-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="00b74-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="00b74-112">Parameters</span></span>

 <span data-ttu-id="00b74-113">_pSession_</span><span class="sxs-lookup"><span data-stu-id="00b74-113">_pSession_</span></span>
  
> <span data-ttu-id="00b74-114">[in] Указатель на сеанс используется клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="00b74-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="00b74-115">_ppmgr_</span><span class="sxs-lookup"><span data-stu-id="00b74-115">_ppmgr_</span></span>
  
> <span data-ttu-id="00b74-116">[out] Указатель на возвращенный интерфейс **IMAPIFormMgr** .</span><span class="sxs-lookup"><span data-stu-id="00b74-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00b74-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00b74-117">Return value</span></span>

<span data-ttu-id="00b74-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="00b74-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00b74-119">Замечания</span><span class="sxs-lookup"><span data-stu-id="00b74-119">Remarks</span></span>

<span data-ttu-id="00b74-120">После клиентское приложение вызывает функцию **MAPIOpenFormMgr** , большинство последующих связанных с forms происходят взаимодействия через поставщика библиотеки форм или интерфейс, возвращенные поставщиком библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="00b74-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="00b74-121">Интерфейс **IMAPIFormMgr** позволяет клиента для работы с обработчики сообщений и выполнять с разрешением от классов сообщений и библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="00b74-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="00b74-122">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="00b74-122">MFCMAPI reference</span></span>

<span data-ttu-id="00b74-123">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="00b74-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="00b74-124">**����**</span><span class="sxs-lookup"><span data-stu-id="00b74-124">**File**</span></span>|<span data-ttu-id="00b74-125">**�������**</span><span class="sxs-lookup"><span data-stu-id="00b74-125">**Function**</span></span>|<span data-ttu-id="00b74-126">**�����������**</span><span class="sxs-lookup"><span data-stu-id="00b74-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00b74-127">MainDlg.cpp Откроется диспетчер форм, можно выбрать форму.</span><span class="sxs-lookup"><span data-stu-id="00b74-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="00b74-128">CMainDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="00b74-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="00b74-129">Mfcmapi (en) использует метод **MAPIOpenFormMgr** , чтобы открыть диспетчер формы, поэтому можно выбирать в форме.</span><span class="sxs-lookup"><span data-stu-id="00b74-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00b74-130">См. также</span><span class="sxs-lookup"><span data-stu-id="00b74-130">See also</span></span>



[<span data-ttu-id="00b74-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="00b74-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

