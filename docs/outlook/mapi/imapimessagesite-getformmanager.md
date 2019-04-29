---
title: Имапимессажеситежетформманажер
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2d4100d9bcd1b086747d742d9636c4bf7a39f50b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419459"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="8cd1a-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="8cd1a-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="8cd1a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cd1a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cd1a-105">Возвращает интерфейс диспетчера форм, который сервер форм может использовать для открытия другого сервера форм.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="8cd1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8cd1a-106">Parameters</span></span>

 <span data-ttu-id="8cd1a-107">_Ппформмгр_</span><span class="sxs-lookup"><span data-stu-id="8cd1a-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="8cd1a-108">вышли Указатель на указатель на возвращенный интерфейс диспетчера форм.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8cd1a-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8cd1a-109">Return value</span></span>

<span data-ttu-id="8cd1a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cd1a-110">S_OK</span></span> 
  
> <span data-ttu-id="8cd1a-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8cd1a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="8cd1a-112">Remarks</span></span>

<span data-ttu-id="8cd1a-113">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="8cd1a-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8cd1a-114">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8cd1a-114">MFCMAPI reference</span></span>

<span data-ttu-id="8cd1a-115">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8cd1a-116">**Файл**</span><span class="sxs-lookup"><span data-stu-id="8cd1a-116">**File**</span></span>|<span data-ttu-id="8cd1a-117">**Функция**</span><span class="sxs-lookup"><span data-stu-id="8cd1a-117">**Function**</span></span>|<span data-ttu-id="8cd1a-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="8cd1a-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8cd1a-119">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="8cd1a-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="8cd1a-120">Кмимапиформвиевер:: Жетформманажер</span><span class="sxs-lookup"><span data-stu-id="8cd1a-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="8cd1a-121">MFCMAPI использует метод **имапимессажесите:: жетформманажер** , чтобы вызвать [мапиопенформмгр](mapiopenformmgr.md) и вернуть результаты этого вызова.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cd1a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="8cd1a-122">See also</span></span>



[<span data-ttu-id="8cd1a-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="8cd1a-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="8cd1a-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8cd1a-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="8cd1a-125">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="8cd1a-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="8cd1a-126">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="8cd1a-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

