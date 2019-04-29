---
title: Имаписессионадминсервицес
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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405907"
---
# <a name="imapisessionadminservices"></a><span data-ttu-id="37a44-103">IMAPISession::AdminServices</span><span class="sxs-lookup"><span data-stu-id="37a44-103">IMAPISession::AdminServices</span></span>

  
  
<span data-ttu-id="37a44-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="37a44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="37a44-105">Возвращает указатель [имсгсервицеадмин](imsgserviceadminiunknown.md) для внесения изменений в службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="37a44-105">Returns an [IMsgServiceAdmin](imsgserviceadminiunknown.md) pointer for making changes to message services.</span></span> 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="37a44-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="37a44-106">Parameters</span></span>

 <span data-ttu-id="37a44-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="37a44-107">_ulFlags_</span></span>
  
> <span data-ttu-id="37a44-108">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="37a44-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="37a44-109">_Лппсервицеадмин_</span><span class="sxs-lookup"><span data-stu-id="37a44-109">_lppServiceAdmin_</span></span>
  
> <span data-ttu-id="37a44-110">вышли Указатель на указатель на объект администрирования службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="37a44-110">[out] A pointer to a pointer to a message service administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="37a44-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="37a44-111">Return value</span></span>

<span data-ttu-id="37a44-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="37a44-112">S_OK</span></span> 
  
> <span data-ttu-id="37a44-113">Указатель на объект администрирования службы сообщений успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="37a44-113">A pointer to a message service administration object was successfully returned.</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="37a44-114">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="37a44-114">Notes to callers</span></span>

<span data-ttu-id="37a44-115">Метод **IMAPISession:: админсервицес** создает объект администрирования службы сообщений, объект, который поддерживает интерфейс **имсгсервицеадмин** , и возвращает указатель.</span><span class="sxs-lookup"><span data-stu-id="37a44-115">The **IMAPISession::AdminServices** method creates a message service administration object, an object that supports the **IMsgServiceAdmin** interface and returns a pointer.</span></span> <span data-ttu-id="37a44-116">С помощью этого указателя можно вызвать методы **имсгсервицеадмин** , чтобы изменить любую службу сообщений в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="37a44-116">By using this pointer, you can call **IMsgServiceAdmin** methods to change any of the message services in the session profile.</span></span> <span data-ttu-id="37a44-117">Обратите внимание, что эти изменения вступают в силу только после следующего сеанса; текущий сеанс не изменяется.</span><span class="sxs-lookup"><span data-stu-id="37a44-117">Be aware that these changes do not take effect until the next session; the current session is unaffected.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="37a44-118">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="37a44-118">MFCMAPI reference</span></span>

<span data-ttu-id="37a44-119">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="37a44-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="37a44-120">**Файл**</span><span class="sxs-lookup"><span data-stu-id="37a44-120">**File**</span></span>|<span data-ttu-id="37a44-121">**Функция**</span><span class="sxs-lookup"><span data-stu-id="37a44-121">**Function**</span></span>|<span data-ttu-id="37a44-122">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="37a44-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="37a44-123">Маписторефунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="37a44-123">MAPIStoreFunctions.cpp</span></span>  <br/> |<span data-ttu-id="37a44-124">Имя_сервера</span><span class="sxs-lookup"><span data-stu-id="37a44-124">GetServerName</span></span>  <br/> |<span data-ttu-id="37a44-125">MFCMAPI использует метод **IMAPISession:: админсервицес** для доступа к профилю для считывания имени сервера.</span><span class="sxs-lookup"><span data-stu-id="37a44-125">MFCMAPI uses the **IMAPISession::AdminServices** method to access the profile to read the server name.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="37a44-126">См. также</span><span class="sxs-lookup"><span data-stu-id="37a44-126">See also</span></span>



[<span data-ttu-id="37a44-127">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="37a44-127">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="37a44-128">IProfAdmin::AdminServices</span><span class="sxs-lookup"><span data-stu-id="37a44-128">IProfAdmin::AdminServices</span></span>](iprofadmin-adminservices.md)
  
[<span data-ttu-id="37a44-129">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="37a44-129">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="37a44-130">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="37a44-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

