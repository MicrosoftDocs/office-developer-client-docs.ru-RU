---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cb7fa7bb7dc17a89fc7cc40ae370accc40fa3941
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579842"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="14ac2-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="14ac2-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="14ac2-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14ac2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14ac2-105">Возвращает указатель [IMsgServiceAdmin](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="14ac2-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="14ac2-106">���������</span><span class="sxs-lookup"><span data-stu-id="14ac2-106">Parameters</span></span>

 <span data-ttu-id="14ac2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="14ac2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="14ac2-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="14ac2-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="14ac2-109">_lppServiceAdmin_</span><span class="sxs-lookup"><span data-stu-id="14ac2-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="14ac2-110">[out] Указатель на указатель на объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="14ac2-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="14ac2-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="14ac2-111">Return value</span></span>

<span data-ttu-id="14ac2-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="14ac2-112">S_OK</span></span> 
  
> <span data-ttu-id="14ac2-113">Указатель на объект администрирования службы сообщение успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="14ac2-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="14ac2-114">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="14ac2-114">Notes to callers</span></span>

<span data-ttu-id="14ac2-115">Метод **IMAPISession::AdminServices** создает объект администрирования службы сообщений, объект, который поддерживает интерфейс **IMsgServiceAdmin** и возвращает указатель.</span><span class="sxs-lookup"><span data-stu-id="14ac2-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="14ac2-116">С помощью этого указателя, можно вызвать методы **IMsgServiceAdmin** для измените какие-либо службы сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="14ac2-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="14ac2-117">Помните о том, что эти изменения не вступят в силу до следующего сеанса; не зависит от текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="14ac2-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="14ac2-118">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="14ac2-118">MFCMAPI reference</span></span>

<span data-ttu-id="14ac2-119">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="14ac2-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="14ac2-120">**����**</span><span class="sxs-lookup"><span data-stu-id="14ac2-120">**File**</span></span>|<span data-ttu-id="14ac2-121">**�������**</span><span class="sxs-lookup"><span data-stu-id="14ac2-121">**Function**</span></span>|<span data-ttu-id="14ac2-122">**�����������**</span><span class="sxs-lookup"><span data-stu-id="14ac2-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14ac2-123">MAPIStoreFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="14ac2-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="14ac2-124">GetServerName</span><span class="sxs-lookup"><span data-stu-id="14ac2-124">GetServerName</span></span>  <br/> |<span data-ttu-id="14ac2-125">Mfcmapi (en) использует метод **IMAPISession::AdminServices** для доступа к профилю для чтения имя сервера.</span><span class="sxs-lookup"><span data-stu-id="14ac2-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14ac2-126">См. также</span><span class="sxs-lookup"><span data-stu-id="14ac2-126">See also</span></span>



[<span data-ttu-id="14ac2-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="14ac2-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="14ac2-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="14ac2-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="14ac2-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="14ac2-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="14ac2-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="14ac2-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

