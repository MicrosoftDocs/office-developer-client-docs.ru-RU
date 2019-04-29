---
title: Имсгсервицеадминадминпровидерс
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422763"
---
# <a name="imsgserviceadminadminproviders"></a><span data-ttu-id="ad5c5-103">IMsgServiceAdmin::AdminProviders</span><span class="sxs-lookup"><span data-stu-id="ad5c5-103">IMsgServiceAdmin::AdminProviders</span></span>

  
  
<span data-ttu-id="ad5c5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad5c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad5c5-105">Возвращает указатель, который предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-105">Returns a pointer that provides access to a provider administration object.</span></span>
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="ad5c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ad5c5-106">Parameters</span></span>

 <span data-ttu-id="ad5c5-107">_Лпуид_</span><span class="sxs-lookup"><span data-stu-id="ad5c5-107">_lpUID_</span></span>
  
> <span data-ttu-id="ad5c5-108">возврата Указатель на структуру [мапиуид](mapiuid.md) , которая содержит уникальный идентификатор для контролируемой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the unique identifier for the message service to be administered.</span></span> 
    
 <span data-ttu-id="ad5c5-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ad5c5-109">_ulFlags_</span></span>
  
> <span data-ttu-id="ad5c5-110">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-110">[in] Always NULL.</span></span> 
    
 <span data-ttu-id="ad5c5-111">_Лпппровидерадмин_</span><span class="sxs-lookup"><span data-stu-id="ad5c5-111">_lppProviderAdmin_</span></span>
  
> <span data-ttu-id="ad5c5-112">вышли Указатель на указатель на объект администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-112">[out] A pointer to a pointer to a provider administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ad5c5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ad5c5-113">Return value</span></span>

<span data-ttu-id="ad5c5-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ad5c5-114">S_OK</span></span> 
  
> <span data-ttu-id="ad5c5-115">Объект администрирования поставщика успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-115">The provider administration object was successfully returned.</span></span>
    
<span data-ttu-id="ad5c5-116">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="ad5c5-116">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ad5c5-117">**Мапиуид** , на который указывает _лпуид_ , не существует.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-117">The **MAPIUID** pointed to by  _lpUID_ does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ad5c5-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad5c5-118">Remarks</span></span>

<span data-ttu-id="ad5c5-119">Метод **имсгсервицеадмин:: админпровидерс** предоставляет доступ к объекту администрирования поставщика.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-119">The **IMsgServiceAdmin::AdminProviders** method provides access to a provider administration object.</span></span> <span data-ttu-id="ad5c5-120">Администрирование поставщика — это объект, который поддерживает интерфейс [ипровидерадмин](iprovideradminiunknown.md) и позволяет клиентам выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ad5c5-120">A provider administration is an object that supports the [IProviderAdmin](iprovideradminiunknown.md) interface and enables clients to do the following:</span></span> 
  
- <span data-ttu-id="ad5c5-121">Добавление поставщиков служб в службу сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-121">Add service providers to a message service.</span></span>
    
- <span data-ttu-id="ad5c5-122">Удаление поставщиков услуг из службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-122">Delete service providers from a message service.</span></span>
    
- <span data-ttu-id="ad5c5-123">Откройте разделы профилей.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-123">Open profile sections.</span></span>
    
- <span data-ttu-id="ad5c5-124">Доступ к таблице поставщика службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-124">Access the message service provider table.</span></span>
    
<span data-ttu-id="ad5c5-125">Типы изменений, которые могут быть применены к службе сообщений в то время, когда профиль используется, зависят от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-125">The types of changes that can actually be made to a message service while the profile is in use depend on the message service.</span></span> <span data-ttu-id="ad5c5-126">Однако большинство служб сообщений не поддерживают такие изменения, как добавление и удаление поставщиков при использовании профиля.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-126">However, most message services do not support changes such as adding and deleting providers while the profile is in use.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ad5c5-127">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="ad5c5-127">Notes to callers</span></span>

<span data-ttu-id="ad5c5-128">Чтобы получить структуру **мапиуид** для службы сообщений для администрирования, извлеките столбец свойства **пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) из строки службы сообщений в таблице служба сообщений.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-128">To retrieve the **MAPIUID** structure for the message service to administer, retrieve the **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property column from the message service's row in the message service table.</span></span> <span data-ttu-id="ad5c5-129">Для получения дополнительных сведений обратитесь к процедуре, описанной в методе [имсгсервицеадмин:: креатемсгсервице](imsgserviceadmin-createmsgservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ad5c5-129">For more information, see the procedure outlined in the [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ad5c5-130">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ad5c5-130">MFCMAPI reference</span></span>

<span data-ttu-id="ad5c5-131">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ad5c5-132">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ad5c5-132">**File**</span></span>|<span data-ttu-id="ad5c5-133">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ad5c5-133">**Function**</span></span>|<span data-ttu-id="ad5c5-134">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ad5c5-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad5c5-135">Мсгсервицетабледлг. cpp</span><span class="sxs-lookup"><span data-stu-id="ad5c5-135">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="ad5c5-136">Кмсгсервицетабледлг:: Ондисплайитем</span><span class="sxs-lookup"><span data-stu-id="ad5c5-136">CMsgServiceTableDlg::OnDisplayItem</span></span>  <br/> |<span data-ttu-id="ad5c5-137">MFCMAPI использует метод **имсгсервицеадмин:: админпровидерс** , чтобы открыть объект администрирования поставщика для службы.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-137">MFCMAPI uses the **IMsgServiceAdmin::AdminProviders** method to open a provider administration object for a service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ad5c5-138">См. также</span><span class="sxs-lookup"><span data-stu-id="ad5c5-138">See also</span></span>



[<span data-ttu-id="ad5c5-139">IProviderAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad5c5-139">IProviderAdmin : IUnknown</span></span>](iprovideradminiunknown.md)
  
[<span data-ttu-id="ad5c5-140">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ad5c5-140">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ad5c5-141">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ad5c5-141">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="ad5c5-142">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ad5c5-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

