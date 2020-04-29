---
title: имапивиевадвисесинконсавед
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407608"
---
# <a name="imapiviewadvisesinkonsaved"></a><span data-ttu-id="7e5b0-103">IMAPIViewAdviseSink::OnSaved</span><span class="sxs-lookup"><span data-stu-id="7e5b0-103">IMAPIViewAdviseSink::OnSaved</span></span>

  
  
<span data-ttu-id="7e5b0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e5b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e5b0-105">Уведомляет средство просмотра форм о том, что текущее сообщение сохранено в форме.</span><span class="sxs-lookup"><span data-stu-id="7e5b0-105">Notifies the form viewer that the current message in a form has been saved.</span></span>
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a><span data-ttu-id="7e5b0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7e5b0-106">Parameters</span></span>

<span data-ttu-id="7e5b0-107">Нет</span><span class="sxs-lookup"><span data-stu-id="7e5b0-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="7e5b0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e5b0-108">Return value</span></span>

<span data-ttu-id="7e5b0-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e5b0-109">S_OK</span></span> 
  
> <span data-ttu-id="7e5b0-110">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="7e5b0-110">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e5b0-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e5b0-111">Remarks</span></span>

<span data-ttu-id="7e5b0-112">Объект Form вызывает метод **имапивиевадвисесинк:: Onsaveed** после успешного сохранения текущего сообщения в форме.</span><span class="sxs-lookup"><span data-stu-id="7e5b0-112">A form object calls the **IMAPIViewAdviseSink::OnSaved** method after the current message in a form has been successfully saved.</span></span> <span data-ttu-id="7e5b0-113">Это позволяет читателям обновлять окна в соответствии с изменениями сообщения.</span><span class="sxs-lookup"><span data-stu-id="7e5b0-113">Doing so permits viewers to update their windows to reflect changes to the message.</span></span> 
  
<span data-ttu-id="7e5b0-114">Дополнительные сведения об уведомлениях формы можно найти в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="7e5b0-114">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7e5b0-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7e5b0-115">See also</span></span>



[<span data-ttu-id="7e5b0-116">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e5b0-116">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

