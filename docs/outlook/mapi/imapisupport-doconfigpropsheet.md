---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3b3499de9446c83cfc3b97b4d6b02e7c430b65f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586398"
---
# <a name="imapisupportdoconfigpropsheet"></a><span data-ttu-id="d79e1-103">IMAPISupport::DoConfigPropsheet</span><span class="sxs-lookup"><span data-stu-id="d79e1-103">IMAPISupport::DoConfigPropsheet</span></span>

  
  
<span data-ttu-id="d79e1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d79e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d79e1-105">Отображает окно свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d79e1-105">Displays a configuration property sheet.</span></span>
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a><span data-ttu-id="d79e1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d79e1-106">Parameters</span></span>

 <span data-ttu-id="d79e1-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d79e1-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d79e1-108">[in] Дескриптор родительского окна окно свойств.</span><span class="sxs-lookup"><span data-stu-id="d79e1-108">[in] A handle to the parent window of the property sheet.</span></span>
    
 <span data-ttu-id="d79e1-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d79e1-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d79e1-110">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="d79e1-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d79e1-111">_lpszTitle_</span><span class="sxs-lookup"><span data-stu-id="d79e1-111">_lpszTitle_</span></span>
  
> <span data-ttu-id="d79e1-112">[in] Указатель на заголовок страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="d79e1-112">[in] A pointer to the title of the property sheet.</span></span>
    
 <span data-ttu-id="d79e1-113">_lpDisplayTable_</span><span class="sxs-lookup"><span data-stu-id="d79e1-113">_lpDisplayTable_</span></span>
  
> <span data-ttu-id="d79e1-114">[in] Указатель на таблицу отображения, описываются элементы управления для отображения в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="d79e1-114">[in] A pointer to the display table that describes the controls to appear on the property sheet.</span></span>
    
 <span data-ttu-id="d79e1-115">_lpConfigData_</span><span class="sxs-lookup"><span data-stu-id="d79e1-115">_lpConfigData_</span></span>
  
> <span data-ttu-id="d79e1-116">[in] Указатель на реализацию [IMAPIProp](imapipropiunknown.md) для использования для доступа к свойствам конфигурации для отображения в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="d79e1-116">[in] A pointer to the [IMAPIProp](imapipropiunknown.md) implementation to be used for accessing the configuration properties to be displayed on the property sheet.</span></span> 
    
 <span data-ttu-id="d79e1-117">_ulTopPage_</span><span class="sxs-lookup"><span data-stu-id="d79e1-117">_ulTopPage_</span></span>
  
> <span data-ttu-id="d79e1-118">[in] Отсчитываемый от нуля индекс для в верхней части страницы по умолчанию страницу свойств.</span><span class="sxs-lookup"><span data-stu-id="d79e1-118">[in] A zero-based index to the default top page of the property sheet.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d79e1-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d79e1-119">Return value</span></span>

<span data-ttu-id="d79e1-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="d79e1-120">S_OK</span></span> 
  
> <span data-ttu-id="d79e1-121">Окно свойств конфигурации отображенные.</span><span class="sxs-lookup"><span data-stu-id="d79e1-121">The configuration property sheet was displayed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d79e1-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="d79e1-122">Remarks</span></span>

<span data-ttu-id="d79e1-123">Метод **IMAPISupport::DoConfigPropsheet** применяется для всех объектов поддержки.</span><span class="sxs-lookup"><span data-stu-id="d79e1-123">The **IMAPISupport::DoConfigPropsheet** method is implemented for all support objects.</span></span> <span data-ttu-id="d79e1-124">**DoConfigPropSheet** предоставляет стандартный пользовательский интерфейс для отображения свойств поставщиков услуг и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d79e1-124">**DoConfigPropSheet** provides a standard user interface for displaying the properties of service providers and message services.</span></span> <span data-ttu-id="d79e1-125">В этом поле стандартное диалоговое окно следует использовать для всех отображает свойства конфигурации, чтобы пользователи выгоднее согласованного интерфейса Windows.</span><span class="sxs-lookup"><span data-stu-id="d79e1-125">You should use this standard dialog box for all configuration property displays so that users benefit from a consistent Windows interface.</span></span> 
  
<span data-ttu-id="d79e1-126">Поставщики услуг вызова **DoConfigPropSheet** как часть их реализации метода [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) или с помощью кнопки используется для отображения сведений о свойствах.</span><span class="sxs-lookup"><span data-stu-id="d79e1-126">Service providers call **DoConfigPropSheet** as part of their implementation of the [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method or from a button used to display details on properties.</span></span> <span data-ttu-id="d79e1-127">Службы сообщений вызов **DoConfigPropSheet** из их функции точки входа службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="d79e1-127">Message services call **DoConfigPropSheet** from their message service entry point function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d79e1-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="d79e1-128">Notes to callers</span></span>

<span data-ttu-id="d79e1-129">Можно создать в таблице отображения, на который указывает параметр _lpDisplayTable_ путем вызова функции [BuildDisplayTable](builddisplaytable.md) или с помощью пользовательского кода.</span><span class="sxs-lookup"><span data-stu-id="d79e1-129">You can create the display table pointed to by the  _lpDisplayTable_ parameter by calling the [BuildDisplayTable](builddisplaytable.md) function or with custom code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d79e1-130">См. также</span><span class="sxs-lookup"><span data-stu-id="d79e1-130">See also</span></span>



[<span data-ttu-id="d79e1-131">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="d79e1-131">BuildDisplayTable</span></span>](builddisplaytable.md)
  
[<span data-ttu-id="d79e1-132">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="d79e1-132">CreateIProp</span></span>](createiprop.md)
  
[<span data-ttu-id="d79e1-133">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d79e1-133">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="d79e1-134">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d79e1-134">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)
  
[<span data-ttu-id="d79e1-135">IMAPIStatus::SettingsDialog</span><span class="sxs-lookup"><span data-stu-id="d79e1-135">IMAPIStatus::SettingsDialog</span></span>](imapistatus-settingsdialog.md)
  
[<span data-ttu-id="d79e1-136">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d79e1-136">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)
  
[<span data-ttu-id="d79e1-137">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="d79e1-137">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="d79e1-138">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="d79e1-138">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="d79e1-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="d79e1-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

