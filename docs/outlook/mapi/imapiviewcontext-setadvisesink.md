---
title: Имапивиевконтекстсетадвисесинк
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351193"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="3323e-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3323e-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="3323e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3323e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3323e-105">Управляет регистрацией формы для получения уведомлений об изменениях в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="3323e-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="3323e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3323e-106">Parameters</span></span>

 <span data-ttu-id="3323e-107">_пмвнс_</span><span class="sxs-lookup"><span data-stu-id="3323e-107">_pmvns_</span></span>
  
> <span data-ttu-id="3323e-108">возврата Указатель на объект приемника уведомлений формы или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="3323e-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3323e-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3323e-109">Return value</span></span>

<span data-ttu-id="3323e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3323e-110">S_OK</span></span> 
  
> <span data-ttu-id="3323e-111">Уведомление о регистрации или отмене для формы успешно завершено.</span><span class="sxs-lookup"><span data-stu-id="3323e-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3323e-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="3323e-112">Remarks</span></span>

<span data-ttu-id="3323e-113">Объекты форм вызовите метод **имапивиевконтекст:: сетадвисесинк** , чтобы узнать об изменениях в средстве просмотра форм или отменить предыдущую регистрацию.</span><span class="sxs-lookup"><span data-stu-id="3323e-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="3323e-114">Если для _пмвнс_ ЗАДАНО значение null, форма хочет отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="3323e-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="3323e-115">Когда _пмвнс_ указывает на допустимый приемник рекомендаций формы, форма запрашивается для регистрации будущих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="3323e-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3323e-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="3323e-116">Notes to implementers</span></span>

<span data-ttu-id="3323e-117">Когда **сетадвисесинк** включает указатель приемника уведомлений формы, храните ссылку на него до тех пор, пока не будет выполнен другой вызов **сетадвисесинк** для отмены уведомления.</span><span class="sxs-lookup"><span data-stu-id="3323e-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="3323e-118">Отправка уведомления при возникновении изменения в средстве просмотра и при загрузке нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="3323e-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="3323e-119">Дополнительную информацию можно узнать в статье [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="3323e-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3323e-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3323e-120">MFCMAPI reference</span></span>

<span data-ttu-id="3323e-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3323e-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3323e-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3323e-122">**File**</span></span>|<span data-ttu-id="3323e-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3323e-123">**Function**</span></span>|<span data-ttu-id="3323e-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3323e-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3323e-125">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="3323e-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="3323e-126">Кмимапиформвиевер:: Сетадвисесинк</span><span class="sxs-lookup"><span data-stu-id="3323e-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="3323e-127">MFCMAPI реализует метод **имапивиевконтекст:: сетадвисесинк** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="3323e-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3323e-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3323e-128">See also</span></span>



[<span data-ttu-id="3323e-129">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3323e-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

