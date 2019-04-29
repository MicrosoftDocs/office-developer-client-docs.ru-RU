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
ms.openlocfilehash: de0c1181450c536dffd5a84242c17bd1dd612566
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418052"
---
# <a name="mapiopenformmgr"></a><span data-ttu-id="75c4f-103">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="75c4f-103">MAPIOpenFormMgr</span></span>

  
  
<span data-ttu-id="75c4f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75c4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75c4f-105">Открывает интерфейс [имапиформмгр](imapiformmgriunknown.md) для объекта поставщика библиотеки форм в контексте существующего сеанса.</span><span class="sxs-lookup"><span data-stu-id="75c4f-105">Opens an [IMAPIFormMgr](imapiformmgriunknown.md) interface on a form library provider object in the context of an existing session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75c4f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="75c4f-106">Header file:</span></span>  <br/> |<span data-ttu-id="75c4f-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="75c4f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="75c4f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="75c4f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="75c4f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="75c4f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="75c4f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="75c4f-110">Called by:</span></span>  <br/> |<span data-ttu-id="75c4f-111">Клиентские приложения</span><span class="sxs-lookup"><span data-stu-id="75c4f-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenFormMgr(
  LPMAPISESSION pSession,
  LPMAPIFORMMGR FAR * ppmgr
);
```

## <a name="parameters"></a><span data-ttu-id="75c4f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="75c4f-112">Parameters</span></span>

 <span data-ttu-id="75c4f-113">_Псессион_</span><span class="sxs-lookup"><span data-stu-id="75c4f-113">_pSession_</span></span>
  
> <span data-ttu-id="75c4f-114">возврата Указатель на сеанс, используемый клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="75c4f-114">[in] Pointer to the session in use by the client application.</span></span>
    
 <span data-ttu-id="75c4f-115">_ппмгр_</span><span class="sxs-lookup"><span data-stu-id="75c4f-115">_ppmgr_</span></span>
  
> <span data-ttu-id="75c4f-116">вышли Указатель на возвращенный интерфейс **имапиформмгр** .</span><span class="sxs-lookup"><span data-stu-id="75c4f-116">[out] Pointer to the returned **IMAPIFormMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="75c4f-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="75c4f-117">Return value</span></span>

<span data-ttu-id="75c4f-118">Нет.</span><span class="sxs-lookup"><span data-stu-id="75c4f-118">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75c4f-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="75c4f-119">Remarks</span></span>

<span data-ttu-id="75c4f-120">После того как клиентское приложение вызовет функцию **мапиопенформмгр** , большинство последующих взаимодействий, связанных с формами, выполняются через поставщика библиотеки форм или через интерфейс, возвращенный поставщиком библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="75c4f-120">After a client application makes a call to the **MAPIOpenFormMgr** function, most subsequent forms-related interactions take place through the form library provider or an interface returned by the form library provider.</span></span> <span data-ttu-id="75c4f-121">Интерфейс **имапиформмгр** позволяет клиенту работать с обработчиками сообщений и выполнять разрешения между классами сообщений и библиотеками форм.</span><span class="sxs-lookup"><span data-stu-id="75c4f-121">The **IMAPIFormMgr** interface allows the client to work with message handlers and perform resolutions between message classes and form libraries.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="75c4f-122">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="75c4f-122">MFCMAPI reference</span></span>

<span data-ttu-id="75c4f-123">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="75c4f-123">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="75c4f-124">**Файл**</span><span class="sxs-lookup"><span data-stu-id="75c4f-124">**File**</span></span>|<span data-ttu-id="75c4f-125">**Функция**</span><span class="sxs-lookup"><span data-stu-id="75c4f-125">**Function**</span></span>|<span data-ttu-id="75c4f-126">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="75c4f-126">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="75c4f-127">Маиндлг. cpp открывает Диспетчер форм, чтобы можно было выбрать форму.</span><span class="sxs-lookup"><span data-stu-id="75c4f-127">MainDlg.cpp opens the form manager so a form can be selected.</span></span>  <br/> |<span data-ttu-id="75c4f-128">Кмаиндлг:: Онселектформ</span><span class="sxs-lookup"><span data-stu-id="75c4f-128">CMainDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="75c4f-129">MFCMAPI использует метод **мапиопенформмгр** , чтобы открыть Диспетчер форм, чтобы можно было выбрать форму.</span><span class="sxs-lookup"><span data-stu-id="75c4f-129">MFCMAPI uses the **MAPIOpenFormMgr** method to open the form manager so a form can be selected.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75c4f-130">См. также</span><span class="sxs-lookup"><span data-stu-id="75c4f-130">See also</span></span>



[<span data-ttu-id="75c4f-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="75c4f-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

